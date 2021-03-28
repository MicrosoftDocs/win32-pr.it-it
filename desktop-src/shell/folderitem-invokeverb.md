---
description: Esegue un verbo sull'elemento.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: Metodo FolderItem. InvokeVerb (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 259ff9613756940d5da8a37585dbf39fb2dc0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524481"
---
# <a name="folderiteminvokeverb-method"></a>FolderItem. InvokeVerb, metodo

Esegue un verbo sull'elemento.

## <a name="syntax"></a>Sintassi


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vVerb* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Stringa che specifica il verbo da eseguire. Deve corrispondere a uno dei valori restituiti dalla proprietà [**FolderItemVerb.Name**](folderitemverb-name.md) dell'elemento. Se non viene specificato alcun verbo, verrà richiamato il verbo predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Un verbo è una stringa utilizzata per specificare un'azione specifica supportata da un elemento. La chiamata di un verbo equivale alla selezione di un comando dal menu di scelta rapida di un elemento. In genere, la chiamata di un verbo avvia un'applicazione correlata. Se ad esempio si richiama il verbo "Open" in un file con estensione txt, il file verrà aperto con un editor di testo, in genere Microsoft Notepad. Per ulteriori informazioni sui verbi, vedere [avvio delle applicazioni](launch.md) .

L'oggetto [**folderitemverbs**](folderitemverbs.md) rappresenta la raccolta di verbi associati all'elemento. Il verbo predefinito può variare per elementi diversi, ma in genere è "aperto".

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **InvokeVerb** per richiamare il verbo predefinito (in questo caso "Open") nella cartella Windows. L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
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
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
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
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
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

[**FolderItem**](folderitem.md)
</dt> <dt>

[**Verbi**](folderitem-verbs.md)
</dt> <dt>

[**DoIt**](folderitemverb-doit.md)
</dt> </dl>

 

 




