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
# <a name="foldergetdetailsof-method"></a><span data-ttu-id="8b009-104">Folder. GetDetailsOf, metodo</span><span class="sxs-lookup"><span data-stu-id="8b009-104">Folder.GetDetailsOf method</span></span>

<span data-ttu-id="8b009-105">Recupera i dettagli relativi a un elemento in una cartella.</span><span class="sxs-lookup"><span data-stu-id="8b009-105">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="8b009-106">Ad esempio, le dimensioni, il tipo o l'ora dell'Ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="8b009-106">For example, its size, type, or the time of its last modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b009-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b009-107">Syntax</span></span>


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a><span data-ttu-id="8b009-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b009-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b009-109">*vItem*</span><span class="sxs-lookup"><span data-stu-id="8b009-109">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="8b009-110">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="8b009-110">Type: **Variant**</span></span>

<span data-ttu-id="8b009-111">Elemento per il quale recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="8b009-111">The item for which to retrieve the information.</span></span> <span data-ttu-id="8b009-112">Deve trattarsi di un oggetto [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="8b009-112">This must be a [**FolderItem**](folderitem.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="8b009-113">*iColumn*</span><span class="sxs-lookup"><span data-stu-id="8b009-113">*iColumn*</span></span> 
</dt> <dd>

<span data-ttu-id="8b009-114">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="8b009-114">Type: **Integer**</span></span>

<span data-ttu-id="8b009-115">Valore **intero** che specifica le informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8b009-115">An **Integer** value that specifies the information to be retrieved.</span></span> <span data-ttu-id="8b009-116">Le informazioni disponibili per un elemento dipendono dalla cartella in cui viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="8b009-116">The information available for an item depends on the folder in which it is displayed.</span></span> <span data-ttu-id="8b009-117">Questo valore corrisponde al numero di colonna in base zero visualizzato in una visualizzazione Shell.</span><span class="sxs-lookup"><span data-stu-id="8b009-117">This value corresponds to the zero-based column number that is displayed in a Shell view.</span></span> <span data-ttu-id="8b009-118">Per un elemento nella file system, può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8b009-118">For an item in the file system, this can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="8b009-119"> (0)</span><span class="sxs-lookup"><span data-stu-id="8b009-119">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8b009-120">Recupera il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8b009-120">Retrieves the name of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="8b009-121">(1)</span><span class="sxs-lookup"><span data-stu-id="8b009-121">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8b009-122">Recupera la dimensione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8b009-122">Retrieves the size of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="8b009-123">(2)</span><span class="sxs-lookup"><span data-stu-id="8b009-123">(2)</span></span>


</dt> <dd>

<span data-ttu-id="8b009-124">Recupera il tipo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8b009-124">Retrieves the type of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="8b009-125">(3)</span><span class="sxs-lookup"><span data-stu-id="8b009-125">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8b009-126">Recupera la data e l'ora dell'Ultima modifica apportata all'elemento.</span><span class="sxs-lookup"><span data-stu-id="8b009-126">Retrieves the date and time that the item was last modified.</span></span>

</dd> <dt>



 <span data-ttu-id="8b009-127">(4)</span><span class="sxs-lookup"><span data-stu-id="8b009-127">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8b009-128">Recupera gli attributi dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8b009-128">Retrieves the attributes of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="8b009-129">(-1)</span><span class="sxs-lookup"><span data-stu-id="8b009-129">(-1)</span></span>


</dt> <dd>

<span data-ttu-id="8b009-130">Recupera le informazioni sulla descrizione comando per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="8b009-130">Retrieves the info tip information for the item.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b009-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b009-131">Return value</span></span>

<span data-ttu-id="8b009-132">Tipo: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="8b009-132">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="8b009-133">Stringa contenente i dettagli recuperati.</span><span class="sxs-lookup"><span data-stu-id="8b009-133">String containing the retrieved detail.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b009-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b009-134">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8b009-135">Non tutti i metodi sono implementati per tutte le cartelle.</span><span class="sxs-lookup"><span data-stu-id="8b009-135">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="8b009-136">Il metodo [_ *ParseName* \*](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL).</span><span class="sxs-lookup"><span data-stu-id="8b009-136">For example, the [_ *ParseName*\*](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="8b009-137">Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).</span><span class="sxs-lookup"><span data-stu-id="8b009-137">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8b009-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="8b009-138">Examples</span></span>

<span data-ttu-id="8b009-139">Nell'esempio seguente viene usato **GetDetailsOf** per recuperare il tipo del file denominato Clock.avi.</span><span class="sxs-lookup"><span data-stu-id="8b009-139">The following example uses **GetDetailsOf** to retrieve the type of the file named Clock.avi.</span></span> <span data-ttu-id="8b009-140">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8b009-140">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8b009-141">JScript</span><span class="sxs-lookup"><span data-stu-id="8b009-141">JScript:</span></span>


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



<span data-ttu-id="8b009-142">VBScript</span><span class="sxs-lookup"><span data-stu-id="8b009-142">VBScript:</span></span>


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



<span data-ttu-id="8b009-143">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8b009-143">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8b009-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b009-144">Requirements</span></span>



| <span data-ttu-id="8b009-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b009-145">Requirement</span></span> | <span data-ttu-id="8b009-146">Valore</span><span class="sxs-lookup"><span data-stu-id="8b009-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b009-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b009-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8b009-148">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8b009-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8b009-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b009-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8b009-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8b009-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8b009-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b009-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b009-152"><dt>Shlobj \_ Core. h (include shldisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b009-152"><dt>Shlobj\_core.h (include Shldisp.h)</dt></span></span> </dl>  |
| <span data-ttu-id="8b009-153">IDL</span><span class="sxs-lookup"><span data-stu-id="8b009-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b009-154"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b009-154"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8b009-155">DLL</span><span class="sxs-lookup"><span data-stu-id="8b009-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b009-156"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="8b009-156"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
