---
description: Contiene i metodi utilizzati per negoziare il tipo di token utilizzato per l'autenticazione dell'endpoint di un servizio.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Interfaccia IUpdateEndpointAuthProvider (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 071bc23bdf9d67412fef561c71e17fe81485984f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526683"
---
# <a name="iupdateendpointauthprovider-interface"></a><span data-ttu-id="5538e-103">Interfaccia IUpdateEndpointAuthProvider</span><span class="sxs-lookup"><span data-stu-id="5538e-103">IUpdateEndpointAuthProvider interface</span></span>

<span data-ttu-id="5538e-104">L'interfaccia **IUpdateEndpointAuthProvider** contiene i metodi usati per negoziare il tipo di token usato per autenticare l'endpoint di un servizio.</span><span class="sxs-lookup"><span data-stu-id="5538e-104">The **IUpdateEndpointAuthProvider** interface contains the methods used for negotiating which type of token is used for authenticating the endpoint of a service.</span></span>

## <a name="members"></a><span data-ttu-id="5538e-105">Membri</span><span class="sxs-lookup"><span data-stu-id="5538e-105">Members</span></span>

<span data-ttu-id="5538e-106">L'interfaccia **IUpdateEndpointAuthProvider** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5538e-106">The **IUpdateEndpointAuthProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5538e-107">**IUpdateEndpointAuthProvider** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5538e-107">**IUpdateEndpointAuthProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="5538e-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="5538e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5538e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="5538e-109">Methods</span></span>

<span data-ttu-id="5538e-110">L'interfaccia **IUpdateEndpointAuthProvider** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5538e-110">The **IUpdateEndpointAuthProvider** interface has these methods.</span></span>



| <span data-ttu-id="5538e-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="5538e-111">Method</span></span>                                                                                             | <span data-ttu-id="5538e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5538e-112">Description</span></span>                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5538e-113">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="5538e-113">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)                           | <span data-ttu-id="5538e-114">Richiedere un token per l'endpoint del servizio usando le credenziali specificate.</span><span class="sxs-lookup"><span data-stu-id="5538e-114">Request a token for the endpoint of the service using the specified credentials.</span></span><br/>    |
| [<span data-ttu-id="5538e-115">**GetPreferredEndpointTokenType**</span><span class="sxs-lookup"><span data-stu-id="5538e-115">**GetPreferredEndpointTokenType**</span></span>](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | <span data-ttu-id="5538e-116">Restituisce il tipo preferito di token di autenticazione per l'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="5538e-116">Returns the preferred type of authentication token for the endpoint of the service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5538e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5538e-117">Remarks</span></span>

<span data-ttu-id="5538e-118">WUA chiama il metodo [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) di questa interfaccia per avviare il processo di negoziazione.</span><span class="sxs-lookup"><span data-stu-id="5538e-118">WUA calls the [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) method of this interface to start the negotiation process.</span></span> <span data-ttu-id="5538e-119">Quando viene effettuata la chiamata, WUA passa l'identificatore del servizio, il tipo di endpoint implementato dal servizio e i tipi di token disponibili.</span><span class="sxs-lookup"><span data-stu-id="5538e-119">When the call is made WUA passes in the service identifier, the type of endpoint implemented by the service, and the token types that are available.</span></span> <span data-ttu-id="5538e-120">L'implementazione di questa interfaccia restituisce quindi i tipi di token che preferisce usare.</span><span class="sxs-lookup"><span data-stu-id="5538e-120">The implementation of this interface then returns the token types that it preferes to use.</span></span>

## <a name="requirements"></a><span data-ttu-id="5538e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5538e-121">Requirements</span></span>



| <span data-ttu-id="5538e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5538e-122">Requirement</span></span> | <span data-ttu-id="5538e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5538e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5538e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5538e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5538e-125">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="5538e-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="5538e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5538e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5538e-127">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="5538e-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="5538e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5538e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5538e-129"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="5538e-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="5538e-130">IDL</span><span class="sxs-lookup"><span data-stu-id="5538e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5538e-131"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5538e-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="5538e-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="5538e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5538e-133"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5538e-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="5538e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5538e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5538e-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5538e-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
