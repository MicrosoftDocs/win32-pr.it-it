---
description: SFVM \_ DIDDRAGDROP può essere modificato o non disponibile.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: Messaggio SFVM_DIDDRAGDROP (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994917"
---
# <a name="sfvm_diddragdrop-message"></a><span data-ttu-id="f3e9e-103">\_Messaggio SFVM DIDDRAGDROP</span><span class="sxs-lookup"><span data-stu-id="f3e9e-103">SFVM\_DIDDRAGDROP message</span></span>

<span data-ttu-id="f3e9e-104">\[**SFVM \_ DIDDRAGDROP** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-104">\[**SFVM\_DIDDRAGDROP** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f3e9e-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="f3e9e-106">Notifica alla funzione di callback che è iniziata un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-106">Notifies the callback function that a drag-and-drop operation has begun.</span></span> <span data-ttu-id="f3e9e-107">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="f3e9e-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a><span data-ttu-id="f3e9e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3e9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3e9e-109">*dwEffect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-109">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e9e-110">Identificatore dell'effetto di rilascio dall'enumerazione [**DropEffect**](../com/dropeffect-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="f3e9e-110">A drop effect specifier from the [**DROPEFFECT**](../com/dropeffect-constants.md) enumeration.</span></span> <span data-ttu-id="f3e9e-111">Questa operazione viene ottenuta chiamando [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span><span class="sxs-lookup"><span data-stu-id="f3e9e-111">This is obtained by calling [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span></span>

</dd> <dt>

<span data-ttu-id="f3e9e-112">*pIdo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-112">*pIdo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e9e-113">Puntatore all'istanza di [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="f3e9e-113">A pointer to the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3e9e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3e9e-114">Requirements</span></span>



| <span data-ttu-id="f3e9e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3e9e-115">Requirement</span></span> | <span data-ttu-id="f3e9e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f3e9e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e9e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3e9e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e9e-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f3e9e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3e9e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e9e-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f3e9e-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f3e9e-121">End of client support</span></span><br/>    | <span data-ttu-id="f3e9e-122">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="f3e9e-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="f3e9e-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f3e9e-123">End of server support</span></span><br/>    | <span data-ttu-id="f3e9e-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3e9e-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="f3e9e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3e9e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3e9e-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3e9e-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
