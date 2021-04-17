---
description: L'evento ReadyStateChange viene inviato quando viene modificata la proprietà ReadyState del controllo MSWebDVD.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522049"
---
# <a name="readystatechange"></a><span data-ttu-id="23e7e-103">ReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="23e7e-103">ReadyStateChange</span></span>

> [!Note]  
> <span data-ttu-id="23e7e-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="23e7e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="23e7e-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="23e7e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="23e7e-106">L' `ReadyStateChange` evento viene inviato quando la proprietà **ReadyState** del controllo mswebdvd è cambiata.</span><span class="sxs-lookup"><span data-stu-id="23e7e-106">The `ReadyStateChange` event is sent when the **ReadyState** property of the MSWebDVD control has changed.</span></span>

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a><span data-ttu-id="23e7e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="23e7e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23e7e-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span><span class="sxs-lookup"><span data-stu-id="23e7e-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span></span>
</dt> <dd>

<span data-ttu-id="23e7e-109">Specifica il nuovo valore della proprietà [**ReadyState**](readystate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="23e7e-109">Specifies the new value of the [**ReadyState**](readystate-property.md) property.</span></span>



| <span data-ttu-id="23e7e-110">Valore</span><span class="sxs-lookup"><span data-stu-id="23e7e-110">Value</span></span> | <span data-ttu-id="23e7e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23e7e-111">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="23e7e-112">0</span><span class="sxs-lookup"><span data-stu-id="23e7e-112">0</span></span>     | <span data-ttu-id="23e7e-113">READYSTATE non \_ inizializzato</span><span class="sxs-lookup"><span data-stu-id="23e7e-113">READYSTATE\_UNINITIALIZED</span></span> |
| <span data-ttu-id="23e7e-114">1</span><span class="sxs-lookup"><span data-stu-id="23e7e-114">1</span></span>     | <span data-ttu-id="23e7e-115">\_caricamento readyState</span><span class="sxs-lookup"><span data-stu-id="23e7e-115">READYSTATE\_LOADING</span></span>       |
| <span data-ttu-id="23e7e-116">2</span><span class="sxs-lookup"><span data-stu-id="23e7e-116">2</span></span>     | <span data-ttu-id="23e7e-117">READYSTATE \_ caricato</span><span class="sxs-lookup"><span data-stu-id="23e7e-117">READYSTATE\_LOADED</span></span>        |
| <span data-ttu-id="23e7e-118">3</span><span class="sxs-lookup"><span data-stu-id="23e7e-118">3</span></span>     | <span data-ttu-id="23e7e-119">READYSTATE \_ interattivo</span><span class="sxs-lookup"><span data-stu-id="23e7e-119">READYSTATE\_INTERACTIVE</span></span>   |
| <span data-ttu-id="23e7e-120">4</span><span class="sxs-lookup"><span data-stu-id="23e7e-120">4</span></span>     | <span data-ttu-id="23e7e-121">READYSTATE \_ completata</span><span class="sxs-lookup"><span data-stu-id="23e7e-121">READYSTATE\_COMPLETE</span></span>      |



 

</dd> </dl>

 

 



