---
title: Identificatori di proprietà (Windows controlli)
description: Questo argomento contiene informazioni sui valori definiti usati per recuperare le proprietà degli stili di visualizzazione. Le definizioni sono disponibili in Vssym32.h.
ms.assetid: b0e22022-fea9-43d1-8ef0-7a1c518760f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf20429d5eb5bd45ea850e3b77c5734ab6b8e0fa0e63fe4c1d2b1c918f837f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078865"
---
# <a name="property-identifiers-windows-controls"></a>Identificatori di proprietà (Windows controlli)

Questo argomento contiene informazioni sui valori definiti usati per recuperare le proprietà degli stili di visualizzazione. Le definizioni sono disponibili in Vssym32.h.

## <a name="property-types"></a>Tipi di proprietà

Nella tabella seguente sono elencati i tipi di proprietà primitive. I valori nella prima colonna non vengono in genere usati dalle applicazioni, ma forniscono un modo per classificare gli identificatori di proprietà.



| Tipo di dati       | Descrizione                              | Tipo restituito                          | Funzione di recupero                                                                                                     |
|-----------------|------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| TMT \_ BOOL       | **TRUE** o **FALSE**                    | Boolean                                | [**GetThemeBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebool), [ **GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                       |
| COLORE \_ TMT      | Valore del colore RGB                          | [**Struttura COLORREF**](/windows/desktop/gdi/colorref) | [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor), [ **GetThemeSysColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolor)                                   |
| TMT \_ DISKSTREAM | Flusso del disco                              | **Hinstance**                          | [**GetThemeStream**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestream)                                                                               |
| Enumerazione \_ TMT       | Valore enumerato                         | Enumerazione                            | [**GetThemeEnumValue**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeenumvalue).                                                                        |
| NOME FILE \_ TMT   | Nome file relativo alla directory del tema | **Matrice WCHAR**                        | [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)                                                                           |
| CARATTERE \_ TMT       | Descrizione del tipo di carattere                         | [**Struttura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)   | [**GetThemeFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefont), [ **GetThemeSysFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysfont)                                       |
| TMT \_ HBITMAP    | Bitmap                                   | **Handle HBITMAP**                     | [**GetThemeBitmap**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebitmap)                                                                               |
| TMT \_ INT        | Numero con segno                            | Intero                                | [**GetThemeInt,**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeint) [**GetThemeSysInt,**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysint) [**GetThemeMetric**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememetric) |
| TMT \_ INTLIST    | Elenco di numeri interi                         | [**Struttura INTLIST**](/windows/desktop/api/UxTheme/ns-uxtheme-intlist)   | [**GetThemeIntList**](/windows/desktop/api/UxTheme/nf-uxtheme-getthemeintlist)                                                                             |
| MARGINI \_ TMT    | Margini: a sinistra, in alto, a destra e in basso    | [**Struttura MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins)   | [**GetThemeMargins**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins)                                                                             |
| POSIZIONE \_ TMT   | Posizione di un elemento                      | [**Struttura POINT**](/previous-versions//dd162805(v=vs.85))       | [**GetThemePosition**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeposition)                                                                           |
| TMT \_ RECT       | Dimensioni e posizione di un rettangolo         | [**Struttura RECT**](/previous-versions//dd162897(v=vs.85))         | [**GetThemeRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemerect)                                                                                   |
| DIMENSIONI \_ TMT       | Dimensioni di un elemento                          | [**Struttura SIZE**](/previous-versions//dd145106(v=vs.85))         | [**GetThemePartSize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepartsize)                                                                           |
| STRINGA \_ TMT     | Stringa Unicode                           | **Matrice WCHAR**                        | [**GetThemeString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestring), [ **GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)                               |



 

## <a name="property-ids"></a>ID di proprietà

Di seguito sono riportati i valori definiti per le proprietà del tema, raggruppati per tipo di dati.

**TMT \_ BOOL**



| ID                        | Note                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALWAYSSHOWSIZINGBAR  | **TRUE** se la barra di ridimensionamento associata alla parte e allo stato deve essere sempre visualizzata.                                                                                                                           |
| TMT \_ AUTOSIZE             | **TRUE** se l'area della didascalia non client associata alla parte e allo stato variano in base alla larghezza del testo.                                                                                                                 |
| TMT \_ BGFILL               | **TRUE** se le immagini di dimensioni true associate alla parte e allo stato devono essere disegnate sul riempimento dello sfondo.                                                                                                        |
| TMT \_ BORDERONLY           | **TRUE** se all'immagine associata alla parte e allo stato deve essere disegnato solo il bordo.                                                                                                                     |
| TMT \_ COMPOSITED           | **TRUE** se il controllo associato alla parte e allo stato gestirà la composizione delle immagini.                                                                                                           |
| TMT \_ COMPOSITEDOPAQUE     |                                                                                                                                                                                                                 |
| \_DRAWBORDER TMT          |                                                                                                                                                                                                                 |
| MENU FLAT TMT \_            | Vedere [**GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool).                                                                                                                                                                 |
| TMT \_ GLYPHONLY            | **TRUE** se il glifo associato alla parte e allo stato deve essere disegnato senza uno sfondo.                                                                                                                  |
| TMT \_ GLYPHTRANSPARENT     | **TRUE** se il glifo associato alla parte e allo stato ha aree trasparenti. Vedere [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor) per la definizione del valore \_ TMT GLYPHCOLOR che definisce il colore trasparente. |
| INTEGRALIZZAZIONE \_ TMT       | **TRUE** se l'immagine truesize o il bordo associato alla parte e allo stato devono essere ridimensionati in base a un fattore 2.                                                                                                     |
| TMT \_ LOCALIZEDMIRRORIMAGE |                                                                                                                                                                                                                 |
| TMT \_ MIRRORIMAGE          | **TRUE** se l'immagine associata alla parte e allo stato deve essere capovolta se la finestra viene visualizzata in modalità di lettura da destra a sinistra.                                                                         |
| TMT \_ NOETCHEDEFFECT       |                                                                                                                                                                                                                 |
| TMT \_ SCALEDBACKGROUND     |                                                                                                                                                                                                                 |
| TMT \_ SOURCEGROW           | **TRUE** se le dimensioni dell'immagine associata alla parte e allo stato saranno maggiori se necessario.                                                                                                                |
| ORIGINI \_ TMTHRINK         | **TRUE** se le dimensioni dell'immagine associata alla parte e allo stato verranno ridotte se necessario.                                                                                                               |
| TESTO \_ TMTAPPLYOVERLAY     |                                                                                                                                                                                                                 |
| TMT \_ TEXTGLOW             |                                                                                                                                                                                                                 |
| TMT \_ TEXTITALIC           |                                                                                                                                                                                                                 |
| TMT \_ TRANSPARENT          |                                                                                                                                                                                                                 |
| UNIFORMIZZAZIONE \_ TMT        | **TRUE** se l'immagine associata alla parte e allo stato deve avere altezza e larghezza uguali.                                                                                                                      |
| TMT \_ USERPICTURE          | **TRUE** se l'immagine associata alla parte e allo stato è basata sull'utente corrente.                                                                                                                          |



 

**COLORE \_ TMT**



| ID                           | Note                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ACCENTCOLORHINT         | Colore utilizzato come suggerimento per il colore principale per i controlli personalizzati.                                                                                                                                    |
| TMT \_ ACTIVEBORDER            |                                                                                                                                                                                                |
| TMT \_ ACTIVECAPTION           |                                                                                                                                                                                                |
| TMT \_ APPWORKSPACE            |                                                                                                                                                                                                |
| SFONDO \_ TMT              |                                                                                                                                                                                                |
| TMT \_ BLENDCOLOR              | Colore utilizzato come colore di blend.                                                                                                                                                               |
| TMT \_ BODYTEXTCOLOR           |                                                                                                                                                                                                |
| COLORE BORDO \_ TMT             | Colore del bordo associato alla parte e allo stato.                                                                                                                                    |
| TMT \_ BORDERCOLORHINT         | Colore utilizzato come suggerimento del colore del bordo per i controlli personalizzati.                                                                                                                                     |
| TMT \_ BTNFACE                 |                                                                                                                                                                                                |
| TMT \_ BTNHIGHLIGHT            |                                                                                                                                                                                                |
| TMT \_ BTNSHADOW               |                                                                                                                                                                                                |
| TMT \_ BTNTEXT                 |                                                                                                                                                                                                |
| PULSANTE \_ TMTALTERNATEFACE     |                                                                                                                                                                                                |
| TMT \_ CAPTIONTEXT             |                                                                                                                                                                                                |
| TMT \_ DKSHADOW3D              |                                                                                                                                                                                                |
| TMT \_ EDGEDKSHADOWCOLOR       | Colore dell'ombreggiatura scura del bordo associato a questa parte e a questo stato.                                                                                                                         |
| TMT \_ EDGEFILLCOLOR           | Colore di riempimento del bordo associato a questa parte e allo stato.                                                                                                                                |
| TMT \_ EDGEHIGHLIGHTCOLOR      | Colore di evidenziazione del bordo associato a questa parte e allo stato.                                                                                                                           |
| TMT \_ EDGELIGHTCOLOR          | Colore chiaro del bordo associato a questa parte e allo stato.                                                                                                                               |
| TMT \_ EDGESHADOWCOLOR         | Colore dell'ombreggiatura del bordo associato a questa parte e allo stato.                                                                                                                              |
| TMT \_ FILLCOLOR               | Colore del riempimento dello sfondo associato alla parte e allo stato.                                                                                                                           |
| TMT \_ FILLCOLORHINT           | Colore utilizzato come suggerimento per il colore di riempimento per i controlli personalizzati.                                                                                                                                       |
| TMT \_ FROMCOLOR1              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR2              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR3              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR4              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR5              |                                                                                                                                                                                                |
| TMT \_ ALONECOLOR               | Colore dell'alone prodotto chiamando [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon) usando questa parte e lo stato.                                                                                    |
| TMT \_ GLYPHTEXTCOLOR          | Colore che verrà utilizzato dal glifo basato sul tipo di carattere associato a questa parte e allo stato.                                                                                                              |
| TMT \_ GLYPHTRANSPARENTCOLOR   | Colore del glifo trasparente associato a questa parte e allo stato. Se il valore TMT GLYPHTRANSPARENT per questa parte e lo stato è TRUE, le parti del glifo che utilizzano questo colore \_ non vengono disegnate. |
| TMT \_ GRADIENTACTIVECAPTION   |                                                                                                                                                                                                |
| SFUMATURA \_ TMTCOLOR1          | Primo colore della sfumatura associata a questa parte e allo stato.                                                                                                                           |
| SFUMATURA \_ TMTCOLOR2          | Secondo colore della sfumatura.                                                                                                                                                              |
| SFUMATURA \_ TMTCOLOR3          | Terzo colore della sfumatura.                                                                                                                                                               |
| SFUMATURA \_ TMTCOLOR4          | Quarto colore della sfumatura.                                                                                                                                                              |
| SFUMATURA \_ TMTCOLOR5          | Quinto colore della sfumatura.                                                                                                                                                               |
| TMT \_ GRADIENTINACTIVECAPTION |                                                                                                                                                                                                |
| TMT \_ GRAYTEXT                |                                                                                                                                                                                                |
| TMT \_ HEADING1TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ HEADING2TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ HIGHLIGHT               |                                                                                                                                                                                                |
| TMT \_ HIGHLIGHTTEXT           |                                                                                                                                                                                                |
| TMT \_ HOTTRACKING             |                                                                                                                                                                                                |
| TMT \_ INACTIVEBORDER          |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTION         |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTIONTEXT     |                                                                                                                                                                                                |
| TMT \_ INFOBK                  |                                                                                                                                                                                                |
| TMT \_ INFOTEXT                |                                                                                                                                                                                                |
| TMT \_ LIGHT3D                 |                                                                                                                                                                                                |
| TMT \_ MENU                    |                                                                                                                                                                                                |
| BARRA DEI \_ MENU TMT                 |                                                                                                                                                                                                |
| TMT \_ MENUHILIGHT             |                                                                                                                                                                                                |
| TMT \_ MENUTEXT                |                                                                                                                                                                                                |
| BARRA DI \_ SCORRIMENTO TMT               |                                                                                                                                                                                                |
| COLORE \_ OMBREGGIATURA TMT             | Colore dell'ombreggiatura disegnata sotto il testo associato a questa parte e allo stato.                                                                                                             |
| TMT \_ TEXTBORDERCOLOR         | Colore del bordo del testo associato a questa parte e allo stato.                                                                                                                              |
| TMT \_ TEXTCOLOR               | Colore del testo associato a questa parte e allo stato.                                                                                                                                     |
| TMT \_ TEXTCOLORHINT           |                                                                                                                                                                                                |
| TMT \_ TEXTSHADOWCOLOR         | Colore dell'ombreggiatura del testo associata a questa parte e allo stato.                                                                                                                              |
| TMT \_ TRANSPARENTCOLOR        | Colore trasparente associato a questa parte e allo stato. Se il valore TMT TRANSPARENT per questa parte e lo stato è TRUE, le parti dell'elemento grafico che usano \_ questo colore non vengono disegnate.           |
| FINESTRA \_ TMT                  |                                                                                                                                                                                                |
| TMT \_ WINDOWFRAME             |                                                                                                                                                                                                |
| TMT \_ WINDOWTEXT              |                                                                                                                                                                                                |



 

**TMT \_ DISKSTREAM**



| ID              | Note |
|-----------------|-------|
| TMT \_ ATLASIMAGE |       |



 

**Enumerazione \_ TMT**



| Enumerazione         | Valori della proprietà                                                                                                                                                                                                                                            | Note                                                                                                                                                |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| BGTYPE              | BT \_ IMAGEFILE, BT \_ BORDERFILL                                                                                                                                                                                                                              | Tipo di disegno di base per questa parte.                                                                                                                |
| BORDERTYPE          | BT \_ RECT, BT \_ ROUNDRECT, ELLISSE BT \_                                                                                                                                                                                                                       | Tipo di bordo disegnato se questa parte è un riempimento con bordo.                                                                                              |
| Contentalignment    | CA \_ A SINISTRA, CA \_ AL CENTRO, CA A \_ DESTRA                                                                                                                                                                                                                            | Allineamento del testo nella didascalia associata a questa parte.                                                                                      |
| FILLTYPE            | FT \_ SOLID, FT \_ VERTGRADIENT, FT \_ HORZGRADIENT, FT \_ RADIALGRADIENT, FT \_ TILEIMAGE                                                                                                                                                                           | Tipo di forma di riempimento disegnata se questa parte è un riempimento con bordo.                                                                                          |
| GLYPHTYPE           | GT \_ NONE, GT \_ IMAGEGLYPH, GT \_ FONTGLYPH                                                                                                                                                                                                                    | Tipo di glifo disegnato su questa parte.                                                                                                                |
| GLYPHFONTSIZINGTYPE | GFST \_ NONE, GFST \_ SIZE, GFST \_ DPI                                                                                                                                                                                                                          | Tipo di metodo usato per selezionare tra glifi di dimensioni diverse.                                                                                    |
| HALIGN              | HA \_ LEFT, HA \_ CENTER, HA \_ RIGHT                                                                                                                                                                                                                            | Allineamento orizzontale se questa parte usa un'immagine di dimensioni vere.                                                                                        |
| ICONEFFECT          | ICE \_ NONE, ICE \_ GLOW, ICE \_ SHADOW, ICE \_ PULSE, ICE \_ ALPHA                                                                                                                                                                                                  | Tipo di effetto da visualizzare quando questa parte viene disegnata [**usando DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                             |
| IMAGELAYOUT         | IL \_ VERTICALE, IL \_ ORIZZONTALE                                                                                                                                                                                                                               | Tipo di allineamento utilizzato quando vengono disegnate più immagini.                                                                                           |
| IMAGESELECTTYPE     | IST \_ NONE, IST \_ SIZE, IST \_ DPI                                                                                                                                                                                                                             | Tipo di metodo usato per selezionare le immagini ridimensionate per questa parte. Vedere il valore TMT \_ IMAGEFILE1 [**di GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename). |
| OFFSETTYPE          | OT \_ TOPLEFT, OT \_ TOPRIGHT, OT \_ TOPMIDDLE, OT \_ BOTTOMLEFT, OT \_ BOTTOMRIGHT, OT \_ BOTTOMMIDDLE, OT \_ MIDDLELEFT, \_ OT \_ MIDDLERIGHT, OT LEFTOFCAPTION, OT \_ RIGHTOFCAPTION, OT \_ LEFTOFLASTBUTTON, OT \_ RIGHTOFLASTBUTTON, OT \_ ABOVELASTBUTTON, OT \_ BELOWLASTBUTTON, OT BELOWLASTBUTTON | Allineamento di questa parte nella finestra.                                                                                                            |
| SIZINGTYPE          | ST \_ TRUESIZE, ST \_ STRETCH, ST \_ TILE, ST \_ TILEHORZ, ST \_ TILEVERT, ST \_ TILECENTER                                                                                                                                                                            | Metodo utilizzato per ridimensionare un'immagine se questa parte usa un file di immagine.                                                                                    |
| TEXTSHADOWTYPE      | TST \_ NONE, TST \_ SINGLE, TST \_ CONTINUOUS                                                                                                                                                                                                                    | Tipo di effetto ombreggiatura da disegnare dietro il testo associato a questa parte.                                                                             |
| TRUESIZESCALINGTYPE | TSST \_ NONE, TSST \_ SIZE, TSST \_ DPI                                                                                                                                                                                                                          | Tipo di ridimensionamento usato se questa parte usa un'immagine di dimensioni vere.                                                                                       |
| Valign              | VA \_ TOP, VA \_ CENTER, VA \_ BOTTOM                                                                                                                                                                                                                            | Allineamento verticale se questa parte usa un'immagine di dimensioni vere.                                                                                          |



 

**NOME FILE \_ TMT**



| ID                  | Note                                                                                                                                        |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ GLYPHIMAGEFILE | Nome file per l'immagine del glifo associata a questa parte e allo stato.                                                                        |
| TMT \_ IMAGEFILE      | Nome file dell'immagine associata a questa parte e stato o nome file di base per più immagini associate a questa parte e stato. |
| TMT \_ IMAGEFILE1     | Nome file della prima immagine ridimensionata associata a questa parte e stato, per il supporto di risoluzioni diverse.                            |
| TMT \_ IMAGEFILE2     | Nome file della seconda immagine ridimensionata.                                                                                                     |
| TMT \_ IMAGEFILE3     | Nome file della terza immagine ridimensionata.                                                                                                      |
| TMT \_ IMAGEFILE4     | Nome file della quarta immagine ridimensionata.                                                                                                     |
| TMT \_ IMAGEFILE5     | Nome file della quinta immagine ridimensionata.                                                                                                      |



 

**CARATTERE \_ TMT**



| ID                    | Note                                                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------|
| TMT \_ BODYFONT         |                                                                                                      |
| TMT \_ CAPTIONFONT      |                                                                                                      |
| TMT \_ GLYPHFONT        | Tipo di carattere con cui verrà disegnato il glifo associato a questa parte, se vengono usati glifi basati sul tipo di carattere. |
| TMT \_ HEADING1FONT     |                                                                                                      |
| TMT \_ HEADING2FONT     |                                                                                                      |
| ICONA \_ TMTTITLEFONT    |                                                                                                      |
| MENU \_ TMTFONT         |                                                                                                      |
| TMT \_ MSGBOXFONT       |                                                                                                      |
| TMT \_ SMALLCAPTIONFONT |                                                                                                      |
| TMT \_ STATUSFONT       |                                                                                                      |



 

**TMT \_ INT**



| ID                       | Note                                                                                                                                                                                                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALPHALEVEL          | Valore alfa (0-255) utilizzato per [**DrawThemeIcon.**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)                                                                                                                                         |
| TMT \_ ALPHATHRESHOLD      | Valore alfa minimo (0-255) che un pixel deve essere considerato opaco.                                                                                                                                  |
| TMT \_ ANIMATIONDELAY      |                                                                                                                                                                                                                  |
| ANIMAZIONE \_ TMTDURATION   |                                                                                                                                                                                                                  |
| TMT \_ BORDERSIZE          | Spessore del bordo disegnato se questa parte usa un riempimento del bordo.                                                                                                                                               |
| SET DI \_ CARATTERI TMT             |                                                                                                                                                                                                                  |
| COLORAZIONE \_ TMTCOLOR   |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONOPACITY |                                                                                                                                                                                                                  |
| FRAME \_ TMTPERSECOND     |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE1            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE2            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE3            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE4            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE5            |                                                                                                                                                                                                                  |
| TMT \_ GLOWINTENSITY       |                                                                                                                                                                                                                  |
| TMT \_ GLYPHINDEX          | Indice dei caratteri nel tipo di carattere selezionato che verrà usato per il glifo, se la parte usa un glifo basato sul tipo di carattere.                                                                                                 |
| TMT \_ GRADIENTRATIO1      | Quantità del primo colore sfumato (TMT \_ GRADIENTCOLOR1) da usare per disegnare la parte. Questo valore può essere compreso tra 0 e 255, ma questo valore più i valori di ognuno dei valori GRADIENTRATIO devono essere aggiunti fino a 255. |
| TMT \_ GRADIENTRATIO2      | Quantità del secondo colore sfumato (TMT \_ GRADIENTCOLOR2) da usare per disegnare la parte.                                                                                                                        |
| TMT \_ GRADIENTRATIO3      | Quantità del terzo colore sfumato (TMT \_ GRADIENTCOLOR3) da usare per disegnare la parte.                                                                                                                         |
| TMT \_ GRADIENTRATIO4      | Quantità del quarto colore sfumato (TMT \_ GRADIENTCOLOR4) da usare per disegnare la parte.                                                                                                                        |
| TMT \_ GRADIENTRATIO5      | Quantità del quinto colore sfumato (TMT \_ GRADIENTCOLOR5) da usare per disegnare la parte.                                                                                                                         |
| ALTEZZA \_ TMT              | Altezza della parte.                                                                                                                                                                                          |
| TMT \_ IMAGECOUNT          | Numero di immagini di stato presenti in un file di immagine.                                                                                                                                                             |
| TMT \_ MINCOLORDEPTH       |                                                                                                                                                                                                                  |
| TMT \_ MINDPI1             | Numero minimo di punti per pollice (dpi) per cui è stato progettato il primo file di immagine.                                                                                                                                      |
| TMT \_ MINDPI2             | Valore dpi minimo per cui è stato progettato il secondo file di immagine.                                                                                                                                                     |
| TMT \_ MINDPI3             | Valore dpi minimo per cui è stato progettato il terzo file di immagine.                                                                                                                                                      |
| TMT \_ MINDPI4             | Valore dpi minimo per cui è stato progettato il quarto file di immagine.                                                                                                                                                     |
| TMT \_ MINDPI5             | Valore dpi minimo per cui è stato progettato il quinto file di immagine.                                                                                                                                                      |
| OPACITÀ \_ TMT             |                                                                                                                                                                                                                  |
| PIXEL \_ TMTPERFRAME      |                                                                                                                                                                                                                  |
| TMT \_ PROGRESSCHUNKSIZE   | Dimensioni delle forme "blocco" del controllo di stato che definiscono l'avanzamento di un'operazione.                                                                                                                 |
| TMT \_ PROGRESSSPACESIZE   | Dimensione totale di tutti i "blocchi" del controllo di stato.                                                                                                                                                          |
| TMT \_ ROUNDCORNERHEIGHT   | Arrotondamento (da 0 a 100%) degli angoli della parte.                                                                                                                                                          |
| TMT \_ ROUNDCORNERWIDTH    | Arrotondamento (da 0 a 100%) degli angoli della parte.                                                                                                                                                          |
| \_SATURAZIONE TMT          | Quantità di saturazione (0-255) da applicare a un'icona disegnata usando [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                                                                                         |
| TMT \_ TEXTBORDERSIZE      | Spessore del bordo disegnato intorno ai caratteri di testo.                                                                                                                                                        |
| TMT \_ TEXTGLOWSIZE        |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR1            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR2            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR3            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR4            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR5            |                                                                                                                                                                                                                  |
| TMT \_ TOHUE1              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE2              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE3              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE4              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE5              |                                                                                                                                                                                                                  |
| TMT \_ TRUESIZESTRETCHMARK | Percentuale delle dimensioni originali di un'immagine di dimensioni vere con cui verrà estesa l'immagine.                                                                                                                        |
| LARGHEZZA \_ TMT               | Larghezza della parte.                                                                                                                                                                                           |



 

**TMT \_ INTLIST**



| ID                       | Note |
|--------------------------|-------|
| TRANSIZIONI \_ TMTDURATIONS |       |



 

**MARGINI \_ TMT**



| ID                  | Note                                                                   |
|---------------------|-------------------------------------------------------------------------|
| TMT \_ CAPTIONMARGINS | Margini che definiscono la posizione del testo della didascalia all'interno di una parte. |
| TMT \_ CONTENTMARGINS | Margini che definiscono la posizione del contenuto all'interno di una parte.      |
| TMT \_ SIZINGMARGINS  | Margini usati per il ridimensionamento di un'immagine di dimensioni non vere.                      |



 

**POSIZIONE \_ TMT**



| ID                    | Note                                                                                                        |
|-----------------------|--------------------------------------------------------------------------------------------------------------|
| TMT \_ MINSIZE          | Dimensioni minime per cui è possibile usare il file di immagine normale prima di passare al file di immagine più piccolo successivo.   |
| TMT \_ MINSIZE1         | Dimensioni minime per cui è possibile usare il primo file di immagine di piccole dimensioni.                                            |
| TMT \_ MINSIZE2         | Dimensioni minime per cui è possibile usare il secondo file di immagine di piccole dimensioni.                                           |
| TMT \_ MINSIZE3         | Dimensioni minime per cui è possibile usare il terzo file di immagine di piccole dimensioni.                                            |
| TMT \_ MINSIZE4         | Dimensioni minime per cui è possibile usare il quarto file di immagine di piccole dimensioni.                                           |
| TMT \_ MINSIZE5         | Dimensioni minime per cui è possibile usare il quinto file di immagine di piccole dimensioni.                                            |
| TMT \_ NORMALSIZE       | Dimensioni dell'immagine normale associata a questa parte.                                                      |
| TMT \_ OFFSET           | Offset di posizione dall'allineamento per questa parte. L'allineamento è definito dal valore \_ OFFSETTYPE TMT. |
| TMT \_ TEXTSHADOWOFFSET | Offset dal testo in corrispondenza del quale vengono disegnate le ombreggiature del testo.                                                    |



 

**TMT \_ RECT**



| ID                       | Note                         |
|--------------------------|-------------------------------|
| TMT \_ ANIMATIONBUTTONRECT |                               |
| TMT \_ ATLASRECT           |                               |
| TMT \_ CUSTOMSPLITRECT     |                               |
| TMT \_ DEFAULTPANESIZE     | Dimensioni predefinite della parte. |



 

**DIMENSIONI \_ TMT**



| ID                      | Note                     |
|-------------------------|---------------------------|
| TMT \_ CAPTIONBARHEIGHT   | Altezza della barra del titolo.       |
| TMT \_ CAPTIONBARWIDTH    | Larghezza della barra del titolo.        |
| MENU \_ TMTBARHEIGHT      | Altezza della barra dei menu.          |
| TMT \_ MENUBARWIDTH       | Larghezza della barra dei menu.           |
| TMT \_ PADDEDBORDERWIDTH  | Spessore del bordo riempito.      |
| TMT \_ SCROLLBARHEIGHT    | Altezza della barra di scorrimento.        |
| TMT \_ SCROLLBARWIDTH     | Larghezza della barra di scorrimento.         |
| TMT \_ SIZINGBORDERWIDTH  | Larghezza di un bordo di ridimensionamento. |
| TMT \_ SMCAPTIONBARHEIGHT | Altezza della barra del titolo.       |
| TMT \_ SMCAPTIONBARWIDTH  | Larghezza della barra del titolo.        |



 

**STRINGA \_ TMT**



| ID                   | Note                                               |
|----------------------|-----------------------------------------------------|
| TMT \_ ALIAS           |                                                     |
| TMT \_ ATLASINPUTIMAGE |                                                     |
| AUTORE \_ TMT          |                                                     |
| TMT \_ CLASSICVALUE    |                                                     |
| COLORI \_ TMTCHEMES    |                                                     |
| SOCIETÀ \_ TMT         |                                                     |
| TMT \_ COPYRIGHT       |                                                     |
| TMT \_ CSSNAME         | Vedere [**GetThemeSysString.**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring) |
| DESCRIZIONE \_ TMT     |                                                     |
| TMT \_ DISPLAYNAME     |                                                     |
| TMT \_ LASTUPDATED     |                                                     |
| DIMENSIONI \_ TMT           |                                                     |
| TESTO \_ TMT            | Testo visualizzato dalla parte.                     |
| DESCRIZIONE COMANDO \_ TMT         |                                                     |
| TMT \_ URL             |                                                     |
| VERSIONE \_ TMT         |                                                     |
| TMT \_ XMLNAME         | Vedere [**GetThemeSysString.**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring) |
| NOME \_ TMT            |                                                     |



 

 

 
