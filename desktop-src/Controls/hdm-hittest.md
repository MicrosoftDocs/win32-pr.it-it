---
title: Messaggio HDM_HITTEST (COMmctrl. h)
description: Verifica un punto per determinare quale elemento di intestazione, se presente, si trova in corrispondenza del punto specificato.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- Controlli di Windows Message HDM_HITTEST
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120306"
---
# <a name="hdm_hittest-message"></a><span data-ttu-id="bbfbc-104">\_Messaggio HDM HITTEST</span><span class="sxs-lookup"><span data-stu-id="bbfbc-104">HDM\_HITTEST message</span></span>

<span data-ttu-id="bbfbc-105">Verifica un punto per determinare quale elemento di intestazione, se presente, si trova in corrispondenza del punto specificato.</span><span class="sxs-lookup"><span data-stu-id="bbfbc-105">Tests a point to determine which header item, if any, is at the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbfbc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbfbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbfbc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbfbc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bbfbc-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bbfbc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bbfbc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbfbc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbfbc-110">Puntatore a una struttura [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) contenente la posizione in cui eseguire il test e ricevere informazioni sui risultati del test.</span><span class="sxs-lookup"><span data-stu-id="bbfbc-110">A pointer to an [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) structure that contains the position to test and receives information about the results of the test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbfbc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbfbc-111">Return value</span></span>

<span data-ttu-id="bbfbc-112">Restituisce l'indice dell'elemento in corrispondenza della posizione specificata, se presente, oppure 1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bbfbc-112">Returns the index of the item at the specified position, if any, or   1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbfbc-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbfbc-113">Requirements</span></span>



| <span data-ttu-id="bbfbc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbfbc-114">Requirement</span></span> | <span data-ttu-id="bbfbc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bbfbc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbfbc-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbfbc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bbfbc-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bbfbc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbfbc-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbfbc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bbfbc-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bbfbc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbfbc-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbfbc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbfbc-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbfbc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





