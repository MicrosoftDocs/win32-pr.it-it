---
title: Messaggio TB_GETBITMAP (COMmctrl. h)
description: Recupera l'indice della bitmap associata a un pulsante in una barra degli strumenti.
ms.assetid: 64878cca-7d71-48ad-b2ed-d2bdc3067592
keywords:
- Controlli di Windows Message TB_GETBITMAP
topic_type:
- apiref
api_name:
- TB_GETBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771073b67b1421a5d9bda9d162bc234400c85885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965002"
---
# <a name="tb_getbitmap-message"></a><span data-ttu-id="aebb5-104">\_Messaggio GETBITMAP TB</span><span class="sxs-lookup"><span data-stu-id="aebb5-104">TB\_GETBITMAP message</span></span>

<span data-ttu-id="aebb5-105">Recupera l'indice della bitmap associata a un pulsante in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="aebb5-105">Retrieves the index of the bitmap associated with a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="aebb5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aebb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aebb5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aebb5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aebb5-108">Identificatore di comando del pulsante di cui deve essere recuperato l'indice bitmap.</span><span class="sxs-lookup"><span data-stu-id="aebb5-108">Command identifier of the button whose bitmap index is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="aebb5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aebb5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="aebb5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="aebb5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aebb5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aebb5-111">Return value</span></span>

<span data-ttu-id="aebb5-112">Restituisce l'indice della bitmap, se ha esito positivo, oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="aebb5-112">Returns the index of the bitmap if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="aebb5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aebb5-113">Requirements</span></span>



| <span data-ttu-id="aebb5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aebb5-114">Requirement</span></span> | <span data-ttu-id="aebb5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="aebb5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aebb5-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aebb5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aebb5-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aebb5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aebb5-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aebb5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aebb5-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aebb5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aebb5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aebb5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aebb5-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aebb5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





