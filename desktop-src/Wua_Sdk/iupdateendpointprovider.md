---
description: Contiene il metodo utilizzato per ottenere un endpoint utilizzato per connettersi a un servizio.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Interfaccia IUpdateEndpointProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307614"
---
# <a name="iupdateendpointprovider-interface"></a><span data-ttu-id="6aeba-103">Interfaccia IUpdateEndpointProvider</span><span class="sxs-lookup"><span data-stu-id="6aeba-103">IUpdateEndpointProvider interface</span></span>

<span data-ttu-id="6aeba-104">Contiene il metodo utilizzato per ottenere un endpoint utilizzato per connettersi a un servizio.</span><span class="sxs-lookup"><span data-stu-id="6aeba-104">Contains the method used to get an endpoint that is used to connect to a service.</span></span> <span data-ttu-id="6aeba-105">Questa interfaccia viene implementata quando si scrive un provider di endpoint.</span><span class="sxs-lookup"><span data-stu-id="6aeba-105">This interface is implemented when writing an endpoint provider.</span></span>

## <a name="members"></a><span data-ttu-id="6aeba-106">Membri</span><span class="sxs-lookup"><span data-stu-id="6aeba-106">Members</span></span>

<span data-ttu-id="6aeba-107">L'interfaccia **IUpdateEndpointProvider** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6aeba-107">The **IUpdateEndpointProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6aeba-108">**IUpdateEndpointProvider** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6aeba-108">**IUpdateEndpointProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="6aeba-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="6aeba-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6aeba-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6aeba-110">Methods</span></span>

<span data-ttu-id="6aeba-111">L'interfaccia **IUpdateEndpointProvider** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6aeba-111">The **IUpdateEndpointProvider** interface has these methods.</span></span>



| <span data-ttu-id="6aeba-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="6aeba-112">Method</span></span>                                                                       | <span data-ttu-id="6aeba-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6aeba-113">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="6aeba-114">**Getserviceendpoint**</span><span class="sxs-lookup"><span data-stu-id="6aeba-114">**GetServiceEndpoint**</span></span>](iupdateendpointauthprovider-getserviceendpoint.md) | <span data-ttu-id="6aeba-115">Richiede un endpoint utilizzato per connettersi a un servizio.</span><span class="sxs-lookup"><span data-stu-id="6aeba-115">Requests an endpoint that is used to connect to a service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6aeba-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6aeba-116">Remarks</span></span>

<span data-ttu-id="6aeba-117">WUA chiama il metodo [**getserviceendpoint**](iupdateendpointauthprovider-getserviceendpoint.md) per avviare il processo di negoziazione.</span><span class="sxs-lookup"><span data-stu-id="6aeba-117">WUA calls the [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) method to start the negotiation process.</span></span> <span data-ttu-id="6aeba-118">Quando viene effettuata la chiamata, WUA passa i tipi di token registrati e l'implementazione di questa interfaccia restituisce i tipi di token che preferisce usare.</span><span class="sxs-lookup"><span data-stu-id="6aeba-118">When the call is made, WUA passes in the registered token types, and the implementation of this interface returns the token types that it prefers to use.</span></span>

 

 
