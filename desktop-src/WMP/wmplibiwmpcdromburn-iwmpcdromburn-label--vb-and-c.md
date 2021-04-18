---
title: Proprietà Label IWMPCdromBurn
description: La proprietà Label ottiene la stringa dell'etichetta del volume CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- Proprietà etichetta Windows Media Player
- Proprietà Label Media Player Windows, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, proprietà Label
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329656"
---
# <a name="iwmpcdromburnlabel-property"></a><span data-ttu-id="376bc-106">Proprietà IWMPCdromBurn:: Label</span><span class="sxs-lookup"><span data-stu-id="376bc-106">IWMPCdromBurn::label property</span></span>

<span data-ttu-id="376bc-107">La proprietà *Label* ottiene la stringa dell'etichetta del volume CD.</span><span class="sxs-lookup"><span data-stu-id="376bc-107">The *label* property gets the CD volume label string.</span></span>

<span data-ttu-id="376bc-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="376bc-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="376bc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="376bc-109">Syntax</span></span>


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a><span data-ttu-id="376bc-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="376bc-110">Property value</span></span>

<span data-ttu-id="376bc-111">**System. String** che è la stringa dell'etichetta del volume.</span><span class="sxs-lookup"><span data-stu-id="376bc-111">A **System.String** that is the volume label string.</span></span>

## <a name="remarks"></a><span data-ttu-id="376bc-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="376bc-112">Remarks</span></span>

<span data-ttu-id="376bc-113">A causa del modo in cui vengono archiviate le etichette CD, l'etichetta del CD potrebbe essere inferiore alla lunghezza della stringa dell'etichetta di volume specificata.</span><span class="sxs-lookup"><span data-stu-id="376bc-113">Due to the way CD labels are stored, the label of the CD may be shorter than the length of the specified volume label string.</span></span> <span data-ttu-id="376bc-114">Se la stringa supera la lunghezza massima consentita per un'etichetta CD, il testo verrà troncato.</span><span class="sxs-lookup"><span data-stu-id="376bc-114">If the string is longer than the maximum length of a CD label, the text will be truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="376bc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="376bc-115">Requirements</span></span>



| <span data-ttu-id="376bc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="376bc-116">Requirement</span></span> | <span data-ttu-id="376bc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="376bc-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="376bc-118">Versione</span><span class="sxs-lookup"><span data-stu-id="376bc-118">Version</span></span><br/>   | <span data-ttu-id="376bc-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="376bc-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="376bc-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="376bc-120">Namespace</span></span><br/> | <span data-ttu-id="376bc-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="376bc-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="376bc-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="376bc-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="376bc-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="376bc-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="376bc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="376bc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="376bc-125">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="376bc-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





