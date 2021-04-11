---
title: Risorsa DIALOGEX
description: Definisce una finestra di dialogo. | Risorsa DIALOGEX
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Menu risorse DIALOGEX e altre risorse
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234814"
---
# <a name="dialogex-resource"></a>Risorsa DIALOGEX

Definisce una finestra di dialogo. L'istruzione definisce la posizione e le dimensioni della finestra di dialogo sullo schermo nonché lo stile della finestra di dialogo. Definisce inoltre quanto segue:

-   ID della guida nella finestra di dialogo e nei controlli all'interno della finestra di dialogo.
-   Utilizzare l'istruzione [**ExStyle**](exstyle-statement.md) per la finestra di dialogo e i controlli all'interno della finestra di dialogo.
-   Spessore del carattere e impostazioni italiche per il tipo di carattere da utilizzare nella finestra di dialogo.
-   Dati specifici del controllo per i controlli all'interno della finestra di dialogo.
-   Uso dei nomi di classe di sistema predefiniti **BEdit**, **IEDIT** e **hedit** .

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome univoco o valore di Unsigned Integer a 16 bit univoco che identifica la finestra di dialogo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Posizione sulla schermata del lato sinistro della finestra di dialogo, in unità di dialogo.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Posizione sullo schermo della parte superiore della finestra di dialogo, in unità di dialogo.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Larghezza*
</dt> <dd>

Larghezza della finestra di dialogo, in unità di dialogo.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*altezza*
</dt> <dd>

Altezza della finestra di dialogo, in unità di dialogo.

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Espressione numerica che indica l'ID utilizzato per identificare la finestra di dialogo durante l'elaborazione della [**\_ Guida di WM**](../shell/wm-help.md) .

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*
</dt> <dd>

Opzioni per la finestra di dialogo. Questa operazione può essere costituita da zero o più delle istruzioni seguenti.



| Istruzione                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Didascalia** "*testo*"                                              | Didascalia della finestra di dialogo se dispone di una barra del titolo. Per ulteriori informazioni, vedere l' [**istruzione Caption**](caption-statement.md).                                                                                                                                                                                                                                                                                                                                                            |
| **Caratteristiche** *DWORD*                                       | Valore **DWORD** definito dall'utente per l'utilizzo da strumenti di risorse. Questo valore non viene utilizzato dal sistema. Per altre informazioni, vedere [**dichiarazione di caratteristiche**](characteristics-statement.md).                                                                                                                                                                                                                                                                                               |
| _Classe_ Class                                                  | Unsigned Integer a 16 bit o una stringa racchiusa tra virgolette doppie ("), che identifica la classe della finestra di dialogo. Per ulteriori informazioni, vedere [**istruzione Class**](class-statement.md).                                                                                                                                                                                                                                                                                     |
| **ExStyle** =  *stili estesi*                                    | Stile finestra esteso della finestra di dialogo. Per ulteriori informazioni, vedere l' [**istruzione EXSTYLE**](exstyle-statement.md).                                                                                                                                                                                                                                                                                                                                                                    |
| **Font** *pointsize*, "*Typeface*", *Weight*, *Italic*, *CharSet* | Dimensioni del punto e carattere tipografico per il tipo di carattere. Per *Weight*, usare i valori ** \_ \* FW* _ definiti in wingdi. h. Per _italic *, specificare TRUE per usare un tipo di carattere corsivo; in caso contrario, FALSE. Per *CharSet*, usare il valore definito nel membro **LfCharSet** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Per ottenere il tipo di carattere definitivo per una finestra di dialogo, un'applicazione deve specificare *CharSet* insieme ad altre proprietà del tipo di carattere. Per altre informazioni, vedere [**istruzione font**](font-statement.md). |
|  *Lingua* lingua, *lingua*                            | Lingua della finestra di dialogo. Per ulteriori informazioni, vedere [**istruzione language**](language-statement.md).                                                                                                                                                                                                                                                                                                                                                                               |
|  *Menu* menu                                               | Menu da utilizzare. Questo valore è il nome del menu o il relativo identificatore di tipo Integer. Per ulteriori informazioni, vedere [**istruzione di menu**](menu-statement.md).                                                                                                                                                                                                                                                                                                                             |
|  *Stili* di stile                                                | Stili della finestra di dialogo. Per ulteriori informazioni, vedere [**istruzione Style**](style-statement.md).                                                                                                                                                                                                                                                                                                                                                                                       |
|  *DWORD* versione                                               | Valore **DWORD** definito dall'utente. Questa istruzione è destinata all'utilizzo da parte di altri strumenti di risorse e non viene utilizzata dal sistema. Per ulteriori informazioni, vedere [**istruzione version**](version-statement.md).                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*istruzioni di controllo*
</dt> <dd>

Il corpo della risorsa **DIALOGEX** è costituito da un numero qualsiasi di istruzioni di controllo. Sono disponibili quattro famiglie di istruzioni di controllo: generico, statico, pulsante e modifica. Per altre informazioni, vedere la sezione Osservazioni.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="remarks"></a>Commenti

Le operazioni valide che possono essere contenute in qualsiasi espressione numerica nelle istruzioni di **DIALOGEX** sono le seguenti:

-   Aggiungi (' +')
-   Subtract ('-')
-   Meno unario ('-')
-   NOT unario (' ~')
-   E (' &')
-   O (' \| ')

Il corpo della risorsa è costituito da istruzioni generiche, statiche, di controllo Button e di modifica. Sebbene ognuna di queste famiglie di istruzioni usi una sintassi diversa per la definizione di funzionalità specifiche dei controlli, tutti condividono una sintassi comune per definire la posizione, le dimensioni, gli stili estesi, il numero di identificazione della guida e i dati specifici del controllo. Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).

