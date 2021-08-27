---
description: Esegue un verbo sull'elemento.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: Metodo FolderItem.InvokeVerb (Shldisp.h)
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
ms.openlocfilehash: 1f6c45c67bd8863b6cf1169670a4d087f29e4441c48592f850a683af5ef0bc1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111791"
---
# <a name="folderiteminvokeverb-method"></a>Metodo FolderItem.InvokeVerb

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

Tipo: **Variante**

Stringa che specifica il verbo da eseguire. Deve essere uno dei valori restituiti [](folderitemverb-name.md) dalla proprietà FolderItemVerb.Name dell'elemento. Se non viene specificato alcun verbo, verrà richiamato il verbo predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Un verbo è una stringa usata per specificare una determinata azione che un elemento supporta. Chiamare un verbo equivale a selezionare un comando dal menu di scelta rapida di un elemento. In genere, la chiamata di un verbo avvia un'applicazione correlata. Ad esempio, se si richiama il verbo "open" in un file .txt, il file viene aperto con un editor di testo, in genere Microsoft Blocco note. Per [altre informazioni sui](launch.md) verbi, vedere Avvio di applicazioni.

[**L'oggetto FolderItemVerbs**](folderitemverbs.md) rappresenta la raccolta di verbi associati all'elemento. Il verbo predefinito può variare per elementi diversi, ma in genere è "aperto".

## <a name="examples"></a>Esempio

Nell'esempio seguente **viene utilizzato InvokeVerb** per richiamare il verbo predefinito ("open" in questo caso) nella Windows cartella. Viene visualizzato un utilizzo appropriato per JScript, VBScript e Visual Basic.

JScript:


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



Vbscript:


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FolderItem**](folderitem.md)
</dt> <dt>

[**Verbi**](folderitem-verbs.md)
</dt> <dt>

[**Doit**](folderitemverb-doit.md)
</dt> </dl>

 

 




