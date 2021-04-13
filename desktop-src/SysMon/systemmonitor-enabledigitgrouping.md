---
title: Proprietà SystemMonitor. EnableDigitGrouping
description: Recupera o imposta un valore che determina se SYSMON utilizza il raggruppamento di cifre durante la visualizzazione dei valori numerici.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Proprietà EnableDigitGrouping SysMon
- Proprietà EnableDigitGrouping SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà EnableDigitGrouping
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400653"
---
# <a name="systemmonitorenabledigitgrouping-property"></a><span data-ttu-id="06a99-106">Proprietà SystemMonitor. EnableDigitGrouping</span><span class="sxs-lookup"><span data-stu-id="06a99-106">SystemMonitor.EnableDigitGrouping property</span></span>

<span data-ttu-id="06a99-107">Recupera o imposta un valore che determina se SYSMON utilizza il raggruppamento di cifre durante la visualizzazione dei valori numerici.</span><span class="sxs-lookup"><span data-stu-id="06a99-107">Retrieves or sets a value that determines if SYSMON uses digit grouping when displaying numeric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a99-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06a99-108">Syntax</span></span>


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a><span data-ttu-id="06a99-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="06a99-109">Property value</span></span>

<span data-ttu-id="06a99-110">Se è true, SYSMON raggruppa le cifre quando si visualizzano i valori numerici, ad esempio 1.214.</span><span class="sxs-lookup"><span data-stu-id="06a99-110">If True, SYSMON will group digits when displaying numeric values, for example, 1,214.</span></span> <span data-ttu-id="06a99-111">Se false, i valori numerici non sono raggruppati, ad esempio 1214.</span><span class="sxs-lookup"><span data-stu-id="06a99-111">If False, numeric values are not grouped, for example, 1214.</span></span> <span data-ttu-id="06a99-112">Il valore predefinito è true.</span><span class="sxs-lookup"><span data-stu-id="06a99-112">True is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a99-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="06a99-113">Remarks</span></span>

<span data-ttu-id="06a99-114">Il simbolo di raggruppamento digit è localizzato.</span><span class="sxs-lookup"><span data-stu-id="06a99-114">The digit grouping symbol is localized.</span></span>

## <a name="requirements"></a><span data-ttu-id="06a99-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06a99-115">Requirements</span></span>



| <span data-ttu-id="06a99-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06a99-116">Requirement</span></span> | <span data-ttu-id="06a99-117">Valore</span><span class="sxs-lookup"><span data-stu-id="06a99-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06a99-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06a99-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06a99-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06a99-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06a99-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06a99-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06a99-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06a99-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06a99-122">DLL</span><span class="sxs-lookup"><span data-stu-id="06a99-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06a99-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="06a99-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





