---
description: Sposta un elemento o elementi in questa cartella.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Metodo Folder. MoveHere (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749178"
---
# <a name="foldermovehere-method"></a>Folder. MoveHere, metodo

Sposta un elemento o elementi in questa cartella.

## <a name="syntax"></a>Sintassi


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vite* \[ in\]
</dt> <dd>

Tipo: **Variant**

Elemento o elementi da spostare. Può trattarsi di una stringa che rappresenta un nome file, un oggetto [**FolderItem**](folderitem.md) o un oggetto [**FolderItems**](folderitems.md) .

</dd> <dt>

*vOptions* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Opzioni per l'operazione di spostamento. Questo valore può essere zero o una combinazione dei valori seguenti. Questi valori sono basati su flag definiti per l'uso con il membro **fFlags** della struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) di C++. Questi flag non sono definiti come tali per Visual Basic, VBScript o JScript, quindi è necessario definirli autonomamente o utilizzarne gli equivalenti numerici.

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



 (9182)


</dt> <dd>

[Versione 5,0.](versions.md) Non spostare i file connessi come gruppo. Spostare solo i file specificati.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

> [!Note]  
> Non tutti i metodi sono implementati per tutte le cartelle. Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL). Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **MoveHere** per spostare il file Temp.txt dalla directory radice dell'unità c alla cartella c: \\ Windows. L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
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



 

 




