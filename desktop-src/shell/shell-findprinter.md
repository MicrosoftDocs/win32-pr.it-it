---
description: 'Metodo Shell.FindPrinter : visualizza la finestra di dialogo Trova stampante.'
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Metodo Shell.FindPrinter (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 17d04b60de2b52ca3d2f17fbdccf7de93ac095b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104309"
---
# <a name="shellfindprinter-method"></a>Metodo Shell.FindPrinter

Consente di visualizzare **la finestra di dialogo** Trova stampante .

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*sName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** contenente il nome della stampante.

</dd> <dt>

*sLocation* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** contenente il percorso della stampante.

</dd> <dt>

*sModel* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** contenente il modello della stampante.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si assegnano stringhe a uno o più parametri facoltativi, queste vengono  visualizzate come valori predefiniti nel controllo di modifica associato quando viene visualizzata la finestra di dialogo Trova stampante . L'utente può accettare o eseguire l'override di questi valori. Se a un parametro non viene assegnato alcun valore, la casella di modifica associata è vuota e l'utente deve immettere un valore.

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **FindPrinter** per visualizzare la **finestra di** dialogo Trova stampante per una determinata applicazione. L'utilizzo viene visualizzato per JScript, VBScript e Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop windows 2000 Professional e Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
