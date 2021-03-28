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
# <a name="folderiteminvokeverb-method"></a><span data-ttu-id="76065-103">FolderItem. InvokeVerb, metodo</span><span class="sxs-lookup"><span data-stu-id="76065-103">FolderItem.InvokeVerb method</span></span>

<span data-ttu-id="76065-104">Esegue un verbo sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="76065-104">Executes a verb on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="76065-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76065-105">Syntax</span></span>


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a><span data-ttu-id="76065-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="76065-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76065-107">*vVerb* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="76065-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76065-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="76065-108">Type: **Variant**</span></span>

<span data-ttu-id="76065-109">Stringa che specifica il verbo da eseguire.</span><span class="sxs-lookup"><span data-stu-id="76065-109">A string that specifies the verb to be executed.</span></span> <span data-ttu-id="76065-110">Deve corrispondere a uno dei valori restituiti dalla proprietà [**FolderItemVerb.Name**](folderitemverb-name.md) dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="76065-110">It must be one of the values returned by the item's [**FolderItemVerb.Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="76065-111">Se non viene specificato alcun verbo, verrà richiamato il verbo predefinito.</span><span class="sxs-lookup"><span data-stu-id="76065-111">If no verb is specified, the default verb will be invoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76065-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76065-112">Return value</span></span>

<span data-ttu-id="76065-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="76065-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76065-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="76065-114">Remarks</span></span>

<span data-ttu-id="76065-115">Un verbo è una stringa utilizzata per specificare un'azione specifica supportata da un elemento.</span><span class="sxs-lookup"><span data-stu-id="76065-115">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="76065-116">La chiamata di un verbo equivale alla selezione di un comando dal menu di scelta rapida di un elemento.</span><span class="sxs-lookup"><span data-stu-id="76065-116">Invoking a verb is equivalent to selecting a command from an item's shortcut menu.</span></span> <span data-ttu-id="76065-117">In genere, la chiamata di un verbo avvia un'applicazione correlata.</span><span class="sxs-lookup"><span data-stu-id="76065-117">Typically, invoking a verb launches a related application.</span></span> <span data-ttu-id="76065-118">Se ad esempio si richiama il verbo "Open" in un file con estensione txt, il file verrà aperto con un editor di testo, in genere Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="76065-118">For example, invoking the "open" verb on a .txt file opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="76065-119">Per ulteriori informazioni sui verbi, vedere [avvio delle applicazioni](launch.md) .</span><span class="sxs-lookup"><span data-stu-id="76065-119">See [Launching Applications](launch.md) for further discussion of verbs.</span></span>

<span data-ttu-id="76065-120">L'oggetto [**folderitemverbs**](folderitemverbs.md) rappresenta la raccolta di verbi associati all'elemento.</span><span class="sxs-lookup"><span data-stu-id="76065-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="76065-121">Il verbo predefinito può variare per elementi diversi, ma in genere è "aperto".</span><span class="sxs-lookup"><span data-stu-id="76065-121">The default verb may vary for different items, but it is typically "open".</span></span>

## <a name="examples"></a><span data-ttu-id="76065-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="76065-122">Examples</span></span>

<span data-ttu-id="76065-123">Nell'esempio seguente viene usato **InvokeVerb** per richiamare il verbo predefinito (in questo caso "Open") nella cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="76065-123">The following example uses **InvokeVerb** to invoke the default verb ("open" in this case) on the Windows folder.</span></span> <span data-ttu-id="76065-124">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="76065-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="76065-125">JScript</span><span class="sxs-lookup"><span data-stu-id="76065-125">JScript:</span></span>


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



<span data-ttu-id="76065-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="76065-126">VBScript:</span></span>


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



<span data-ttu-id="76065-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="76065-127">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="76065-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76065-128">Requirements</span></span>



| <span data-ttu-id="76065-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="76065-129">Requirement</span></span> | <span data-ttu-id="76065-130">Valore</span><span class="sxs-lookup"><span data-stu-id="76065-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76065-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76065-131">Minimum supported client</span></span><br/> | <span data-ttu-id="76065-132">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="76065-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="76065-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76065-133">Minimum supported server</span></span><br/> | <span data-ttu-id="76065-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="76065-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="76065-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76065-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="76065-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="76065-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="76065-137">IDL</span><span class="sxs-lookup"><span data-stu-id="76065-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76065-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76065-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="76065-139">DLL</span><span class="sxs-lookup"><span data-stu-id="76065-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76065-140"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="76065-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76065-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76065-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76065-142">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="76065-142">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="76065-143">**Verbi**</span><span class="sxs-lookup"><span data-stu-id="76065-143">**Verbs**</span></span>](folderitem-verbs.md)
</dt> <dt>

[<span data-ttu-id="76065-144">**DoIt**</span><span class="sxs-lookup"><span data-stu-id="76065-144">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




