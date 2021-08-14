---
description: Sposta uno o più elementi in questa cartella.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Metodo Folder.MoveHere (Shldisp.h)
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
ms.openlocfilehash: eb826d23a168d81d838341e96fa5e613f8b6f5261a3cda548a2be320acebbde8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458919"
---
# <a name="foldermovehere-method"></a>Metodo Folder.MoveHere

Sposta uno o più elementi in questa cartella.

## <a name="syntax"></a>Sintassi


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vItem* \[ Pollici\]
</dt> <dd>

Tipo: **Variante**

Elemento o elementi da spostare. Può trattarsi di una stringa che rappresenta un nome file, un [**oggetto FolderItem**](folderitem.md) o [**un oggetto FolderItems.**](folderitems.md)

</dd> <dt>

*vOptions* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

Opzioni per l'operazione di spostamento. Questo valore può essere zero o una combinazione dei valori seguenti. Questi valori sono basati sui flag definiti per l'uso con il membro **fFlags** della struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) di C++. Questi flag non sono definiti come tali per Visual Basic, VBScript o JScript, pertanto è necessario definirli manualmente o usare i relativi equivalenti numerici.

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

Eseguire l'operazione sui file solo se è specificato un nome di file con caratteri jolly ( \* . \* ).

</dd> <dt>



 (256)


</dt> <dd>

Consente di visualizzare una finestra di dialogo di stato senza visualizzare i nomi dei file.

</dd> <dt>



 (512)


</dt> <dd>

Non confermare la creazione di una nuova directory se l'operazione ne richiede una.

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



 (9182)


</dt> <dd>

[Versione 5.0.](versions.md) Non spostare i file connessi come gruppo. Spostare solo i file specificati.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

> [!Note]  
> Non tutti i metodi vengono implementati per tutte le cartelle. Ad esempio, il [**metodo ParseName**](folder-parsename.md) non è implementato per la cartella Pannello di controllo (CSIDL \_ CONTROLS). Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).

 

## <a name="examples"></a>Esempio

L'esempio seguente **usa MoveHere** per spostare il file Temp.txt dalla directory radice dell'unità C alla cartella C: \\ Windows. Viene visualizzato l'utilizzo corretto JScript, VBScript e Visual Basic.

JScript:


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



Vbscript:


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




