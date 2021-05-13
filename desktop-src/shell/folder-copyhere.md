---
description: Copia uno o più elementi in una cartella.
title: Metodo Folder.CopyHere (Shldisp.h)
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
ms.openlocfilehash: 1466e5d01715c0c820cbc7cd9809c51e4963ec56
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842142"
---
# <a name="foldercopyhere-method"></a>Metodo Folder.CopyHere

Copia uno o più elementi in una cartella.

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

Elemento o elementi da copiare. Può trattarsi di una stringa che rappresenta un nome file, un [**oggetto FolderItem**](folderitem.md) o [**un oggetto FolderItems.**](folderitems.md)

</dd> <dt>

*vOptions* \[ Opzionale\]
</dt> <dd>

Tipo: **Variant**

Opzioni per l'operazione di copia. Questo valore può essere zero o una combinazione dei valori seguenti. Questi valori sono basati sui flag definiti per l'uso con il membro **fFlags** della struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) di C++. Ogni spazio dei nomi della shell deve fornire la propria implementazione di questi flag e ogni spazio dei nomi può scegliere di ignorare alcuni o anche tutti questi flag. Questi flag non sono definiti in base al nome per Visual Basic, VBScript o JScript, pertanto è necessario definirli manualmente o usare i relativi equivalenti numerici.

> [!Note]  
> In alcuni casi, ad esempio i file compressi (zip), alcuni flag di opzione possono essere ignorati per impostazione predefinita.

 

<dt>



 (4)


</dt> <dd>

Non visualizzare una finestra di dialogo di stato.

</dd> <dt>



 (8)


</dt> <dd>

Assegnare al file utilizzato un nuovo nome in un'operazione di spostamento, copia o ridenominazione se esiste già un file con il nome di destinazione.

</dd> <dt>



 (16)


</dt> <dd>

Rispondere con "Sì a tutti" per qualsiasi finestra di dialogo visualizzata.

</dd> <dt>



 (64)


</dt> <dd>

Se possibile, mantenere le informazioni di annullamento.

</dd> <dt>



 (128)


</dt> <dd>

Eseguire l'operazione sui file solo se è specificato un nome file con caratteri jolly ( \* . \* ).

</dd> <dt>



 (256)


</dt> <dd>

Visualizzare una finestra di dialogo di stato ma non visualizzare i nomi dei file.

</dd> <dt>



 (512)


</dt> <dd>

Non confermare la creazione di una nuova directory se l'operazione ne richiede la creazione.

</dd> <dt>



 (1024)


</dt> <dd>

Non visualizzare un'interfaccia utente se si verifica un errore.

</dd> <dt>



 (2048)


</dt> <dd>

[Versione 4.71.](versions.md) Non copiare gli attributi di sicurezza del file.

</dd> <dt>



 (4096)


</dt> <dd>

Operare solo nella directory locale. Non operare in modo ricorsivo nelle sottodirectory.

</dd> <dt>



 (8192)


</dt> <dd>

[Versione 5.0.](versions.md) Non copiare i file connessi come gruppo. Copiare solo i file specificati.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Non viene inviata alcuna notifica al programma chiamante per indicare che la copia è stata completata.

> [!Note]  
> Non tutti i metodi vengono implementati per tutte le cartelle. Ad esempio, il [**metodo ParseName**](folder-parsename.md) non è implementato per la cartella Pannello di controllo (CSIDL \_ CONTROLS). Se si tenta di chiamare un metodo non implementato, viene generato 0x800A01BD errore di tipo decimale 445.

 

## <a name="examples"></a>Esempio

L'esempio seguente **usa CopyHere** per copiare il file Autoexec.bat dalla directory radice alla directory C: \\ Windows. Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.

Jscript:


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



Vbscript:


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
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Cartella**](folder.md)
</dt> </dl>

 

 




