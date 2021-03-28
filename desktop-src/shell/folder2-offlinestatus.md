---
description: Contiene lo stato offline della cartella.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Proprietà Cartella2. OfflineStatus (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977071"
---
# <a name="folder2offlinestatus-property"></a><span data-ttu-id="75650-103">Proprietà Cartella2. OfflineStatus</span><span class="sxs-lookup"><span data-stu-id="75650-103">Folder2.OfflineStatus property</span></span>

<span data-ttu-id="75650-104">Contiene lo stato offline della cartella.</span><span class="sxs-lookup"><span data-stu-id="75650-104">Contains the offline status of the folder.</span></span>

<span data-ttu-id="75650-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="75650-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="75650-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75650-106">Syntax</span></span>


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a><span data-ttu-id="75650-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="75650-107">Property value</span></span>

<span data-ttu-id="75650-108">**Intero** impostato su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="75650-108">An **Integer** that is set to one of the following values.</span></span>

<dt>



 <span data-ttu-id="75650-109">(OFS \_ DIRTYCACHE)</span><span class="sxs-lookup"><span data-stu-id="75650-109">(OFS\_DIRTYCACHE)</span></span>


</dt> <dd>

<span data-ttu-id="75650-110">Il server è online con modifiche non sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="75650-110">Server is online with unsynchronized changes.</span></span>

</dd> <dt>



 <span data-ttu-id="75650-111">(OFS \_ INATTIVO</span><span class="sxs-lookup"><span data-stu-id="75650-111">(OFS\_INACTIVE)</span></span>


</dt> <dd>

<span data-ttu-id="75650-112">La memorizzazione nella cache offline non è abilitata per questa cartella.</span><span class="sxs-lookup"><span data-stu-id="75650-112">Offline caching is not enabled for this folder.</span></span>

</dd> <dt>



 <span data-ttu-id="75650-113">(OFS \_ OFFLINE</span><span class="sxs-lookup"><span data-stu-id="75650-113">(OFS\_OFFLINE)</span></span>


</dt> <dd>

<span data-ttu-id="75650-114">Il server è offline.</span><span class="sxs-lookup"><span data-stu-id="75650-114">Server is offline.</span></span>

</dd> <dt>



 <span data-ttu-id="75650-115">(OFS \_ ONLINE</span><span class="sxs-lookup"><span data-stu-id="75650-115">(OFS\_ONLINE)</span></span>


</dt> <dd>

<span data-ttu-id="75650-116">Il server è online.</span><span class="sxs-lookup"><span data-stu-id="75650-116">Server is online.</span></span>

</dd> <dt>



 <span data-ttu-id="75650-117">(OFS \_ SERVERBACK)</span><span class="sxs-lookup"><span data-stu-id="75650-117">(OFS\_SERVERBACK)</span></span>


</dt> <dd>

<span data-ttu-id="75650-118">Il server è offline, ma è possibile raggiungerlo.</span><span class="sxs-lookup"><span data-stu-id="75650-118">Server is offline but can be reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75650-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="75650-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="75650-120">Per il corretto funzionamento di **OfflineStatus** , è necessario abilitare la file offline tramite Opzioni cartella.</span><span class="sxs-lookup"><span data-stu-id="75650-120">Offline Files must be enabled through Folder Options for **OfflineStatus** to work correctly.</span></span> <span data-ttu-id="75650-121">Se l'opzione File offline non è abilitata, la proprietà restituisce **OFS \_ inactive**.</span><span class="sxs-lookup"><span data-stu-id="75650-121">If the Offline Files option is not enabled, the property returns **OFS\_INACTIVE**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="75650-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="75650-122">Examples</span></span>

<span data-ttu-id="75650-123">Nell'esempio seguente viene illustrato l'uso corretto di **OfflineStatus** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="75650-123">The following example shows the proper use of **OfflineStatus** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="75650-124">JScript</span><span class="sxs-lookup"><span data-stu-id="75650-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



<span data-ttu-id="75650-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="75650-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="75650-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="75650-126">Visual Basic:</span></span>


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="75650-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75650-127">Requirements</span></span>



| <span data-ttu-id="75650-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="75650-128">Requirement</span></span> | <span data-ttu-id="75650-129">Valore</span><span class="sxs-lookup"><span data-stu-id="75650-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75650-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75650-130">Minimum supported client</span></span><br/> | <span data-ttu-id="75650-131">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="75650-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75650-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75650-132">Minimum supported server</span></span><br/> | <span data-ttu-id="75650-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75650-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="75650-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75650-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="75650-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="75650-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="75650-136">IDL</span><span class="sxs-lookup"><span data-stu-id="75650-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="75650-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="75650-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="75650-138">DLL</span><span class="sxs-lookup"><span data-stu-id="75650-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75650-139"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="75650-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75650-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75650-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75650-141">**Cartella2**</span><span class="sxs-lookup"><span data-stu-id="75650-141">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="75650-142">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="75650-142">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




