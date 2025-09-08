# デザインガイド - オランダ総選挙2025サイト

## 📋 基本情報
- **サイトURL**: https://bonomari.github.io/nl-election2025-report/
- **作成日**: 2025年9月8日
- **最終更新**: 2025年9月8日

## 🎨 カラーパレット（確定版）

### **基本カラー**
- **プライマリー**: `#1e40af` (ロイヤルブルー)
- **セカンダリー**: `#059669` (グリーン)
- **アクセント**: `#dc2626` (レッド)

### **政党別カラー（絶対変更禁止）**
```css
/* PVV - オレンジからブルーへのグラデーション */
.party-pvv { 
    background: linear-gradient(135deg, #ea580c, #1e40af);
    color: white;
}

/* GL–PvdA - グリーンからレッドへのグラデーション */
.party-gl-pvda { 
    background: linear-gradient(135deg, #059669, #dc2626);
    color: white;
}

/* VVD - 濃紺 */
.party-vvd { 
    background: #1e3a8a;
    color: white;
}

/* NSC - ティール */
.party-nsc { 
    background: #0891b2;
    color: white;
}

/* BBB - ライトグリーン */
.party-bbb { 
    background: #84cc16;
    color: white;
}
```

### **中規模政党カラー**
```css
/* D66 - ライトブルー */
.party-d66 { background: #0ea5e9; color: white; }

/* SP - 赤 */
.party-sp { background: #dc2626; color: white; }

/* Volt - 紫 */
.party-volt { background: #7c3aed; color: white; }

/* FvD - ダークグレー */
.party-fvd { background: #374151; color: white; }
```

## 🏗️ 基本レイアウト

### **ヘッダー**
```css
header {
    background: linear-gradient(135deg, #1e40af, #3b82f6);
    color: white;
    padding: 30px;
    border-radius: 10px;
}
```

### **セクション見出し**
```css
.section h2 {
    color: #1e40af;  /* ロイヤルブルー */
    border-bottom: 2px solid #eee;
}
```

### **更新日表示**
```css
.last-updated {
    background: #059669;  /* グリーン */
    color: white;
    border-radius: 20px;
}
```

## 📄 ファイル命名規則

### **政党ページ**
- ✅ `PVV.html`
- ✅ `GL_PvdA.html` (アンダースコア使用)
- ✅ `VVD.html`
- ✅ `NSC.html`
- ✅ `BBB.html`
- ❌ `GL-PvdA.html` (ハイフン禁止)

### **その他ページ**
- `middle-parties.html` (中規模政党)
- `small-parties.html` (小規模政党)
- `overview.html` (総合分析)

### **週次レポート**
- `weekly/week36-2025.html`
- `weekly/week35-2025.html`

## 🚫 禁止事項

### **絶対禁止**
1. **オレンジ色の多用** - オランダ国色だが政党色ではない
2. **政党カラーの勝手な変更** - 上記CSS以外使用禁止
3. **ハイフン入りファイル名** - 404エラーの原因

### **避けるべき色**
- `#FF6B35` (オレンジ) - ヘッダーやメイン色での使用禁止
- `#F7931E` (明るいオレンジ) - 同上

## 📊 政策マトリックス仕様

### **スタンス分類カラー**
```css
.stance-support {
    background: #d4edda;    /* 緑背景 */
    color: #155724;         /* 緑文字 */
}

.stance-conditional {
    background: #fff3cd;    /* 黄背景 */
    color: #856404;         /* 黄文字 */
}

.stance-oppose {
    background: #f8d7da;    /* 赤背景 */
    color: #721c24;         /* 赤文字 */
}
```

### **4軸政策分析**
1. **対NATO姿勢**: 支持/条件付き支持/反対
2. **対EU統合**: 統合推進/現状維持/懐疑的
3. **移民政策**: 受入拡大/現状維持/制限強化  
4. **防衛費負担**: GDP2%以上/現状維持/削減志向

## 🔄 更新手順

### **新スレッド開始時**
1. 「docs/design-guide.md参照」と最初に指示
2. 政党カラーは上記CSS通り厳守
3. ヘッダーはロイヤルブルー厳守

### **データ更新時**
- HTMLの中身のみ変更
- CSSは原則変更しない
- 新政党追加時のみCSS追加

### **新ページ作成時**
- 既存ページのCSS部分をコピー
- 政党カラーは上記定義を使用
- ファイル名は命名規則に従う

## 📝 アーカイブ方針

### **用語統一**
- ✅ "アーカイブ" 
- ❌ "魚拓" (使用禁止)

### **アーカイブステータス**
```css
.archived { background: #d4edda; color: #155724; }      /* 完了 */
.missing { background: #f8d7da; color: #721c24; }       /* 要収集 */
.pending { background: #fff3cd; color: #856404; }       /* 収集中 */
```

## 🎯 品質チェックリスト

### **新ページ作成時の確認項目**
- [ ] ヘッダーがロイヤルブルーか
- [ ] 政党カラーが上記CSS通りか
- [ ] オレンジ色を多用していないか
- [ ] ファイル名が命名規則通りか
- [ ] リンクが正しく動作するか
- [ ] レスポンシブ対応できているか

---

## 🚨 緊急時の対処

**外観が崩れた場合**
1. このガイドのCSS定義を確認
2. 政党カラーが正しく適用されているか確認
3. ファイル名にハイフンが入っていないか確認

**新しい開発者/AIアシスタントへの引き継ぎ**
1. このファイルを最初に読ませる
2. 「政党カラーとヘッダーカラーは絶対変更禁止」を強調
3. サンプルとして既存のindex.htmlを参照させる
