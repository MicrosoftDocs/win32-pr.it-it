---
description: Contiene lo stato offline della cartella.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Proprietà Folder2.OfflineStatus (Shldisp.h)
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
ms.openlocfilehash: a2664a99fb103b41bd3b5040b3876b0cb92b8f9c010f420f93af7eb62a6f32bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860248"
---
# <a name="folder2offlinestatus-property"></a>Folder2.OfflineStatus - proprietà

Contiene lo stato offline della cartella.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a>Valore proprietà

Intero **impostato** su uno dei valori seguenti.

<dt>



 (OFS \_ DIRTYCACHE)


</dt> <dd>

Il server è online con modifiche non sincronizzate.

</dd> <dt>



 (OFS \_ INATTIVO)


</dt> <dd>

La memorizzazione nella cache offline non è abilitata per questa cartella.

</dd> <dt>



 (OFS \_ OFFLINE)


</dt> <dd>

Il server è offline.

</dd> <dt>



 (OFS \_ ONLINE)


</dt> <dd>

Il server è online.

</dd> <dt>



 (OFS \_ SERVERBACK)


</dt> <dd>

Il server è offline, ma può essere raggiunto.

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> File offline essere abilitato tramite Opzioni cartella per il corretto funzionamento **di OfflineStatus.** Se l File offline'opzione non è abilitata, la proprietà restituisce **OFS \_ INACTIVE**.

 

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso corretto di **OfflineStatus** per JScript, VBScript e Visual Basic.

JScript:


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



Vbscript:


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Cartella2**](folder2-object.md)
</dt> <dt>

[**Cartella**](folder.md)
</dt> </dl>

 

 




