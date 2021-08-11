---
title: Risorsa DIALOGEX
description: Definisce una finestra di dialogo. | Risorsa DIALOGEX
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Menu delle risorse DIALOGEX e altre risorse
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e999d4f42477451fef25bd59fb95606624cc4fd60d340231b3ee95558834d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235310"
---
# <a name="dialogex-resource"></a>Risorsa DIALOGEX

Definisce una finestra di dialogo. L'istruzione definisce la posizione e le dimensioni della finestra di dialogo sullo schermo, nonché lo stile della finestra di dialogo. Definisce anche quanto segue:

-   ID della Guida nella finestra di dialogo stessa e nei controlli all'interno della finestra di dialogo.
-   Uso [**dell'istruzione EXSTYLE**](exstyle-statement.md) per la finestra di dialogo stessa e per i controlli all'interno della finestra di dialogo.
-   Impostazioni relative a spessore del carattere e corsivo per il tipo di carattere da utilizzare nella finestra di dialogo.
-   Dati specifici del controllo per i controlli all'interno della finestra di dialogo.
-   Uso dei nomi di classe di sistema predefiniti **BEDIT,** **IEDIT** e **HEDIT.**

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*Nameid*
</dt> <dd>

Nome univoco o valore unsigned integer a 16 bit univoco che identifica la finestra di dialogo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Posizione nella schermata del lato sinistro della finestra di dialogo, in unità di finestra di dialogo.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Posizione nella schermata superiore della finestra di dialogo, in unità di finestra di dialogo.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Larghezza*
</dt> <dd>

Larghezza della finestra di dialogo, in unità di finestra di dialogo.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Altezza*
</dt> <dd>

Altezza della finestra di dialogo, in unità di finestra di dialogo.

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*HELPID*
</dt> <dd>

Espressione numerica che indica l'ID usato per identificare la finestra di dialogo durante [**l'elaborazione della \_ Guida WM.**](../shell/wm-help.md)

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*istruzioni facoltative*
</dt> <dd>

Opzioni per la finestra di dialogo. Può trattarsi di zero o più delle istruzioni seguenti.



| Istruzione                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DIDASCALIA** "*text*"                                              | Didascalia della finestra di dialogo se dispone di una barra del titolo. Per altre informazioni, vedere [**Istruzione CAPTION.**](caption-statement.md)                                                                                                                                                                                                                                                                                                                                                            |
| **CHARACTERISTICS** *dword*                                       | Valore DWORD definito **dall'utente** per l'uso da parte degli strumenti delle risorse. Questo valore non viene utilizzato dal sistema. Per altre informazioni, vedere [**Istruzione CHARACTERISTICS.**](characteristics-statement.md)                                                                                                                                                                                                                                                                                               |
| **Classe**_CLASS_                                                  | Intero senza segno a 16 bit o stringa, racchiusa tra virgolette doppie ("), che identifica la classe della finestra di dialogo. Per altre informazioni, vedere [**Istruzione CLASS.**](class-statement.md)                                                                                                                                                                                                                                                                                     |
| **EXSTYLE** =  *stili estesi*                                    | Stile esteso della finestra di dialogo. Per altre informazioni, vedere [**Istruzione EXSTYLE.**](exstyle-statement.md)                                                                                                                                                                                                                                                                                                                                                                    |
| **FONT** *punta a*, " carattere *tipografico*", *spessore*, *corsivo*, *charset* | Dimensione del punto e carattere tipografico per il tipo di carattere. Per *peso,* usare i valori **FW \_ \** _ definiti in WinGDI.h. Per _italic*, specificare TRUE per usare un carattere corsivo, FALSE in caso contrario. Per *charset*, usare il valore definito nel membro **lfCharSet** della [**struttura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta) Per ottenere il tipo di carattere definitivo per una finestra di dialogo, un'applicazione deve specificare *un set di* caratteri insieme ad altre proprietà del tipo di carattere. Per altre informazioni, vedere [**Istruzione FONT**](font-statement.md). |
| **LANGUAGE** *language*, *sottolinguaggio*                            | Lingua della finestra di dialogo. Per altre informazioni, vedere [**Language Statement**](language-statement.md).                                                                                                                                                                                                                                                                                                                                                                               |
| **MENU** *menuname*                                               | Menu da usare. Questo valore è il nome del menu o il relativo identificatore integer. Per altre informazioni, vedere [**Istruzione MENU.**](menu-statement.md)                                                                                                                                                                                                                                                                                                                             |
| **Stili DI** *STILE*                                                | Stili della finestra di dialogo. Per altre informazioni, vedere [**Istruzione STYLE.**](style-statement.md)                                                                                                                                                                                                                                                                                                                                                                                       |
| **VERSION** *dword*                                               | Valore **DWORD definito dall'utente.** Questa istruzione è destinata all'uso da parte di strumenti aggiuntivi per le risorse e non viene usata dal sistema. Per altre informazioni, vedere [**Istruzione VERSION.**](version-statement.md)                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*istruzioni di controllo*
</dt> <dd>

Il corpo della **risorsa DIALOGEX** è costituito da un numero qualsiasi di istruzioni di controllo. Sono disponibili quattro famiglie di istruzioni di controllo: generica, statica, pulsante e modifica. Per altre informazioni, vedere la sezione Osservazioni.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse.](common-resource-attributes.md)

