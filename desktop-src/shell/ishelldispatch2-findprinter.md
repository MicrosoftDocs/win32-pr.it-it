---
description: Consente di visualizzare la finestra di dialogo Trova stampante.
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: Metodo IShellDispatch2. FindPrinter (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 81124e3f0d04244b9b81e812e090bde25971c17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226366"
---
# <a name="ishelldispatch2findprinter-method"></a>IShellDispatch2. FindPrinter, metodo

Consente di visualizzare la finestra di dialogo **Trova stampante** .

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
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

**Stringa** che contiene il nome della stampante.

</dd> <dt>

*sLocation* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Stringa** che contiene la posizione della stampante.

</dd> <dt>

*sModel* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Stringa** che contiene il modello di stampante.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il metodo [**Shell. FindPrinter**](./shell-findprinter.md) .

Se si assegnano stringhe a uno o più parametri facoltativi, questi vengono visualizzati come valori predefiniti nel controllo di modifica associato quando viene visualizzata la finestra di dialogo **Trova stampante** . L'utente può accettare o eseguire l'override di questi valori. Se non viene assegnato alcun valore a un parametro, la casella di modifica associata è vuota e l'utente deve immettere un valore.

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **FindPrinter** per visualizzare la finestra di dialogo **Trova stampante** per una particolare applicazione. L'utilizzo viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



VBScript


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
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



 

 
