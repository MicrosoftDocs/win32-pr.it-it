---
description: Recupera i dettagli relativi a un elemento in una cartella. Ad esempio, le dimensioni, il tipo o l'ora dell'Ultima modifica.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Metodo Folder. GetDetailsOf (Shlobj \_ Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ab89f00f254778a2417644d894f1e9e81eb43cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966395"
---
# <a name="foldergetdetailsof-method"></a>Folder. GetDetailsOf, metodo

Recupera i dettagli relativi a un elemento in una cartella. Ad esempio, le dimensioni, il tipo o l'ora dell'Ultima modifica.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vItem* 
</dt> <dd>

Tipo: **Variant**

Elemento per il quale recuperare le informazioni. Deve trattarsi di un oggetto [**FolderItem**](folderitem.md) .

</dd> <dt>

*iColumn* 
</dt> <dd>

Tipo: **Integer**

Valore **intero** che specifica le informazioni da recuperare. Le informazioni disponibili per un elemento dipendono dalla cartella in cui viene visualizzata. Questo valore corrisponde al numero di colonna in base zero visualizzato in una visualizzazione Shell. Per un elemento nella file system, può essere uno dei valori seguenti:

<dt>



  (0)


</dt> <dd>

Recupera il nome dell'elemento.

</dd> <dt>



 (1)


</dt> <dd>

Recupera la dimensione dell'elemento.

</dd> <dt>



 (2)


</dt> <dd>

Recupera il tipo dell'elemento.

</dd> <dt>



 (3)


</dt> <dd>

Recupera la data e l'ora dell'Ultima modifica apportata all'elemento.

</dd> <dt>



 (4)


</dt> <dd>

Recupera gli attributi dell'elemento.

</dd> <dt>



 (-1)


</dt> <dd>

Recupera le informazioni sulla descrizione comando per l'elemento.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _

Stringa contenente i dettagli recuperati.

## <a name="remarks"></a>Commenti

> [!Note]  
> Non tutti i metodi sono implementati per tutte le cartelle. Il metodo [_ *ParseName* *](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL). Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **GetDetailsOf** per recuperare il tipo del file denominato Clock.avi. L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
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
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
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
| Intestazione<br/>                   | <dl> <dt>Shlobj \_ Core. h (include shldisp. h)</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 
