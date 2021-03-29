---
description: Esegue un verbo su un elemento della shell.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Metodo ShellFolderItem. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978159"
---
# <a name="shellfolderiteminvokeverbex-method"></a><span data-ttu-id="839e7-103">ShellFolderItem. InvokeVerbEx, metodo</span><span class="sxs-lookup"><span data-stu-id="839e7-103">ShellFolderItem.InvokeVerbEx method</span></span>

<span data-ttu-id="839e7-104">Esegue un verbo su un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="839e7-104">Executes a verb on a Shell item.</span></span>

## <a name="syntax"></a><span data-ttu-id="839e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="839e7-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="839e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="839e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="839e7-107">*vVerb* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="839e7-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="839e7-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="839e7-108">Type: **Variant**</span></span>

<span data-ttu-id="839e7-109">**Variant** che contiene la stringa del verbo che corrisponde al comando da eseguire.</span><span class="sxs-lookup"><span data-stu-id="839e7-109">A **Variant** that contains the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="839e7-110">Deve corrispondere a uno dei valori restituiti dalla proprietà [**Name**](folderitemverb-name.md) dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="839e7-110">It must be one of the values returned by the item's [**Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="839e7-111">Se non viene specificato alcun verbo, viene eseguito il verbo predefinito.</span><span class="sxs-lookup"><span data-stu-id="839e7-111">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="839e7-112">*vArgs* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="839e7-112">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="839e7-113">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="839e7-113">Type: **Variant**</span></span>

<span data-ttu-id="839e7-114">**Variant** costituito da una stringa con uno o più argomenti del comando specificato da *vVerb*.</span><span class="sxs-lookup"><span data-stu-id="839e7-114">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="839e7-115">Il formato di questa stringa dipende dal verbo specifico.</span><span class="sxs-lookup"><span data-stu-id="839e7-115">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="839e7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="839e7-116">Remarks</span></span>

<span data-ttu-id="839e7-117">Un verbo è una stringa utilizzata per specificare un'azione specifica supportata da un elemento.</span><span class="sxs-lookup"><span data-stu-id="839e7-117">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="839e7-118">In genere, la chiamata di un verbo avvia un'applicazione correlata.</span><span class="sxs-lookup"><span data-stu-id="839e7-118">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="839e7-119">Se, ad esempio, si chiama il verbo **aperto** in un file con estensione txt, in genere il file viene aperto con un editor di testo, in genere Microsoft blocco note.</span><span class="sxs-lookup"><span data-stu-id="839e7-119">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="839e7-120">L'oggetto [**folderitemverbs**](folderitemverbs.md) rappresenta la raccolta di verbi associati all'elemento.</span><span class="sxs-lookup"><span data-stu-id="839e7-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="839e7-121">Per ulteriori informazioni sui verbi, vedere [avvio di applicazioni](launch.md).</span><span class="sxs-lookup"><span data-stu-id="839e7-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

<span data-ttu-id="839e7-122">Questo metodo è simile a [**InvokeVerb**](folderitem-invokeverb.md), ma consente di specificare argomenti per il comando e per il comando stesso.</span><span class="sxs-lookup"><span data-stu-id="839e7-122">This method is similar to [**InvokeVerb**](folderitem-invokeverb.md), but it allows you to specify arguments to the command as well as the command itself.</span></span>

## <a name="examples"></a><span data-ttu-id="839e7-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="839e7-123">Examples</span></span>

<span data-ttu-id="839e7-124">Negli esempi seguenti viene illustrato l'utilizzo corretto di questo metodo in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="839e7-124">The following examples show the proper use of this method in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="839e7-125">JScript</span><span class="sxs-lookup"><span data-stu-id="839e7-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



<span data-ttu-id="839e7-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="839e7-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
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
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="839e7-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="839e7-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="839e7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="839e7-128">Requirements</span></span>



| <span data-ttu-id="839e7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="839e7-129">Requirement</span></span> | <span data-ttu-id="839e7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="839e7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="839e7-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="839e7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="839e7-132">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="839e7-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="839e7-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="839e7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="839e7-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="839e7-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="839e7-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="839e7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="839e7-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="839e7-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="839e7-137">IDL</span><span class="sxs-lookup"><span data-stu-id="839e7-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="839e7-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="839e7-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="839e7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="839e7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="839e7-140"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="839e7-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="839e7-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="839e7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="839e7-142">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="839e7-142">**ShellFolderItem**</span></span>](shellfolderitem-object.md)
</dt> <dt>

[<span data-ttu-id="839e7-143">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="839e7-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