### <a name="generic-control-statements"></a>Istruzioni di controllo generico

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Testo della finestra per il controllo. Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*ID*
</dt> <dd>

Identificatore del controllo. Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).

</dd> <dt>

<span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*
</dt> <dd>

Nome della classe. Può trattarsi di una stringa racchiusa tra virgolette doppie (") o di una delle classi di sistema predefinite seguenti: **Button**, **static**, **Edit**, **ListBox**, **ScrollBar** o **ComboBox**.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Gli stili della finestra (esplicito **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* es \_ \* *_, _* lbs \_ \* *_, _* SBS \_ \* *_ e _* \_ \*** i valori di stile CBS definiti in winuser. H possono essere usati aggiungendo un'inclusione al file RC: `#include "winuser.h"` ). Per altre informazioni, vedere [stili di finestra](/windows/desktop/winmsg/window-styles).

</dd> </dl>

### <a name="static-control-statements"></a>Istruzioni di controllo statico

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*
</dt> <dd>

**LTEXT**, **RTEXT** o **CTEXT**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Testo della finestra per il controllo. Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*ID*
</dt> <dd>

Identificatore del controllo. Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).

</dd> </dl>

### <a name="button-control-statements"></a>Istruzioni di controllo Button

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*
</dt> <dd>

**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CheckBox**, **PUSHBOX**, **pulsante**, **RadioButton**, **STATE3** o **UserButton**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Testo della finestra per il controllo. Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*ID*
</dt> <dd>

Identificatore del controllo. Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).

</dd> </dl>

### <a name="edit-control-statements"></a>Modificare le istruzioni di controllo

``` syntax
editClass id
```

<dl> <dt>

<span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*
</dt> <dd>

**EDITTEXT**, **BEdit**, **hedit** o **IEDIT**.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*ID*
</dt> <dd>

Identificatore del controllo. Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilizzo delle finestre di dialogo](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**ACCELERATORI**](accelerators-resource.md)
</dt> <dt>

[**CARATTERISTICHE**](characteristics-statement.md)
</dt> <dt>

[**CONTROLLO**](control-control.md)
</dt> <dt>

[**CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**LINGUAGGIO**](language-statement.md)
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[MENU](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 
