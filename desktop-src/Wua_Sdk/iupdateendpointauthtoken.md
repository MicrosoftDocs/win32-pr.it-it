---
description: Fornisce i metodi che WUA può utilizzare per raccogliere informazioni sul token dell'endpoint.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interfaccia IUpdateEndpointAuthToken (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485140"
---
# <a name="iupdateendpointauthtoken-interface"></a><span data-ttu-id="62935-103">Interfaccia IUpdateEndpointAuthToken</span><span class="sxs-lookup"><span data-stu-id="62935-103">IUpdateEndpointAuthToken interface</span></span>

<span data-ttu-id="62935-104">Fornisce i metodi che WUA può utilizzare per raccogliere informazioni sul token dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="62935-104">Provides the methods that WUA can use to gather information about the endpoint token.</span></span>

## <a name="members"></a><span data-ttu-id="62935-105">Membri</span><span class="sxs-lookup"><span data-stu-id="62935-105">Members</span></span>

<span data-ttu-id="62935-106">L'interfaccia **IUpdateEndpointAuthToken** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="62935-106">The **IUpdateEndpointAuthToken** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="62935-107">**IUpdateEndpointAuthToken** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="62935-107">**IUpdateEndpointAuthToken** also has these types of members:</span></span>

-   [<span data-ttu-id="62935-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="62935-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="62935-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="62935-109">Methods</span></span>

<span data-ttu-id="62935-110">L'interfaccia **IUpdateEndpointAuthToken** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="62935-110">The **IUpdateEndpointAuthToken** interface has these methods.</span></span>



| <span data-ttu-id="62935-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="62935-111">Method</span></span>                                                                                | <span data-ttu-id="62935-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62935-112">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62935-113">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="62935-113">**ServiceID**</span></span>](iupdateendpointauthtoken-serviceid.md)                               | <span data-ttu-id="62935-114">Ottiene l'identificatore del servizio da autenticare.</span><span class="sxs-lookup"><span data-stu-id="62935-114">Gets the identifier of the service to be authenticated.</span></span><br/>                                                          |
| [<span data-ttu-id="62935-115">**SigningKey**</span><span class="sxs-lookup"><span data-stu-id="62935-115">**SigningKey**</span></span>](iupdateendpointauthtoken-signingkey.md)                             | <span data-ttu-id="62935-116">Ottiene la chiave utilizzata per firmare i messaggi in uscita tra il computer client e sercvice.</span><span class="sxs-lookup"><span data-stu-id="62935-116">Gets the key used to sign outgoing messages between the client computer and the sercvice.</span></span><br/>                        |
| [<span data-ttu-id="62935-117">**TokenData**</span><span class="sxs-lookup"><span data-stu-id="62935-117">**TokenData**</span></span>](iupdateendpointauthtoken-tokendata.md)                               | <span data-ttu-id="62935-118">Ottiene i dati XML (inviati in rete) che rappresenta il token.</span><span class="sxs-lookup"><span data-stu-id="62935-118">Gets the XML data (sent over the wire) that represents the token.</span></span> <br/>                                               |
| [<span data-ttu-id="62935-119">**TokenReferenceAttached**</span><span class="sxs-lookup"><span data-stu-id="62935-119">**TokenReferenceAttached**</span></span>](iupdateendpointauthtoken-tokenreferenceattached.md)     | <span data-ttu-id="62935-120">Ottiene il formato XML di un riferimento associato al token.</span><span class="sxs-lookup"><span data-stu-id="62935-120">Gets the XML format of an attached reference to the token.</span></span><br/>                                                       |
| [<span data-ttu-id="62935-121">**TokenReferenceUnattached**</span><span class="sxs-lookup"><span data-stu-id="62935-121">**TokenReferenceUnattached**</span></span>](iupdateendpointauthtoken-tokenreferenceunattached.md) | <span data-ttu-id="62935-122">Ottiene il formato XML di un riferimento non associato al token.</span><span class="sxs-lookup"><span data-stu-id="62935-122">Gets the XML format of an unattached reference to the token.</span></span><br/>                                                     |
| [<span data-ttu-id="62935-123">**TokenType**</span><span class="sxs-lookup"><span data-stu-id="62935-123">**TokenType**</span></span>](iupdateendpointauthtoken-tokentype.md)                               | <span data-ttu-id="62935-124">Ottiene il tipo del token dell'endpoint, ad esempio un token WS-Security SAML (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="62935-124">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="62935-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62935-125">Requirements</span></span>



| <span data-ttu-id="62935-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="62935-126">Requirement</span></span> | <span data-ttu-id="62935-127">Valore</span><span class="sxs-lookup"><span data-stu-id="62935-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62935-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62935-128">Minimum supported client</span></span><br/> | <span data-ttu-id="62935-129">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="62935-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="62935-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62935-130">Minimum supported server</span></span><br/> | <span data-ttu-id="62935-131">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="62935-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="62935-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62935-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="62935-133"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="62935-133"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="62935-134">IDL</span><span class="sxs-lookup"><span data-stu-id="62935-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62935-135"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62935-135"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="62935-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="62935-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="62935-137"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62935-137"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="62935-138">DLL</span><span class="sxs-lookup"><span data-stu-id="62935-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62935-139"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62935-139"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
