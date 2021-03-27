---
description: "Consente all'oggetto callback di fornire una pagina da aggiungere alla finestra delle proprietà delle proprietà dell'oggetto selezionato. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_ADDPROPERTYPAGES (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994885"
---
# <a name="sfvm_addpropertypages-message"></a><span data-ttu-id="95fc5-104">\_Messaggio SFVM ADDPROPERTYPAGES</span><span class="sxs-lookup"><span data-stu-id="95fc5-104">SFVM\_ADDPROPERTYPAGES message</span></span>

<span data-ttu-id="95fc5-105">Consente all'oggetto callback di fornire una pagina da aggiungere alla finestra **delle proprietà delle proprietà dell'** oggetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="95fc5-105">Allows the callback object to provide a page to add to the **Properties** property sheet of the selected object.</span></span> <span data-ttu-id="95fc5-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="95fc5-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a><span data-ttu-id="95fc5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="95fc5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95fc5-108">*pData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="95fc5-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95fc5-109">Indirizzo di una struttura [**di \_ \_ dati SFVM**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) .</span><span class="sxs-lookup"><span data-stu-id="95fc5-109">The address of a [**SFVM\_PROPPAGE\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95fc5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="95fc5-110">Remarks</span></span>

<span data-ttu-id="95fc5-111">Questo messaggio funge essenzialmente dalla stessa funzione di [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="95fc5-111">This message serves essentially the same function as [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span> <span data-ttu-id="95fc5-112">Per ulteriori informazioni, vedere [creazione di gestori della finestra delle proprietà](propsheet-handlers.md) .</span><span class="sxs-lookup"><span data-stu-id="95fc5-112">See [Creating Property Sheet Handlers](propsheet-handlers.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="95fc5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95fc5-113">Requirements</span></span>



| <span data-ttu-id="95fc5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="95fc5-114">Requirement</span></span> | <span data-ttu-id="95fc5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="95fc5-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="95fc5-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95fc5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="95fc5-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="95fc5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="95fc5-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95fc5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="95fc5-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="95fc5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="95fc5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95fc5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="95fc5-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="95fc5-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
