---
description: Imposta un filtro con caratteri jolly da applicare agli elementi restituiti.
ms.assetid: 19ca82c5-16ff-46c7-8ea1-ddbfc2ce3ac9
title: Metodo FolderItems3. Filter (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems3.Filter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 26a24dc3ef1f4d0de09dbd97a5dce4c8ed8c783b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749138"
---
# <a name="folderitems3filter-method"></a><span data-ttu-id="cbfed-103">Metodo FolderItems3. Filter</span><span class="sxs-lookup"><span data-stu-id="cbfed-103">FolderItems3.Filter method</span></span>

<span data-ttu-id="cbfed-104">Imposta un filtro con caratteri jolly da applicare agli elementi restituiti.</span><span class="sxs-lookup"><span data-stu-id="cbfed-104">Sets a wildcard filter to apply to the items returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbfed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbfed-105">Syntax</span></span>


```JScript
iRetVal = FolderItems3.Filter(
  grfFlags,
  bstrFilter
)
```



## <a name="parameters"></a><span data-ttu-id="cbfed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cbfed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbfed-107">*grfFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbfed-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbfed-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="cbfed-108">Type: **Integer**</span></span>

<span data-ttu-id="cbfed-109">Questo parametro può essere uno dei flag elencati in [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf).</span><span class="sxs-lookup"><span data-stu-id="cbfed-109">This parameter can be one of the flags listed in [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf).</span></span>

</dd> <dt>

<span data-ttu-id="cbfed-110">*bstrFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbfed-110">*bstrFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbfed-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cbfed-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cbfed-112">Stringa di filtro che specifica gli elementi che devono essere elencati nella raccolta [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfed-112">A filter string that specifies what should be listed in the [**FolderItems**](folderitems.md) collection.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="cbfed-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="cbfed-113">Examples</span></span>

<span data-ttu-id="cbfed-114">Nell'esempio seguente viene illustrato l'utilizzo corretto del **filtro** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cbfed-114">The following example shows the proper usage of **Filter** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cbfed-115">JScript</span><span class="sxs-lookup"><span data-stu-id="cbfed-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems3FilterJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems3;
            
            objFolderItems3 = objFolder.Items();
            if (objFolderItems3 != null)
            {
                var SHCONTF_NONFOLDERS = 64;
                
                alert(objFolderItems3.Count);
                objFolderItems3.Filter(SHCONTF_NONFOLDERS, "*.txt");
                alert(objFolderItems3.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="cbfed-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="cbfed-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems3FilterVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems3
                        
                set objFolderItems3 = objFolder.Items()
                if (not objFolderItems3 is nothing) then
                    dim SHCONTF_NONFOLDERS
                
                    SHCONTF_NONFOLDERS = 64
                    alert(objFolderItems3.Count)
                    objFolderItems3.Filter SHCONTF_NONFOLDERS, "*.txt"
                    alert(objFolderItems3.Count)
                end if
                set objFolderItems3 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="cbfed-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cbfed-117">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems3FilterVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems3 As FolderItems3
            
            Set objFolderItems3 = objFolder.Items
                If (Not objFolderItems3 Is Nothing) Then
                    Dim SHCONTF_NONFOLDERS As Long
                    
                    SHCONTF_NONFOLDERS = 64
                    Debug.Print objFolderItems3.Count
                    objFolderItems3.Filter SHCONTF_NONFOLDERS, "*.exe"
                    Debug.Print objFolderItems3.Count
                End If
            Set objFolderItems3 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cbfed-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbfed-118">Requirements</span></span>



| <span data-ttu-id="cbfed-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbfed-119">Requirement</span></span> | <span data-ttu-id="cbfed-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cbfed-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbfed-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbfed-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cbfed-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cbfed-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cbfed-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbfed-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cbfed-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cbfed-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cbfed-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbfed-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbfed-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbfed-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cbfed-127">IDL</span><span class="sxs-lookup"><span data-stu-id="cbfed-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cbfed-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cbfed-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cbfed-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cbfed-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbfed-130"><dt>Shell32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="cbfed-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbfed-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbfed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbfed-132">**FolderItems3**</span><span class="sxs-lookup"><span data-stu-id="cbfed-132">**FolderItems3**</span></span>](folderitems3-object.md)
</dt> <dt>

[<span data-ttu-id="cbfed-133">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="cbfed-133">**FolderItems2**</span></span>](folderitems2-object.md)
</dt> <dt>

[<span data-ttu-id="cbfed-134">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="cbfed-134">**FolderItem**</span></span>](folderitem.md)
</dt> </dl>

 

 
