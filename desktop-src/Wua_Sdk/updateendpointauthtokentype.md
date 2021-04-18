---
description: Definisce il tipo di token che è possibile utilizzare per l'autenticazione con un endpoint.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Enumerazione UpdateEndpointAuthTokenType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: c978841511b7cfff895a15936a41d169a8500927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305831"
---
# <a name="updateendpointauthtokentype-enumeration"></a><span data-ttu-id="6a0de-103">Enumerazione UpdateEndpointAuthTokenType</span><span class="sxs-lookup"><span data-stu-id="6a0de-103">UpdateEndpointAuthTokenType enumeration</span></span>

<span data-ttu-id="6a0de-104">Definisce il tipo di token che è possibile utilizzare per l'autenticazione con un endpoint.</span><span class="sxs-lookup"><span data-stu-id="6a0de-104">Defines the type of tokens that can be used for authenticating with an endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a0de-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a0de-105">Syntax</span></span>


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a><span data-ttu-id="6a0de-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="6a0de-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6a0de-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span><span class="sxs-lookup"><span data-stu-id="6a0de-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span></span>
</dt> <dd>

<span data-ttu-id="6a0de-108">Non è necessario alcun token di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="6a0de-108">No authentication token is needed.</span></span>

</dd> <dt>

<span data-ttu-id="6a0de-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span><span class="sxs-lookup"><span data-stu-id="6a0de-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span></span>
</dt> <dd>

<span data-ttu-id="6a0de-110">Il token di autenticazione per l'endpoint è un token WS-Security SAML (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="6a0de-110">The authentication token for the endpoint is a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a0de-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a0de-111">Requirements</span></span>



| <span data-ttu-id="6a0de-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a0de-112">Requirement</span></span> | <span data-ttu-id="6a0de-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6a0de-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a0de-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a0de-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6a0de-115">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6a0de-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="6a0de-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a0de-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6a0de-117">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6a0de-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6a0de-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a0de-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a0de-119"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a0de-119"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a0de-120">IDL</span><span class="sxs-lookup"><span data-stu-id="6a0de-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a0de-121"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a0de-121"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




