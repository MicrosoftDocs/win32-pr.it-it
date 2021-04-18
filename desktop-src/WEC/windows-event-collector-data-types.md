---
title: Tipi di dati dell'agente di raccolta eventi Windows (Evcoll. h)
description: I tipi di dati per l'agente di raccolta eventi di Windows vengono utilizzati come tipi di variabile oggetto sottoscrizione evento, tipi di parametri di funzione e tipi restituiti di funzione.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300921"
---
# <a name="windows-event-collector-data-types"></a><span data-ttu-id="196a4-105">Tipi di dati dell'agente di raccolta eventi Windows</span><span class="sxs-lookup"><span data-stu-id="196a4-105">Windows Event Collector Data Types</span></span>

<span data-ttu-id="196a4-106">I tipi di dati per l'agente di raccolta eventi di Windows vengono utilizzati come tipi di variabile oggetto sottoscrizione evento, tipi di parametri di funzione e tipi restituiti di funzione.</span><span class="sxs-lookup"><span data-stu-id="196a4-106">The data types for the Windows Event Collector are used as event subscription object variable types, function parameter types, and function return types.</span></span>


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="196a4-107">**\_handle EC**</span><span class="sxs-lookup"><span data-stu-id="196a4-107">**EC\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="196a4-108">Handle per un oggetto sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="196a4-108">Handle to a subscription object.</span></span> <span data-ttu-id="196a4-109">Utilizzato per rappresentare una sottoscrizione dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="196a4-109">Used to represent an event collector subscription.</span></span>

</dd> <dt>

<span data-ttu-id="196a4-110">**\_ \_ \_ Handle proprietà matrice di oggetti EC \_**</span><span class="sxs-lookup"><span data-stu-id="196a4-110">**EC\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="196a4-111">Handle per una matrice di valori di proprietà per le origini eventi di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="196a4-111">Handle to an array of property values for the event sources of a subscription.</span></span> <span data-ttu-id="196a4-112">L'handle di matrice viene restituito dal metodo [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) quando il valore **EcSubscriptionEventSources** viene passato nel parametro *PropertyId* .</span><span class="sxs-lookup"><span data-stu-id="196a4-112">The array handle is returned by the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) method when the **EcSubscriptionEventSources** value is passed into the *PropertyId* parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="196a4-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="196a4-113">Requirements</span></span>



| <span data-ttu-id="196a4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="196a4-114">Requirement</span></span> | <span data-ttu-id="196a4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="196a4-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="196a4-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="196a4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="196a4-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="196a4-117">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="196a4-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="196a4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="196a4-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="196a4-119">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="196a4-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="196a4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="196a4-121"><dt>Evcoll. h</dt></span><span class="sxs-lookup"><span data-stu-id="196a4-121"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





