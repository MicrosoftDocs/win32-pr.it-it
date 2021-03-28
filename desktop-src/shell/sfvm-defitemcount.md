---
description: "Consente all'oggetto callback di specificare il numero di elementi nella visualizzazione cartelle. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_DEFITEMCOUNT (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 62306eaa-e52e-432b-9233-d990519d5739
api_name:
- SFVM_DEFITEMCOUNT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4e3f746e422428ab9f925cf4ff3f460ccd578367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967747"
---
# <a name="sfvm_defitemcount-message"></a><span data-ttu-id="a554a-104">\_Messaggio SFVM DEFITEMCOUNT</span><span class="sxs-lookup"><span data-stu-id="a554a-104">SFVM\_DEFITEMCOUNT message</span></span>

<span data-ttu-id="a554a-105">Consente all'oggetto callback di specificare il numero di elementi nella visualizzazione cartelle.</span><span class="sxs-lookup"><span data-stu-id="a554a-105">Allows the callback object to specify the number of items in the folder view.</span></span> <span data-ttu-id="a554a-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="a554a-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFITEMCOUNT 

    lParam = (LPARAM)(UINT*) cItems;

            
```



## <a name="parameters"></a><span data-ttu-id="a554a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a554a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a554a-108">*cItems* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a554a-108">*cItems* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a554a-109">Numero di elementi nella visualizzazione cartelle.</span><span class="sxs-lookup"><span data-stu-id="a554a-109">The number of items in the folder view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a554a-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a554a-110">Requirements</span></span>



| <span data-ttu-id="a554a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a554a-111">Requirement</span></span> | <span data-ttu-id="a554a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a554a-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a554a-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a554a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a554a-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a554a-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a554a-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a554a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a554a-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a554a-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a554a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a554a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a554a-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="a554a-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
