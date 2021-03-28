---
description: "Consente all'oggetto callback di specificare un parametro di ordinamento predefinito. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_GETSORTDEFAULTS (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980882"
---
# <a name="sfvm_getsortdefaults-message"></a><span data-ttu-id="14045-104">\_Messaggio SFVM GETSORTDEFAULTS</span><span class="sxs-lookup"><span data-stu-id="14045-104">SFVM\_GETSORTDEFAULTS message</span></span>

<span data-ttu-id="14045-105">Consente all'oggetto callback di specificare un parametro di ordinamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="14045-105">Allows the callback object to specify a default sorting parameter.</span></span> <span data-ttu-id="14045-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="14045-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="14045-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="14045-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14045-108">*iDirection* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="14045-108">*iDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14045-109">Direzione di ordinamento predefinita.</span><span class="sxs-lookup"><span data-stu-id="14045-109">The default sorting direction.</span></span> <span data-ttu-id="14045-110">Impostare questo parametro su un valore positivo per eseguire l'ordinamento in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="14045-110">Set this parameter to a positive value to sort in ascending order.</span></span> <span data-ttu-id="14045-111">Impostare questo parametro su zero o su un valore negativo per eseguire l'ordinamento in ordine decrescente.</span><span class="sxs-lookup"><span data-stu-id="14045-111">Set this parameter to zero or a negative value to sort in descending order.</span></span>

</dd> <dt>

<span data-ttu-id="14045-112">*IColumn* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="14045-112">*iColumn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14045-113">Colonna utilizzata per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="14045-113">The column used for the sort.</span></span> <span data-ttu-id="14045-114">Questa operazione verrà passata a [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) nei 16 bit inferiori del relativo valore *lParam* .</span><span class="sxs-lookup"><span data-stu-id="14045-114">This will be passed to the [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) in the lower 16 bits of its *lParam* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14045-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="14045-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="14045-116">: **SFVM \_ GETSORTDEFAULTS** non è riconosciuto dall'oggetto visualizzazione cartella di sistema.</span><span class="sxs-lookup"><span data-stu-id="14045-116">: **SFVM\_GETSORTDEFAULTS** is not recognized by the system folder view object.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="14045-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14045-117">Requirements</span></span>



| <span data-ttu-id="14045-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="14045-118">Requirement</span></span> | <span data-ttu-id="14045-119">Valore</span><span class="sxs-lookup"><span data-stu-id="14045-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="14045-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14045-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14045-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14045-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="14045-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14045-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14045-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14045-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="14045-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14045-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="14045-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="14045-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
