---
description: Cerca la destinazione di un collegamento shell, anche se la destinazione è stata spostata o rinominata.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: Metodo ShellLinkObject.Resolve (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fdff3fd1a606b8dbec35476988497dd14892692a42e6502343716264873c184d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857494"
---
# <a name="shelllinkobjectresolve-method"></a>Metodo ShellLinkObject.Resolve

Cerca la destinazione di un collegamento shell, anche se la destinazione è stata spostata o rinominata.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fFlags* \[ Pollici\]
</dt> <dd>

Tipo: **Integer**

Flag che specificano l'azione da eseguire. Può trattarsi di una combinazione dei valori seguenti:

<dt>



 (1)


</dt> <dd>

Non visualizzare una finestra di dialogo se il collegamento non può essere risolto. Quando questo flag è impostato, la parola di ordine superiore *di fFlags* specifica una durata del timeout, in millisecondi. Il metodo restituisce se il collegamento non può essere risolto entro la durata del timeout. Se la parola più importante è impostata su zero, la durata del timeout viene impostata su 3000 millisecondi (3 secondi).

</dd> <dt>



 (4)


</dt> <dd>

Se il collegamento è stato modificato, aggiornarne il percorso e l'elenco di identificatori.

</dd> <dt>



 (8)


</dt> <dd>

Non aggiornare le informazioni sul collegamento.

</dd> <dt>



 (16)


</dt> <dd>

Non eseguire l'euristica di ricerca.

</dd> <dt>



 (32)


</dt> <dd>

Non usare il rilevamento dei collegamenti distribuiti.

</dd> <dt>



 (64)


</dt> <dd>

Disabilitare il rilevamento dei collegamenti distribuiti. Per impostazione predefinita, il rilevamento dei collegamenti distribuiti tiene traccia dei supporti rimovibili tra più dispositivi in base al nome del volume. Usa anche il percorso UNC per tenere traccia dei file system remoti la cui lettera di unità è stata modificata. L'impostazione di questo flag disabilita entrambi i tipi di rilevamento.

</dd> <dt>



 (128)


</dt> <dd>

Chiamare il programma Windows di installazione.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo è essenzialmente identico nella funzionalità di [**Resolve.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) Per altre informazioni sulla risoluzione dei collegamenti, vedere la sezione Osservazioni di tale pagina.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.Resolve(1)
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellLinkObjectResolveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional solo con app desktop SP3 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
