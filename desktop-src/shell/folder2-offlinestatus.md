---
description: Contiene lo stato offline della cartella.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Proprietà Cartella2. OfflineStatus (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977071"
---
# <a name="folder2offlinestatus-property"></a>Proprietà Cartella2. OfflineStatus

Contiene lo stato offline della cartella.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a>Valore proprietà

**Intero** impostato su uno dei valori seguenti.

<dt>



 (OFS \_ DIRTYCACHE)


</dt> <dd>

Il server è online con modifiche non sincronizzate.

</dd> <dt>



 (OFS \_ INATTIVO


</dt> <dd>

La memorizzazione nella cache offline non è abilitata per questa cartella.

</dd> <dt>



 (OFS \_ OFFLINE


</dt> <dd>

Il server è offline.

</dd> <dt>



 (OFS \_ ONLINE


</dt> <dd>

Il server è online.

</dd> <dt>



 (OFS \_ SERVERBACK)


</dt> <dd>

Il server è offline, ma è possibile raggiungerlo.

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> Per il corretto funzionamento di **OfflineStatus** , è necessario abilitare la file offline tramite Opzioni cartella. Se l'opzione File offline non è abilitata, la proprietà restituisce **OFS \_ inactive**.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'uso corretto di **OfflineStatus** per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Cartella2**](folder2-object.md)
</dt> <dt>

[**Cartella**](folder.md)
</dt> </dl>

 

 




