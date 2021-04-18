---
description: La proprietà ReadyState Recupera il ReadyState dell'oggetto MSWebDVD.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Proprietà ReadyState (ocidl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326989"
---
# <a name="readystate-property"></a><span data-ttu-id="e3afb-103">Proprietà ReadyState</span><span class="sxs-lookup"><span data-stu-id="e3afb-103">ReadyState Property</span></span>

> [!Note]  
> <span data-ttu-id="e3afb-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e3afb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e3afb-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e3afb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e3afb-106">La `ReadyState` proprietà recupera il readyState dell'oggetto **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="e3afb-106">The `ReadyState` property retrieves the ReadyState of the **MSWebDVD** object.</span></span>

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a><span data-ttu-id="e3afb-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3afb-107">Return Value</span></span>

<span data-ttu-id="e3afb-108">Restituisce un valore intero che rappresenta il ReadyState del controllo.</span><span class="sxs-lookup"><span data-stu-id="e3afb-108">Returns an integer value representing the control's ReadyState.</span></span>



| <span data-ttu-id="e3afb-109">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e3afb-109">Return code</span></span> | <span data-ttu-id="e3afb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3afb-110">Description</span></span>                                               |
|-------------|-----------------------------------------------------------|
| <span data-ttu-id="e3afb-111">0</span><span class="sxs-lookup"><span data-stu-id="e3afb-111">0</span></span>           | <span data-ttu-id="e3afb-112">Stato di inizializzazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="e3afb-112">Default initialization state.</span></span>                             |
| <span data-ttu-id="e3afb-113">1</span><span class="sxs-lookup"><span data-stu-id="e3afb-113">1</span></span>           | <span data-ttu-id="e3afb-114">È in corso il caricamento delle proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e3afb-114">Object is loading its properties.</span></span>                         |
| <span data-ttu-id="e3afb-115">2</span><span class="sxs-lookup"><span data-stu-id="e3afb-115">2</span></span>           | <span data-ttu-id="e3afb-116">L'oggetto è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="e3afb-116">Object has been initialized.</span></span>                              |
| <span data-ttu-id="e3afb-117">3</span><span class="sxs-lookup"><span data-stu-id="e3afb-117">3</span></span>           | <span data-ttu-id="e3afb-118">L'oggetto è interattivo, ma non tutti i relativi dati sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="e3afb-118">Object is interactive, but not all its data is available.</span></span> |
| <span data-ttu-id="e3afb-119">4</span><span class="sxs-lookup"><span data-stu-id="e3afb-119">4</span></span>           | <span data-ttu-id="e3afb-120">L'oggetto ha ricevuto tutti i dati.</span><span class="sxs-lookup"><span data-stu-id="e3afb-120">Object has received all its data.</span></span>                         |



 

## <a name="remarks"></a><span data-ttu-id="e3afb-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3afb-121">Remarks</span></span>

<span data-ttu-id="e3afb-122">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e3afb-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="e3afb-123">Qualsiasi oggetto incorporato in una pagina Web espone la `ReadyState` Proprietà.</span><span class="sxs-lookup"><span data-stu-id="e3afb-123">Any object embedded in a Web page exposes the `ReadyState` property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3afb-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3afb-124">Requirements</span></span>



| <span data-ttu-id="e3afb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3afb-125">Requirement</span></span> | <span data-ttu-id="e3afb-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e3afb-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3afb-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3afb-127">Header</span></span><br/> | <dl> <span data-ttu-id="e3afb-128"><dt>Ocidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3afb-128"><dt>Ocidl.h</dt></span></span> </dl> |



 

 




