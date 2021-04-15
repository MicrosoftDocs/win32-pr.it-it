---
title: CENUMVAR. CPP
description: Nel componente provider di esempio, l'implementazione di base per le classi derivate xxxEnumVariant si trova in cenumvar. cpp. I metodi associati sono elencati nella tabella seguente.
ms.assetid: 6b38bc99-25d4-40af-863a-9cc37f786d9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d361cb7d3e2657a31645fba05aa2e1a23762a3fc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339214"
---
# <a name="cenumvarcpp"></a><span data-ttu-id="d6c63-104">CENUMVAR. CPP</span><span class="sxs-lookup"><span data-stu-id="d6c63-104">CENUMVAR.CPP</span></span>

<span data-ttu-id="d6c63-105">Nel componente provider di esempio, l'implementazione di base per le classi derivate xxxEnumVariant si trova in cenumvar. cpp.</span><span class="sxs-lookup"><span data-stu-id="d6c63-105">In the example provider component, the base implementation for xxxEnumVariant derived classes can be found in cenumvar.cpp.</span></span> <span data-ttu-id="d6c63-106">I metodi associati sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d6c63-106">Associated methods are listed in the following table.</span></span>



| <span data-ttu-id="d6c63-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="d6c63-107">Method</span></span>                                          | <span data-ttu-id="d6c63-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6c63-108">Description</span></span>                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c63-109">**CSampleDSEnumVariant::CSampleDSEnumVariant**</span><span class="sxs-lookup"><span data-stu-id="d6c63-109">**CSampleDSEnumVariant::CSampleDSEnumVariant**</span></span>  | <span data-ttu-id="d6c63-110">Costruttore standard.</span><span class="sxs-lookup"><span data-stu-id="d6c63-110">Standard constructor.</span></span>                                                                 |
| <span data-ttu-id="d6c63-111">**CSampleDSEnumVariant:: ~ CSampleDSEnumVariant**</span><span class="sxs-lookup"><span data-stu-id="d6c63-111">**CSampleDSEnumVariant::~CSampleDSEnumVariant**</span></span> | <span data-ttu-id="d6c63-112">Distruttore standard.</span><span class="sxs-lookup"><span data-stu-id="d6c63-112">Standard destructor.</span></span>                                                                  |
| <span data-ttu-id="d6c63-113">**CSampleDSEnumVariant:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="d6c63-113">**CSampleDSEnumVariant::QueryInterface**</span></span>        | <span data-ttu-id="d6c63-114">Implementazione standard di [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="d6c63-114">Standard [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) implementation.</span></span> |
| <span data-ttu-id="d6c63-115">**CSampleDSEnumVariant:: AddRef**</span><span class="sxs-lookup"><span data-stu-id="d6c63-115">**CSampleDSEnumVariant::AddRef**</span></span>                | <span data-ttu-id="d6c63-116">Implementazione standard di [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) .</span><span class="sxs-lookup"><span data-stu-id="d6c63-116">Standard [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) implementation.</span></span>                 |
| <span data-ttu-id="d6c63-117">**CSampleDSEnumVariant:: Release**</span><span class="sxs-lookup"><span data-stu-id="d6c63-117">**CSampleDSEnumVariant::Release**</span></span>               | <span data-ttu-id="d6c63-118">Implementazione standard di [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="d6c63-118">Standard [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) implementation.</span></span>               |
| <span data-ttu-id="d6c63-119">**CSampleDSEnumVariant:: Skip**</span><span class="sxs-lookup"><span data-stu-id="d6c63-119">**CSampleDSEnumVariant::Skip**</span></span>                  | <span data-ttu-id="d6c63-120">Implementazione standard di **IEnumXXXX:: Skip** .</span><span class="sxs-lookup"><span data-stu-id="d6c63-120">Standard **IEnumXXXX::Skip** implementation.</span></span>                                          |
| <span data-ttu-id="d6c63-121">**CSampleDSEnumVariant:: Reset**</span><span class="sxs-lookup"><span data-stu-id="d6c63-121">**CSampleDSEnumVariant::Reset**</span></span>                 | <span data-ttu-id="d6c63-122">Implementazione standard di **IEnumXXXX:: Reset** .</span><span class="sxs-lookup"><span data-stu-id="d6c63-122">Standard **IEnumXXXX::Reset** implementation.</span></span>                                         |
| <span data-ttu-id="d6c63-123">**CSampleDSEnumVariant:: Clone**</span><span class="sxs-lookup"><span data-stu-id="d6c63-123">**CSampleDSEnumVariant::Clone**</span></span>                 | <span data-ttu-id="d6c63-124">Implementazione standard di **IEnumXXXX:: Clone** .</span><span class="sxs-lookup"><span data-stu-id="d6c63-124">Standard **IEnumXXXX::Clone** implementation.</span></span>                                         |



 

 

 