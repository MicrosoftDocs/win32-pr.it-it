---
title: Risorsa finestra di dialogo
description: Definisce una finestra di dialogo. | Risorsa finestra di dialogo
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Menu delle risorse della finestra di dialogo e altre risorse
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321318"
---
# <a name="dialog-resource"></a>Risorsa finestra di dialogo

Definisce una finestra di dialogo. L'istruzione definisce la posizione e le dimensioni della finestra di dialogo sullo schermo nonché lo stile della finestra di dialogo.

> [!Note]  
> La **finestra di dialogo** è un ID di risorsa obsoleto. Le nuove applicazioni devono usare [**DIALOGEX**](dialogex-resource.md).

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome univoco o valore di Unsigned Integer a 16 bit univoco che identifica la finestra di dialogo.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*
</dt> <dd>

Opzioni per la finestra di dialogo. Questa operazione può essere costituita da zero o più delle istruzioni seguenti.



| Istruzione                                                        | Descrizione                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Didascalia**](caption-statement.md) "*testo*"                    | Didascalia della finestra di dialogo se dispone di una barra del titolo. Per ulteriori informazioni, vedere la [**didascalia**](caption-statement.md).                                                                             |
| [**Caratteristiche**](characteristics-statement.md) *DWORD*     | Valore **DWORD** definito dall'utente per l'utilizzo da strumenti di risorse. Questo valore non viene utilizzato dal sistema. Per ulteriori informazioni, vedere [**caratteristiche**](characteristics-statement.md).                |
| [](class-statement.md) *Classe* Class                         | Unsigned Integer a 16 bit o una stringa racchiusa tra virgolette doppie ("), che identifica la classe della finestra di dialogo. Per ulteriori informazioni, vedere la [**classe**](class-statement.md).      |
| **ExStyle =** *stili estesi*                                   | Stile finestra esteso della finestra di dialogo. Per ulteriori informazioni, vedere [**ExStyle**](exstyle-statement.md).                                                                                     |
| **Carattere** *pointsize*, carattere *tipografico*                                 | Dimensioni del punto e carattere tipografico per il tipo di carattere. Per ulteriori informazioni, vedere [**carattere**](font-statement.md).                                                                                              |
| [](language-statement.md) *Lingua* lingua, *lingua* | Lingua della finestra di dialogo. Per ulteriori informazioni, vedere [**Language**](language-statement.md).                                                                                                |
|  *Menu* menu                                              | Menu da utilizzare. Questo valore è il nome del menu o il relativo identificatore di tipo Integer.                                                                                                        |
| [](style-statement.md) *Stili* di stile                        | Stili della finestra di dialogo. Per ulteriori informazioni, vedere [**stile**](style-statement.md).                                                                                                        |
| [](version-statement.md) *DWORD* versione                     | Valore **DWORD** definito dall'utente. Questa istruzione è destinata all'utilizzo da parte di altri strumenti di risorse e non viene utilizzata dal sistema. Per ulteriori informazioni, vedere [**Version**](version-statement.md). |



 

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="remarks"></a>Commenti

La funzione [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) restituisce le unità di base della finestra di dialogo in pixel. Il significato esatto delle coordinate dipende dallo stile definito dall'istruzione di opzione [**Style**](style-statement.md) . Per le finestre di dialogo di tipo figlio, le coordinate sono relative all'origine della finestra padre, a meno che la finestra di dialogo non disponga dello stile **DS \_ ABSALIGN**; in tal caso, le coordinate sono relative all'origine della schermata di visualizzazione.

Non usare lo stile **WS \_ figlio** con una finestra di dialogo modale. La funzione [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) Disabilita sempre il padre/proprietario della finestra di dialogo appena creata. Quando una finestra padre è disabilitata, le finestre figlio vengono disabilitate in modo implicito. Poiché la finestra padre della finestra di dialogo di tipo figlio è disabilitata, la finestra di dialogo di tipo figlio è anch ' essa.

Se una finestra di dialogo ha lo stile **DS \_ ABSALIGN** , le coordinate della finestra di dialogo per l'angolo superiore sinistro sono relative all'origine dello schermo anziché all'angolo superiore sinistro della finestra padre. Questo stile viene in genere utilizzato quando si desidera che la finestra di dialogo venga avviata in una parte specifica della visualizzazione, indipendentemente dalla posizione in cui è possibile che la finestra padre si trovi sullo schermo.

La finestra di **dialogo** nome può essere usata anche come parametro Class-Name per la funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per creare una finestra con gli attributi della finestra di dialogo.

## <a name="examples"></a>Esempio

Di seguito viene illustrato l'utilizzo dell'istruzione della **finestra di dialogo** :

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

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

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 
