---
description: 'Metodo IShellDispatch2.FindPrinter: visualizza la finestra di dialogo Trova stampante.'
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: Metodo IShellDispatch2.FindPrinter (Shldisp.h)
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
ms.openlocfilehash: 64a3975039255de76b3e59432b0848cc2cb1795b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117119"
---
# <a name="ishelldispatch2findprinter-method"></a>Metodo IShellDispatch2.FindPrinter

Visualizza la **finestra di dialogo Trova** stampante.

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

Valore **String** contenente il nome della stampante.

</dd> <dt>

*sLocation* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** che contiene il percorso della stampante.

</dd> <dt>

*sModel* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** che contiene il modello di stampante.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.FindPrinter.**](./shell-findprinter.md)

Se si assegnano stringhe a uno o più parametri facoltativi, vengono visualizzate  come valori predefiniti nel controllo di modifica associato quando viene visualizzata la finestra di dialogo Trova stampante . L'utente può accettare o eseguire l'override di questi valori. Se a un parametro non viene assegnato alcun valore, la casella di modifica associata è vuota e l'utente deve immettere un valore.

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'uso di **FindPrinter** per visualizzare la **finestra di** dialogo Trova stampante per una determinata applicazione. L'utilizzo è illustrato per JScript, VBScript e Visual Basic.

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
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
