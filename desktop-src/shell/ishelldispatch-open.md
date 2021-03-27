---
description: Apre la cartella specificata.
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
title: Metodo IShellDispatch. Open (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d794020313ad776c1d538dc2acb909d562d32f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753087"
---
# <a name="ishelldispatchopen-method"></a>Metodo IShellDispatch. Open

Apre la cartella specificata.

## <a name="syntax"></a>Sintassi


```JScript
IShellDispatch.Open(
  vDir
)
```


```VB

IShellDispatch.Open( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*vdir* \[ in\]
</dt> <dd>

Tipo: **Variant**

Stringa che specifica il percorso della cartella o uno dei valori [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) . Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript. In questi casi, i valori numerici devono essere usati al suo posto.

Se *vdir* è impostato su uno dei [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) e la cartella speciale non esiste, la funzione creerà la cartella.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Questo metodo non restituisce valori.

### <a name="vb"></a>VB

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il metodo [**Shell. Open**](shell-open.md) .

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **Open** in JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**Esplora**](shell-explore.md)
</dt> </dl>

 

 




