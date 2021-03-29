---
description: Esegue un verbo su un elemento della shell.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Metodo ShellFolderItem. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978159"
---
# <a name="shellfolderiteminvokeverbex-method"></a>ShellFolderItem. InvokeVerbEx, metodo

Esegue un verbo su un elemento della shell.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vVerb* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

**Variant** che contiene la stringa del verbo che corrisponde al comando da eseguire. Deve corrispondere a uno dei valori restituiti dalla proprietà [**Name**](folderitemverb-name.md) dell'elemento. Se non viene specificato alcun verbo, viene eseguito il verbo predefinito.

</dd> <dt>

*vArgs* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

**Variant** costituito da una stringa con uno o più argomenti del comando specificato da *vVerb*. Il formato di questa stringa dipende dal verbo specifico.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un verbo è una stringa utilizzata per specificare un'azione specifica supportata da un elemento. In genere, la chiamata di un verbo avvia un'applicazione correlata. Se, ad esempio, si chiama il verbo **aperto** in un file con estensione txt, in genere il file viene aperto con un editor di testo, in genere Microsoft blocco note. L'oggetto [**folderitemverbs**](folderitemverbs.md) rappresenta la raccolta di verbi associati all'elemento. Per ulteriori informazioni sui verbi, vedere [avvio di applicazioni](launch.md).

Questo metodo è simile a [**InvokeVerb**](folderitem-invokeverb.md), ma consente di specificare argomenti per il comando e per il comando stesso.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo corretto di questo metodo in JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
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

[**ShellFolderItem**](shellfolderitem-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




