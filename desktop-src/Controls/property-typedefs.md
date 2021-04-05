---
title: Identificatori di proprietà (controlli Windows)
description: In questo argomento vengono fornite informazioni sui valori definiti utilizzati per recuperare le proprietà degli stili di visualizzazione. Le definizioni si trovano in Vssym32. h.
ms.assetid: b0e22022-fea9-43d1-8ef0-7a1c518760f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0869ac80332a5dbdb146ee255f5c9e73f4a812
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739279"
---
# <a name="property-identifiers-windows-controls"></a>Identificatori di proprietà (controlli Windows)

In questo argomento vengono fornite informazioni sui valori definiti utilizzati per recuperare le proprietà degli stili di visualizzazione. Le definizioni si trovano in Vssym32. h.

## <a name="property-types"></a>Tipi di proprietà

Nella tabella seguente sono elencati i tipi di proprietà primitivi. I valori nella prima colonna non vengono in genere usati dalle applicazioni, ma consentono di classificare gli identificatori di proprietà.



| Tipo di dati       | Descrizione                              | Tipo restituito                          | Funzione di recupero                                                                                                     |
|-----------------|------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| \_bool TMT       | **True** o **false**                    | Boolean                                | [**GetThemeBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebool), [ **GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                       |
| \_colore TMT      | Valore colore RGB                          | Struttura [**COLORREF**](/windows/desktop/gdi/colorref) | [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor), [ **GetThemeSysColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolor)                                   |
| \_DISKSTREAM TMT | Flusso del disco                              | **HINSTANCE**                          | [**GetThemeStream**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestream)                                                                               |
| \_enumerazione TMT       | Valore enumerato                         | Enumerazione                            | [**GetThemeEnumValue**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeenumvalue).                                                                        |
| \_nome file TMT   | Nome file relativo alla directory del tema | Matrice **WCHAR**                        | [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)                                                                           |
| \_tipo di carattere TMT       | Descrizione carattere                         | [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) (struttura)   | [**GetThemeFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefont), [ **GetThemeSysFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysfont)                                       |
| \_HBITMAP TMT    | Bitmap                                   | Handle **HBITMAP**                     | [**GetThemeBitmap**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebitmap)                                                                               |
| \_int TMT        | Numero con segno                            | Integer                                | [**GetThemeInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeint), [**GetThemeSysInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysint), [**GetThemeMetric**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememetric) |
| TMT \_ intlr    | Elenco di numeri interi                         | Struttura [**intlt**](/windows/desktop/api/UxTheme/ns-uxtheme-intlist)   | [**GetThemeIntList**](/windows/desktop/api/UxTheme/nf-uxtheme-getthemeintlist)                                                                             |
| \_margini TMT    | Margini: a sinistra, in alto, a destra e in basso    | Struttura [**margini**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins)   | [**GetThemeMargins**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins)                                                                             |
| \_posizione TMT   | Posizione di un elemento                      | Struttura [**Point**](/previous-versions//dd162805(v=vs.85))       | [**GetThemePosition**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeposition)                                                                           |
| TMT \_ Rect       | Dimensioni e posizione di un rettangolo         | Struttura [**Rect**](/previous-versions//dd162897(v=vs.85))         | [**GetThemeRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemerect)                                                                                   |
| \_dimensioni TMT       | Dimensioni di un elemento                          | Struttura [**dimensioni**](/previous-versions//dd145106(v=vs.85))         | [**GetThemePartSize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepartsize)                                                                           |
| \_stringa TMT     | Stringa Unicode                           | Matrice **WCHAR**                        | [**GetThemeString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestring), [ **GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)                               |



 

## <a name="property-ids"></a>ID di proprietà

Di seguito sono riportati i valori definiti per le proprietà del tema, raggruppati per tipo di dati.

**\_bool TMT**



| ID                        | Note                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ALWAYSSHOWSIZINGBAR TMT  | **True** se la barra di ridimensionamento associata alla parte e allo stato deve essere sempre visualizzata.                                                                                                                           |
| \_ridimensionamento automatico TMT             | **True** se l'area della didascalia non client associata alla parte e allo stato variano con la larghezza del testo.                                                                                                                 |
| \_BGFILL TMT               | **True** se le immagini di dimensioni reali associate alla parte e allo stato devono essere disegnate sul riempimento dello sfondo.                                                                                                        |
| \_BORDERONLY TMT           | **True** se l'immagine associata alla parte e allo stato deve avere solo il bordo disegnato.                                                                                                                     |
| TMT \_ composito           | **True** se il controllo associato alla parte e allo stato gestirà la propria composizione di immagini.                                                                                                           |
| \_COMPOSITEDOPAQUE TMT     |                                                                                                                                                                                                                 |
| \_DRAWBORDERS TMT          |                                                                                                                                                                                                                 |
| \_FLATMENUS TMT            | Vedere [**GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool).                                                                                                                                                                 |
| \_GLYPHONLY TMT            | **True** se il glifo associato alla parte e allo stato deve essere disegnato senza uno sfondo.                                                                                                                  |
| \_GLYPHTRANSPARENT TMT     | **True** se il glifo associato alla parte e allo stato hanno aree trasparenti. Vedere [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor) per la definizione del \_ valore GLYPHCOLOR di TMT che definisce il colore trasparente. |
| \_INTEGRALSIZING TMT       | **True** se l'immagine o il bordo TrueSize associato alla parte e allo stato deve essere ridimensionato a un fattore di 2.                                                                                                     |
| \_LOCALIZEDMIRRORIMAGE TMT |                                                                                                                                                                                                                 |
| \_MIRRORIMAGE TMT          | **True** se l'immagine associata alla parte e allo stato deve essere capovolta se la finestra viene visualizzata in modalità di lettura da destra a sinistra.                                                                         |
| \_NOETCHEDEFFECT TMT       |                                                                                                                                                                                                                 |
| \_SCALEDBACKGROUND TMT     |                                                                                                                                                                                                                 |
| \_SOURCEGROW TMT           | **True** se l'immagine associata alla parte e allo stato sarà ridimensionata di dimensioni maggiori, se necessario.                                                                                                                |
| \_SOURCESHRINK TMT         | **True** se l'immagine associata alla parte e allo stato aumenterà di dimensioni minori se necessario.                                                                                                               |
| \_TEXTAPPLYOVERLAY TMT     |                                                                                                                                                                                                                 |
| \_TEXTGLOW TMT             |                                                                                                                                                                                                                 |
| \_TEXTITALIC TMT           |                                                                                                                                                                                                                 |
| TMT \_ trasparente          |                                                                                                                                                                                                                 |
| \_UNIFORMSIZING TMT        | **True** se l'immagine associata alla parte e allo stato deve avere altezza e larghezza uguali.                                                                                                                      |
| \_USERPICTURE TMT          | **True** se l'immagine associata alla parte e allo stato è basata sull'utente corrente.                                                                                                                          |



 

**\_colore TMT**



| ID                           | Note                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ACCENTCOLORHINT TMT         | Colore utilizzato come hint di colore per i controlli personalizzati.                                                                                                                                    |
| \_ACTIVEBORDER TMT            |                                                                                                                                                                                                |
| \_ACTIVECAPTION TMT           |                                                                                                                                                                                                |
| \_APPWORKSPACE TMT            |                                                                                                                                                                                                |
| \_sfondo TMT              |                                                                                                                                                                                                |
| \_BLENDCOLOR TMT              | Colore utilizzato come colore di Blend.                                                                                                                                                               |
| \_BODYTEXTCOLOR TMT           |                                                                                                                                                                                                |
| \_BorderColor TMT             | Colore del bordo associato alla parte e allo stato.                                                                                                                                    |
| \_BORDERCOLORHINT TMT         | Colore utilizzato come hint per il colore del bordo per i controlli personalizzati.                                                                                                                                     |
| \_BTNFACE TMT                 |                                                                                                                                                                                                |
| \_BTNHIGHLIGHT TMT            |                                                                                                                                                                                                |
| \_BTNSHADOW TMT               |                                                                                                                                                                                                |
| \_BTNTEXT TMT                 |                                                                                                                                                                                                |
| \_BUTTONALTERNATEFACE TMT     |                                                                                                                                                                                                |
| \_CAPTIONTEXT TMT             |                                                                                                                                                                                                |
| \_DKSHADOW3D TMT              |                                                                                                                                                                                                |
| \_EDGEDKSHADOWCOLOR TMT       | Colore dell'ombreggiatura scura del bordo associato a questa parte e allo stato.                                                                                                                         |
| \_EDGEFILLCOLOR TMT           | Colore di riempimento del bordo associato a questa parte e allo stato.                                                                                                                                |
| \_EDGEHIGHLIGHTCOLOR TMT      | Colore di evidenziazione del bordo associato a questa parte e allo stato.                                                                                                                           |
| \_EDGELIGHTCOLOR TMT          | Colore chiaro del bordo associato a questa parte e allo stato.                                                                                                                               |
| \_EDGESHADOWCOLOR TMT         | Colore dell'ombreggiatura del bordo associato a questa parte e allo stato.                                                                                                                              |
| \_FillColor TMT               | Colore del riempimento dello sfondo associato alla parte e allo stato.                                                                                                                           |
| \_FILLCOLORHINT TMT           | Colore utilizzato come hint per il colore di riempimento per i controlli personalizzati.                                                                                                                                       |
| \_FROMCOLOR1 TMT              |                                                                                                                                                                                                |
| \_FROMCOLOR2 TMT              |                                                                                                                                                                                                |
| \_FROMCOLOR3 TMT              |                                                                                                                                                                                                |
| \_FROMCOLOR4 TMT              |                                                                                                                                                                                                |
| \_FROMCOLOR5 TMT              |                                                                                                                                                                                                |
| \_GLOWCOLOR TMT               | Colore dell'alone prodotto chiamando [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon) utilizzando questa parte e lo stato.                                                                                    |
| \_GLYPHTEXTCOLOR TMT          | Colore che verrà utilizzato dal glifo basato sui tipi di carattere associato a questa parte e allo stato.                                                                                                              |
| \_GLYPHTRANSPARENTCOLOR TMT   | Colore del glifo trasparente associato a questa parte e allo stato. Se il \_ valore GLYPHTRANSPARENT di TMT per questa parte e lo stato è **true**, le parti del glifo che usano questo colore non vengono disegnate. |
| \_GRADIENTACTIVECAPTION TMT   |                                                                                                                                                                                                |
| \_GRADIENTCOLOR1 TMT          | Primo colore della sfumatura associata a questa parte e allo stato.                                                                                                                           |
| \_GRADIENTCOLOR2 TMT          | Il secondo colore della sfumatura.                                                                                                                                                              |
| \_GRADIENTCOLOR3 TMT          | Terzo colore della sfumatura.                                                                                                                                                               |
| \_GRADIENTCOLOR4 TMT          | Quarto colore della sfumatura.                                                                                                                                                              |
| \_GRADIENTCOLOR5 TMT          | Il quinto colore della sfumatura.                                                                                                                                                               |
| \_GRADIENTINACTIVECAPTION TMT |                                                                                                                                                                                                |
| \_GRAYTEXT TMT                |                                                                                                                                                                                                |
| \_HEADING1TEXTCOLOR TMT       |                                                                                                                                                                                                |
| \_HEADING2TEXTCOLOR TMT       |                                                                                                                                                                                                |
| \_evidenziazione TMT               |                                                                                                                                                                                                |
| \_HIGHLIGHTTEXT TMT           |                                                                                                                                                                                                |
| \_HOTTRACKING TMT             |                                                                                                                                                                                                |
| \_INACTIVEBORDER TMT          |                                                                                                                                                                                                |
| \_INACTIVECAPTION TMT         |                                                                                                                                                                                                |
| \_INACTIVECAPTIONTEXT TMT     |                                                                                                                                                                                                |
| \_INFOBK TMT                  |                                                                                                                                                                                                |
| \_INFOTEXT TMT                |                                                                                                                                                                                                |
| \_LIGHT3D TMT                 |                                                                                                                                                                                                |
| \_menu TMT                    |                                                                                                                                                                                                |
| \_barra dei menu TMT                 |                                                                                                                                                                                                |
| \_MENUHILIGHT TMT             |                                                                                                                                                                                                |
| \_MENUTEXT TMT                |                                                                                                                                                                                                |
| \_barra di scorrimento TMT               |                                                                                                                                                                                                |
| \_SHADOWCOLOR TMT             | Colore dell'ombreggiatura disegnata sotto il testo associato a questa parte e allo stato.                                                                                                             |
| \_TEXTBORDERCOLOR TMT         | Colore del bordo del testo associato a questa parte e allo stato.                                                                                                                              |
| \_TEXTCOLOR TMT               | Colore del testo associato a questa parte e allo stato.                                                                                                                                     |
| \_TEXTCOLORHINT TMT           |                                                                                                                                                                                                |
| \_TEXTSHADOWCOLOR TMT         | Colore dell'ombreggiatura del testo associato a questa parte e allo stato.                                                                                                                              |
| \_TRANSPARENTCOLOR TMT        | Colore trasparente associato a questa parte e allo stato. Se il \_ valore trasparente TMT per questa parte e lo stato è **true**, le parti del grafico che utilizzano questo colore non vengono tracciate.          |
| \_finestra TMT                  |                                                                                                                                                                                                |
| \_WINDOWFRAME TMT             |                                                                                                                                                                                                |
| \_WINDOWTEXT TMT              |                                                                                                                                                                                                |



 

**\_DISKSTREAM TMT**



| ID              | Note |
|-----------------|-------|
| \_ATLASIMAGE TMT |       |



 

**\_enumerazione TMT**



| Enumerazione         | Valori della proprietà                                                                                                                                                                                                                                            | Note                                                                                                                                                |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| BGTYPE              | BT \_ IMAGEFILE, BT \_ BORDERFILL                                                                                                                                                                                                                              | Tipo di disegno di base per questa parte.                                                                                                                |
| BORDERTYPE          | BT \_ Rect, BT \_ ROUNDRECT, BT \_ ellisse                                                                                                                                                                                                                       | Tipo di bordo disegnato se questa parte è un riempimento del bordo.                                                                                              |
| CONTENTALIGNMENT    | CA \_ sinistra, \_ centro CA, CA a \_ destra                                                                                                                                                                                                                            | Allineamento del testo nella didascalia associata a questa parte.                                                                                      |
| ELEMENTO FILLTYPE            | FT \_ Solid, ft \_ VERTGRADIENT, ft \_ HORZGRADIENT, FT \_ RADIALGRADIENT, ft \_ TILEIMAGE                                                                                                                                                                           | Tipo di forma riempimento disegnata se questa parte è un riempimento del bordo.                                                                                          |
| GLYPHTYPE           | GT \_ None, gt \_ IMAGEGLYPH, gt \_ FONTGLYPH                                                                                                                                                                                                                    | Tipo di glifo disegnato in questa parte.                                                                                                                |
| GLYPHFONTSIZINGTYPE | GFST \_ None, GFST \_ size, GFST \_ dpi                                                                                                                                                                                                                          | Tipo di metodo utilizzato per la selezione tra glifi di dimensioni diverse.                                                                                    |
| HALIGN              | HA \_ Left, ha \_ Center, ha a \_ destra                                                                                                                                                                                                                            | Allineamento orizzontale se questa parte utilizza un'immagine di dimensioni reali.                                                                                        |
| ICONEFFECT          | ICE \_ None, Ice \_ Glow, Ice \_ shadow, Ice \_ Pulse, Ice \_ Alpha                                                                                                                                                                                                  | Tipo di effetto da visualizzare quando questa parte viene disegnata usando [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                             |
| IMAGELAYOUT         | IL \_ verticale, il \_ orizzontale                                                                                                                                                                                                                               | Tipo di allineamento utilizzato quando vengono disegnate più immagini.                                                                                           |
| IMAGESELECTTYPE     | IST \_ None, \_ dimensioni IST, ist \_ dpi                                                                                                                                                                                                                             | Tipo di metodo utilizzato per selezionare le immagini di dimensioni per questa parte. Vedere il \_ valore TMT IMAGEFILE1 di [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename). |
| OFFSETTYPE          | OT in \_ uscita, OT in \_ alto, OT in \_ alto, OT \_ BOTTOMLEFT, OT \_ BOTTOMRIGHT, OT \_ BOTTOMMIDDLE, OT \_ MIDDLELEFT, OT MIDDLERIGHT, \_ \_ \_ \_ \_ \_ \_ OT LEFTOFCAPTION, OT RIGHTOFCAPTION, OT LEFTOFLASTBUTTON, OT RIGHTOFLASTBUTTON, OT ABOVELASTBUTTON, OT BELOWLASTBUTTON, OT | Allineamento di questa parte nella finestra.                                                                                                            |
| SIZINGTYPE          | ST \_ TRUESIZE, St \_ stretch, St \_ Tile, ST \_ TILEHORZ, St \_ TILEVERT, St \_ TILECENTER                                                                                                                                                                            | Metodo utilizzato per ridimensionare un'immagine se questa parte utilizza un file di immagine.                                                                                    |
| TEXTSHADOWTYPE      | TST \_ None, TST \_ singolo, TST \_ Continuous                                                                                                                                                                                                                    | Tipo di effetto ombreggiatura da creare dietro il testo associato a questa parte.                                                                             |
| TRUESIZESCALINGTYPE | TSST \_ None, TSST \_ size, TSST \_ dpi                                                                                                                                                                                                                          | Tipo di ridimensionamento utilizzato se questa parte utilizza un'immagine di dimensioni reali.                                                                                       |
| VALIGN              | VA in \_ alto, al centro, va in \_ \_ basso                                                                                                                                                                                                                            | Allineamento verticale se questa parte utilizza un'immagine di dimensioni reali.                                                                                          |



 

**\_nome file TMT**



| ID                  | Note                                                                                                                                        |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| \_GLYPHIMAGEFILE TMT | Nome del file per l'immagine del glifo associato a questa parte e allo stato.                                                                        |
| \_IMAGEFILE TMT      | Nome del file dell'immagine associata a questa parte e stato oppure il nome file di base per più immagini associate a questa parte e allo stato. |
| \_IMAGEFILE1 TMT     | Nome del file della prima immagine ridimensionata associata a questa parte e allo stato, per il supporto di risoluzioni diverse.                            |
| \_IMAGEFILE2 TMT     | Nome del file della seconda immagine ridimensionata.                                                                                                     |
| \_IMAGEFILE3 TMT     | Nome del file della terza immagine ridimensionata.                                                                                                      |
| \_IMAGEFILE4 TMT     | Nome del file della quarta immagine ridimensionata.                                                                                                     |
| \_IMAGEFILE5 TMT     | Nome del file della quinta immagine ridimensionata.                                                                                                      |



 

**\_tipo di carattere TMT**



| ID                    | Note                                                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------|
| \_BODYFONT TMT         |                                                                                                      |
| \_CAPTIONFONT TMT      |                                                                                                      |
| \_GLYPHFONT TMT        | Il tipo di carattere a cui verrà disegnato il glifo associato a questa parte, se vengono usati glifi basati su caratteri. |
| \_HEADING1FONT TMT     |                                                                                                      |
| \_HEADING2FONT TMT     |                                                                                                      |
| \_ICONTITLEFONT TMT    |                                                                                                      |
| \_MENUFONT TMT         |                                                                                                      |
| \_MSGBOXFONT TMT       |                                                                                                      |
| \_SMALLCAPTIONFONT TMT |                                                                                                      |
| \_STATUSFONT TMT       |                                                                                                      |



 

**\_int TMT**



| ID                       | Note                                                                                                                                                                                                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ALPHALEVEL TMT          | Valore alfa (0-255) utilizzato per [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                                                                                                                         |
| \_ALPHATHRESHOLD TMT      | Valore alfa minimo (0-255) che deve essere considerato opaco per un pixel.                                                                                                                                  |
| \_ANIMATIONDELAY TMT      |                                                                                                                                                                                                                  |
| \_ANIMATIONDURATION TMT   |                                                                                                                                                                                                                  |
| \_BORDERSIZE TMT          | Spessore del bordo disegnato se questa parte utilizza un riempimento del bordo.                                                                                                                                               |
| \_set di caratteri TMT             |                                                                                                                                                                                                                  |
| \_COLORIZATIONCOLOR TMT   |                                                                                                                                                                                                                  |
| \_COLORIZATIONOPACITY TMT |                                                                                                                                                                                                                  |
| \_FRAMESPERSECOND TMT     |                                                                                                                                                                                                                  |
| \_FROMHUE1 TMT            |                                                                                                                                                                                                                  |
| \_FROMHUE2 TMT            |                                                                                                                                                                                                                  |
| \_FROMHUE3 TMT            |                                                                                                                                                                                                                  |
| \_FROMHUE4 TMT            |                                                                                                                                                                                                                  |
| \_FROMHUE5 TMT            |                                                                                                                                                                                                                  |
| \_GLOWINTENSITY TMT       |                                                                                                                                                                                                                  |
| \_GLYPHINDEX TMT          | Indice dei caratteri nel tipo di carattere selezionato che verrà utilizzato per il glifo, se la parte utilizza un glifo basato sui tipi di carattere.                                                                                                 |
| \_GRADIENTRATIO1 TMT      | Quantità del primo colore sfumato (TMT \_ GRADIENTCOLOR1) da utilizzare per disegnare la parte. Questo valore può essere compreso tra 0 e 255, ma questo valore e i valori di ognuno dei valori di GRADIENTRATIO devono essere aggiunti fino a 255. |
| \_GRADIENTRATIO2 TMT      | Quantità del secondo colore sfumato (TMT \_ GRADIENTCOLOR2) da utilizzare per disegnare la parte.                                                                                                                        |
| \_GRADIENTRATIO3 TMT      | Quantità del terzo colore sfumato (TMT \_ GRADIENTCOLOR3) da utilizzare per disegnare la parte.                                                                                                                         |
| \_GRADIENTRATIO4 TMT      | Quantità del quarto colore sfumato (TMT \_ GRADIENTCOLOR4) da utilizzare per disegnare la parte.                                                                                                                        |
| \_GRADIENTRATIO5 TMT      | Quantità del quinto colore sfumato (TMT \_ GRADIENTCOLOR5) da utilizzare per disegnare la parte.                                                                                                                         |
| \_altezza TMT              | Altezza della parte.                                                                                                                                                                                          |
| \_IMAGECOUNT TMT          | Il numero di immagini di stato presenti in un file di immagine.                                                                                                                                                             |
| \_MINCOLORDEPTH TMT       |                                                                                                                                                                                                                  |
| \_MINDPI1 TMT             | Numero minimo di punti per pollice (dpi) per cui è stato progettato il primo file di immagine.                                                                                                                                      |
| \_MINDPI2 TMT             | Valore dpi minimo per il quale è stato progettato il secondo file di immagine.                                                                                                                                                     |
| \_MINDPI3 TMT             | Valore dpi minimo per il quale è stato progettato il terzo file di immagine.                                                                                                                                                      |
| \_MINDPI4 TMT             | Valore dpi minimo per cui è stato progettato il quarto file di immagine.                                                                                                                                                     |
| \_MINDPI5 TMT             | Valore dpi minimo per il quale è stato progettato il quinto file di immagine.                                                                                                                                                      |
| \_opacità TMT             |                                                                                                                                                                                                                  |
| \_PIXELSPERFRAME TMT      |                                                                                                                                                                                                                  |
| \_PROGRESSCHUNKSIZE TMT   | Dimensioni delle forme "blocco" del controllo dello stato di avanzamento che definiscono la distanza di avanzamento di un'operazione.                                                                                                                 |
| \_PROGRESSSPACESIZE TMT   | Dimensioni totali di tutti i "blocchi" del controllo dello stato di avanzamento.                                                                                                                                                          |
| \_ROUNDCORNERHEIGHT TMT   | Arrotondamento (da 0 a 100%) degli angoli della parte.                                                                                                                                                          |
| \_ROUNDCORNERWIDTH TMT    | Arrotondamento (da 0 a 100%) degli angoli della parte.                                                                                                                                                          |
| \_saturazione TMT          | Quantità di saturazione (0-255) da applicare a un'icona disegnata usando [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                                                                                         |
| \_TEXTBORDERSIZE TMT      | Spessore del bordo tracciato intorno ai caratteri di testo.                                                                                                                                                        |
| \_TEXTGLOWSIZE TMT        |                                                                                                                                                                                                                  |
| \_TOCOLOR1 TMT            |                                                                                                                                                                                                                  |
| \_TOCOLOR2 TMT            |                                                                                                                                                                                                                  |
| \_TOCOLOR3 TMT            |                                                                                                                                                                                                                  |
| \_TOCOLOR4 TMT            |                                                                                                                                                                                                                  |
| \_TOCOLOR5 TMT            |                                                                                                                                                                                                                  |
| \_TOHUE1 TMT              |                                                                                                                                                                                                                  |
| \_TOHUE2 TMT              |                                                                                                                                                                                                                  |
| \_TOHUE3 TMT              |                                                                                                                                                                                                                  |
| \_TOHUE4 TMT              |                                                                                                                                                                                                                  |
| \_TOHUE5 TMT              |                                                                                                                                                                                                                  |
| \_TRUESIZESTRETCHMARK TMT | Percentuale delle dimensioni originali di un'immagine di dimensioni reali in corrispondenza della quale l'immagine verrà allungata.                                                                                                                        |
| \_larghezza TMT               | Larghezza della parte.                                                                                                                                                                                           |



 

**TMT \_ intlr**



| ID                       | Note |
|--------------------------|-------|
| \_TRANSITIONDURATIONS TMT |       |



 

**\_margini TMT**



| ID                  | Note                                                                   |
|---------------------|-------------------------------------------------------------------------|
| \_CAPTIONMARGINS TMT | I margini che definiscono dove il testo della didascalia può essere inserito all'interno di una parte. |
| \_CONTENTMARGINS TMT | I margini che definiscono la posizione in cui il contenuto può essere inserito all'interno di una parte.      |
| \_SIZINGMARGINS TMT  | Margini utilizzati per dimensionare un'immagine di dimensioni non reali.                      |



 

**\_posizione TMT**



| ID                    | Note                                                                                                        |
|-----------------------|--------------------------------------------------------------------------------------------------------------|
| \_MINSIZE TMT          | Dimensioni minime per cui è possibile utilizzare il file di immagine normale prima del passaggio al file di immagine più piccolo successivo.   |
| \_DIMMINIMA1 TMT         | Dimensioni minime per cui è possibile utilizzare il primo file di immagine piccolo.                                            |
| \_MINSIZE2 TMT         | Dimensioni minime per cui è possibile utilizzare il secondo file di immagine piccolo.                                           |
| \_MINSIZE3 TMT         | Dimensioni minime per cui è possibile utilizzare il terzo file di immagine piccolo.                                            |
| \_MINSIZE4 TMT         | Dimensioni minime per cui è possibile utilizzare il quarto file di immagine piccolo.                                           |
| \_MINSIZE5 TMT         | Dimensioni minime per le quali è possibile utilizzare il quinto file di immagine piccolo.                                            |
| \_NORMALSIZE TMT       | Dimensione dell'immagine normale associata a questa parte.                                                      |
| \_offset TMT           | Offset di posizione dall'allineamento per questa parte. L'allineamento è definito dal \_ valore OFFSETTYPE di TMT. |
| \_TEXTSHADOWOFFSET TMT | Offset dal testo in cui vengono disegnate le ombreggiature del testo.                                                    |



 

**TMT \_ Rect**



| ID                       | Note                         |
|--------------------------|-------------------------------|
| \_ANIMATIONBUTTONRECT TMT |                               |
| \_ATLASRECT TMT           |                               |
| \_CUSTOMSPLITRECT TMT     |                               |
| \_DEFAULTPANESIZE TMT     | Dimensioni predefinite della parte. |



 

**\_dimensioni TMT**



| ID                      | Note                     |
|-------------------------|---------------------------|
| \_CAPTIONBARHEIGHT TMT   | Altezza della barra del titolo.       |
| \_CAPTIONBARWIDTH TMT    | Larghezza della barra del titolo.        |
| \_MENUBARHEIGHT TMT      | Altezza della barra dei menu.          |
| \_MENUBARWIDTH TMT       | Larghezza della barra dei menu.           |
| \_PADDEDBORDERWIDTH TMT  | Spessore bordo imbottito.      |
| \_SCROLLBARHEIGHT TMT    | Altezza barra di scorrimento.        |
| \_SCROLLBARWIDTH TMT     | Larghezza della barra di scorrimento.         |
| \_SIZINGBORDERWIDTH TMT  | Larghezza di un bordo di ridimensionamento. |
| \_SMCAPTIONBARHEIGHT TMT | Altezza della barra del titolo.       |
| \_SMCAPTIONBARWIDTH TMT  | Larghezza della barra del titolo.        |



 

**\_stringa TMT**



| ID                   | Note                                               |
|----------------------|-----------------------------------------------------|
| \_alias TMT           |                                                     |
| \_ATLASINPUTIMAGE TMT |                                                     |
| autore di TMT \_          |                                                     |
| \_CLASSICVALUE TMT    |                                                     |
| \_COLORSCHEMES TMT    |                                                     |
| \_società TMT         |                                                     |
| \_Copyright TMT       |                                                     |
| \_CSSNAME TMT         | Vedere [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring). |
| Descrizione di TMT \_     |                                                     |
| \_DisplayName TMT     |                                                     |
| \_LASTUPDATED TMT     |                                                     |
| \_dimensioni TMT           |                                                     |
| \_testo TMT            | Testo visualizzato dalla parte.                     |
| \_Descrizione comando TMT         |                                                     |
| \_URL TMT             |                                                     |
| versione di TMT \_         |                                                     |
| XmlName TMT \_         | Vedere [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring). |
| \_nome TMT            |                                                     |



 

 

 
