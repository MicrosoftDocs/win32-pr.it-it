---
description: Copia un elemento o elementi in una cartella.
title: Metodo Folder. CopyHere (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: ac616aa88cfb0ad6742c6037ec28e8b93ff1a4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994736"
---
# <a name="foldercopyhere-method"></a>Folder. CopyHere, metodo

Copia un elemento o elementi in una cartella.

## <a name="syntax"></a>Sintassi


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vItem* 
</dt> <dd>

Tipo: **Variant**

Elemento o elementi da copiare. Può trattarsi di una stringa che rappresenta un nome file, un oggetto [**FolderItem**](folderitem.md) o un oggetto [**FolderItems**](folderitems.md) .

</dd> <dt>

*vOptions* \[ opzionale\]
</dt> <dd>

Tipo: **Variant**

Opzioni per l'operazione di copia. Questo valore può essere zero o una combinazione dei valori seguenti. Questi valori sono basati su flag definiti per l'uso con il membro **fFlags** della struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) di C++. Ogni spazio dei nomi della shell deve fornire la propria implementazione di questi flag e ogni spazio dei nomi può scegliere di ignorare alcuni o anche tutti questi flag. Questi flag non sono definiti per nome per Visual Basic, VBScript o JScript, quindi è necessario definirli autonomamente o utilizzarne gli equivalenti numerici.

> [!Note]  
> In alcuni casi, ad esempio file compressi (zip), alcuni flag di opzione possono essere ignorati dalla progettazione.

 

<dt>



 (4)


</dt> <dd>

Non visualizzare una finestra di dialogo di stato.

</dd> <dt>



 (8)


</dt> <dd>

Assegnare al file un nuovo nome in un'operazione di spostamento, copia o ridenominazione se esiste già un file con il nome di destinazione.

</dd> <dt>



 (16)


</dt> <dd>

Rispondere con "Sì a tutti" per qualsiasi finestra di dialogo visualizzata.

</dd> <dt>



 (64)


</dt> <dd>

Mantenere le informazioni di annullamento, se possibile.

</dd> <dt>



 (128)


</dt> <dd>

Eseguire l'operazione sui file solo se viene specificato un nome file con caratteri jolly ( \* . \* ).

</dd> <dt>



 (256)


</dt> <dd>

Visualizza una finestra di dialogo di stato ma non Mostra i nomi dei file.

</dd> <dt>



 (512)


</dt> <dd>

Non confermare la creazione di una nuova directory se l'operazione ne richiede la creazione.

</dd> <dt>



 (1024)


</dt> <dd>

Se si verifica un errore, non visualizzare un'interfaccia utente.

</dd> <dt>



 (2048)


</dt> <dd>

[Versione 4,71.](versions.md) Non copiare gli attributi di sicurezza del file.

</dd> <dt>



 (4096)


</dt> <dd>

Utilizzare solo nella directory locale. Non funzionano in modo ricorsivo nelle sottodirectory.

</dd> <dt>



 (8192)


</dt> <dd>

[Versione 5,0.](versions.md) Non copiare i file connessi come gruppo. Copiare solo i file specificati.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Non viene fornita alcuna notifica al programma chiamante per indicare che la copia è stata completata.

> [!Note]  
> Non tutti i metodi sono implementati per tutte le cartelle. Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL). Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **CopyHere** per copiare il file di Autoexec.bat dalla directory radice alla directory C: \\ Windows. L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



VBScript


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
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

[**Cartella**](folder.md)
</dt> </dl>

 

 