## <a name="remarks"></a>Commenti

Le operazioni valide che possono essere contenute in una qualsiasi delle espressioni numeriche nelle istruzioni di **DIALOGEX** sono le seguenti:

-   Aggiungi ('+')
-   Sottrazione ('-')
-   Unry minus ('-')
-   NOT uniri ('~')
-   AND ('&')
-   OR (' \| ')

Il corpo della risorsa è costituito da istruzioni generiche, statiche, pulsanti e controlli di modifica. Sebbene ognuna di queste famiglie di istruzioni usi una sintassi diversa per la definizione di funzionalità specifiche dei relativi controlli, condividono tutte una sintassi comune per la definizione di posizione, dimensioni, stili estesi, numero di identificazione della Guida e dati specifici del controllo. Per altre informazioni, vedere [Parametri di controllo comuni.](common-control-parameters.md)

### <a name="generic-control-statements"></a>Istruzioni di controllo generiche

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Testo della finestra per il controllo. Per altre informazioni, vedere [Parametri di controllo comuni.](common-control-parameters.md)

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificatore del controllo. Per altre informazioni, vedere [Parametri di controllo comuni.](common-control-parameters.md)

</dd> <dt>

<span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*Classname*
</dt> <dd>

Nome della classe. Può trattarsi di una stringa racchiusa tra virgolette doppie (") o di una delle classi di sistema predefinite **seguenti: BUTTON**, **STATIC**, **EDIT**, **LISTBOX**, **SCROLLBAR** o **COMBOBOX**.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili di finestra (I valori di stile **WS \_ \* *_, _* \_ \* BS *_, _* \_ \* SS *_, _* ES \_ \* *_, _* LBS \_ \* *_, _* \_ \* SBS *_, e _* CBS \_ \*** definiti in Winuser.H possono essere usati aggiungendo un'inclusione al file RC: `#include "winuser.h"` ). Per altre informazioni, vedere [Stili delle finestre.](/windows/desktop/winmsg/window-styles)

</dd> </dl>

### <a name="static-control-statements"></a>Istruzioni di controllo statico

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*
</dt> <dd>

**LTEXT,** **RTEXT** o **CTEXT.**

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Testo della finestra per il controllo. Per altre informazioni, vedere [Parametri di controllo comuni.](common-control-parameters.md)

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificatore del controllo. Per altre informazioni, vedere [Parametri di controllo comuni.](common-control-parameters.md)

</dd> </dl>

### <a name="button-control-statements"></a>Istruzioni di controllo Button

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*Classe button*
</dt> <dd>

**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CHECKBOX**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3** O **USERBUTTON**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Testo della finestra per il controllo. Per altre informazioni, vedere [Parametri di controllo comuni.](common-control-parameters.md)

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificatore del controllo. Per altre informazioni, vedere [Parametri di controllo comuni.](common-control-parameters.md)

</dd> </dl>

### <a name="edit-control-statements"></a>Modificare istruzioni di controllo

``` syntax
editClass id
```

<dl> <dt>

<span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*
</dt> <dd>

**EDITTEXT,** **BEDIT,** **HEDIT** o **IEDIT.**

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificatore del controllo. Per altre informazioni, vedere [Parametri di controllo comuni.](common-control-parameters.md)

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle finestre di dialogo](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**Acceleratori**](accelerators-resource.md)
</dt> <dt>

[**Caratteristiche**](characteristics-statement.md)
</dt> <dt>

[**Controllo**](control-control.md)
</dt> <dt>

[**Finestra di dialogo CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**Createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Finestra di dialogo**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**Lingua**](language-statement.md)
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[Menu](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 
