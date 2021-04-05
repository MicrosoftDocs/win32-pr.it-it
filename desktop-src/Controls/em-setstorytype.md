---
title: Messaggio di EM_SETSTORYTYPE (RichEdit. h)
description: Imposta il tipo di storia.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- Controlli di Windows Message EM_SETSTORYTYPE
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873590"
---
# <a name="em_setstorytype-message"></a><span data-ttu-id="3bb26-104">\_Messaggio SETSTORYTYPE em</span><span class="sxs-lookup"><span data-stu-id="3bb26-104">EM\_SETSTORYTYPE message</span></span>

<span data-ttu-id="3bb26-105">Imposta il tipo di storia.</span><span class="sxs-lookup"><span data-stu-id="3bb26-105">Sets the story type.</span></span>


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a><span data-ttu-id="3bb26-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3bb26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb26-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3bb26-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb26-108">Indice della storia.</span><span class="sxs-lookup"><span data-stu-id="3bb26-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="3bb26-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3bb26-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb26-110">Nuovo tipo di storia.</span><span class="sxs-lookup"><span data-stu-id="3bb26-110">The new story type.</span></span> <span data-ttu-id="3bb26-111">Per un elenco di tipi di storie, vedere [**em \_ GETSTORYTYPE**](em-getstorytype.md).</span><span class="sxs-lookup"><span data-stu-id="3bb26-111">For a list of story types, see [**EM\_GETSTORYTYPE**](em-getstorytype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb26-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3bb26-112">Return value</span></span>

<span data-ttu-id="3bb26-113">Tipo di storia che è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="3bb26-113">The story type that was set.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb26-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bb26-114">Requirements</span></span>



| <span data-ttu-id="3bb26-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bb26-115">Requirement</span></span> | <span data-ttu-id="3bb26-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3bb26-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb26-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bb26-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb26-118">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3bb26-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3bb26-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bb26-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb26-120">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3bb26-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3bb26-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3bb26-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bb26-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bb26-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





