---
description: Ottiene un oggetto che rappresenta l'elemento padre dell'elemento.
ms.assetid: 612e76d8-d8bc-419c-b319-75b1f324840a
title: Proprietà FolderItem. Parent (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f2da3504596c3b351318b33c929dad3b5a958165
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749162"
---
# <a name="folderitemparent-property"></a><span data-ttu-id="d4855-103">Proprietà FolderItem. Parent</span><span class="sxs-lookup"><span data-stu-id="d4855-103">FolderItem.Parent property</span></span>

<span data-ttu-id="d4855-104">Ottiene un oggetto che rappresenta l'elemento padre dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d4855-104">Gets an object that represents the parent of the item.</span></span>

<span data-ttu-id="d4855-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d4855-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4855-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4855-106">Syntax</span></span>


```JScript
objParent = FolderItem.Parent
```



## <a name="property-value"></a><span data-ttu-id="d4855-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d4855-107">Property value</span></span>

<span data-ttu-id="d4855-108">Variabile di tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="d4855-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="d4855-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="d4855-109">Examples</span></span>

<span data-ttu-id="d4855-110">Nell'esempio seguente viene illustrato l'utilizzo corretto dell' **elemento padre** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d4855-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d4855-111">JScript</span><span class="sxs-lookup"><span data-stu-id="d4855-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



<span data-ttu-id="d4855-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="d4855-112">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnFolderItemParentVB()
        dim objShell
        dim objFolder2
        dim ssfWINDOWS

        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem

                set objFolderItem = objFolder2.Self
                    if (not objFolderItem is nothing) then
                        dim objParent

                        set objParent = objFolderItem.Parent
                            if (not objParent is nothing) then
                                alert("Got parent object")
                            end if
                        set objParent = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder2 = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d4855-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d4855-113">Visual Basic:</span></span>


```VB
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



## <a name="requirements"></a><span data-ttu-id="d4855-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4855-114">Requirements</span></span>



| <span data-ttu-id="d4855-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4855-115">Requirement</span></span> | <span data-ttu-id="d4855-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d4855-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4855-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4855-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d4855-118">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d4855-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d4855-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4855-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d4855-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d4855-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d4855-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4855-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4855-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4855-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d4855-123">IDL</span><span class="sxs-lookup"><span data-stu-id="d4855-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4855-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4855-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d4855-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d4855-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4855-126"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="d4855-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
