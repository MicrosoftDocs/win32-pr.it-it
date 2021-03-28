---
description: Esegue un verbo in una raccolta di oggetti FolderItem. Questo metodo è un'estensione del metodo InvokeVerb, che consente il controllo aggiuntivo dell'operazione tramite un set di flag.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: Metodo FolderItems2. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aa9b986b5cb76f14cc950f522e1e289224c17b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977015"
---
# <a name="folderitems2invokeverbex-method"></a>FolderItems2. InvokeVerbEx, metodo

Esegue un verbo in una raccolta di oggetti [**FolderItem**](folderitem.md) . Questo metodo è un'estensione del metodo [**InvokeVerb**](folderitem-invokeverb.md) , che consente il controllo aggiuntivo dell'operazione tramite un set di flag.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vVerb* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

**Variant** con la stringa del verbo che corrisponde al comando da eseguire. Se non viene specificato alcun verbo, viene eseguito il verbo predefinito.

</dd> <dt>

*vArgs* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

**Variant** costituito da una stringa con uno o più argomenti del comando specificato da *vVerb*. Il formato di questa stringa dipende dal verbo specifico.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un verbo è una stringa utilizzata per specificare una determinata azione associata a un elemento o a una raccolta di elementi. In genere, la chiamata di un verbo avvia un'applicazione correlata. Se, ad esempio, si chiama il verbo **aperto** in un file con estensione txt, in genere il file viene aperto con un editor di testo, in genere Microsoft blocco note. Per ulteriori informazioni sui verbi, vedere [avvio di applicazioni](launch.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **InvokeVerbEx** per richiamare il verbo predefinito ("Open") su **computer locale**. L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
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

[**FolderItems2**](folderitems2-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




