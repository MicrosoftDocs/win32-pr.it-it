---
description: Esegue un verbo in una raccolta di oggetti FolderItem. Questo metodo è un'estensione del metodo InvokeVerb, che consente il controllo aggiuntivo dell'operazione tramite un set di flag.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: Metodo FolderItems2. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aa9b986b5cb76f14cc950f522e1e289224c17b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977015"
---
# <a name="folderitems2invokeverbex-method"></a><span data-ttu-id="37512-104">FolderItems2. InvokeVerbEx, metodo</span><span class="sxs-lookup"><span data-stu-id="37512-104">FolderItems2.InvokeVerbEx method</span></span>

<span data-ttu-id="37512-105">Esegue un verbo in una raccolta di oggetti [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="37512-105">Executes a verb on a collection of [**FolderItem**](folderitem.md) objects.</span></span> <span data-ttu-id="37512-106">Questo metodo è un'estensione del metodo [**InvokeVerb**](folderitem-invokeverb.md) , che consente il controllo aggiuntivo dell'operazione tramite un set di flag.</span><span class="sxs-lookup"><span data-stu-id="37512-106">This method is an extension of the [**InvokeVerb**](folderitem-invokeverb.md) method, allowing additional control of the operation through a set of flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="37512-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37512-107">Syntax</span></span>


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="37512-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="37512-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37512-109">*vVerb* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="37512-109">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37512-110">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="37512-110">Type: **Variant**</span></span>

<span data-ttu-id="37512-111">**Variant** con la stringa del verbo che corrisponde al comando da eseguire.</span><span class="sxs-lookup"><span data-stu-id="37512-111">A **Variant** with the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="37512-112">Se non viene specificato alcun verbo, viene eseguito il verbo predefinito.</span><span class="sxs-lookup"><span data-stu-id="37512-112">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="37512-113">*vArgs* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="37512-113">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37512-114">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="37512-114">Type: **Variant**</span></span>

<span data-ttu-id="37512-115">**Variant** costituito da una stringa con uno o più argomenti del comando specificato da *vVerb*.</span><span class="sxs-lookup"><span data-stu-id="37512-115">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="37512-116">Il formato di questa stringa dipende dal verbo specifico.</span><span class="sxs-lookup"><span data-stu-id="37512-116">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37512-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="37512-117">Remarks</span></span>

<span data-ttu-id="37512-118">Un verbo è una stringa utilizzata per specificare una determinata azione associata a un elemento o a una raccolta di elementi.</span><span class="sxs-lookup"><span data-stu-id="37512-118">A verb is a string used to specify a particular action associated with an item or collection of items.</span></span> <span data-ttu-id="37512-119">In genere, la chiamata di un verbo avvia un'applicazione correlata.</span><span class="sxs-lookup"><span data-stu-id="37512-119">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="37512-120">Se, ad esempio, si chiama il verbo **aperto** in un file con estensione txt, in genere il file viene aperto con un editor di testo, in genere Microsoft blocco note.</span><span class="sxs-lookup"><span data-stu-id="37512-120">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="37512-121">Per ulteriori informazioni sui verbi, vedere [avvio di applicazioni](launch.md).</span><span class="sxs-lookup"><span data-stu-id="37512-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

## <a name="examples"></a><span data-ttu-id="37512-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="37512-122">Examples</span></span>

<span data-ttu-id="37512-123">Nell'esempio seguente viene usato **InvokeVerbEx** per richiamare il verbo predefinito ("Open") su **computer locale**.</span><span class="sxs-lookup"><span data-stu-id="37512-123">The following example uses **InvokeVerbEx** to invoke the default verb ("open") on **My Computer**.</span></span> <span data-ttu-id="37512-124">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="37512-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="37512-125">JScript</span><span class="sxs-lookup"><span data-stu-id="37512-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



<span data-ttu-id="37512-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="37512-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="37512-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="37512-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="37512-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37512-128">Requirements</span></span>



| <span data-ttu-id="37512-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="37512-129">Requirement</span></span> | <span data-ttu-id="37512-130">Valore</span><span class="sxs-lookup"><span data-stu-id="37512-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37512-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37512-131">Minimum supported client</span></span><br/> | <span data-ttu-id="37512-132">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="37512-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37512-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37512-133">Minimum supported server</span></span><br/> | <span data-ttu-id="37512-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37512-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="37512-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37512-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="37512-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="37512-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="37512-137">IDL</span><span class="sxs-lookup"><span data-stu-id="37512-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37512-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="37512-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="37512-139">DLL</span><span class="sxs-lookup"><span data-stu-id="37512-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37512-140"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="37512-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37512-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37512-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37512-142">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="37512-142">**FolderItems2**</span></span>](folderitems2-object.md)
</dt> <dt>

[<span data-ttu-id="37512-143">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="37512-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




