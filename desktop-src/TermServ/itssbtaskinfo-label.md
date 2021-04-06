---
title: Proprietà Label ITsSbTaskInfo
description: Recupera l'etichetta che descrive lo scopo dell'attività.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà etichetta
- Etichetta Servizi Desktop remoto proprietà, interfaccia ITsSbTaskInfo
- Interfaccia ITsSbTaskInfo Servizi Desktop remoto, proprietà Label
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f85aaea366cf002d4ec1bacce8f29a6aa67fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743506"
---
# <a name="itssbtaskinfolabel-property"></a><span data-ttu-id="926ae-106">Proprietà ITsSbTaskInfo:: Label</span><span class="sxs-lookup"><span data-stu-id="926ae-106">ITsSbTaskInfo::Label property</span></span>

<span data-ttu-id="926ae-107">Recupera l'etichetta che descrive lo scopo dell'attività.</span><span class="sxs-lookup"><span data-stu-id="926ae-107">Retrieves the label that describes the purpose of the task.</span></span>

<span data-ttu-id="926ae-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="926ae-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="926ae-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="926ae-109">Syntax</span></span>


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a><span data-ttu-id="926ae-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="926ae-110">Property value</span></span>

<span data-ttu-id="926ae-111">Puntatore a un valore **BSTR** che contiene l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="926ae-111">A pointer to a **BSTR** value that contains the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="926ae-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="926ae-112">Requirements</span></span>



| <span data-ttu-id="926ae-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="926ae-113">Requirement</span></span> | <span data-ttu-id="926ae-114">Valore</span><span class="sxs-lookup"><span data-stu-id="926ae-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="926ae-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="926ae-115">Minimum supported client</span></span><br/> | <span data-ttu-id="926ae-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="926ae-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="926ae-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="926ae-117">Minimum supported server</span></span><br/> | <span data-ttu-id="926ae-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="926ae-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="926ae-119">IDL</span><span class="sxs-lookup"><span data-stu-id="926ae-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="926ae-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="926ae-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="926ae-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="926ae-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="926ae-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="926ae-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





