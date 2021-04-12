---
description: Ottiene il tipo del token dell'endpoint, ad esempio un token WS-Security SAML (Security Assertion Markup Language) 1,1.
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: 'Metodo IUpdateEndpointAuthToken:: TokenType (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bc2373c5dd49a3bf01d39b63360a3cf9df9f57d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526677"
---
# <a name="iupdateendpointauthtokentokentype-method"></a><span data-ttu-id="9783c-103">Metodo IUpdateEndpointAuthToken:: TokenType</span><span class="sxs-lookup"><span data-stu-id="9783c-103">IUpdateEndpointAuthToken::TokenType method</span></span>

<span data-ttu-id="9783c-104">Ottiene il tipo del token dell'endpoint, ad esempio un token WS-Security SAML (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="9783c-104">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

## <a name="syntax"></a><span data-ttu-id="9783c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9783c-105">Syntax</span></span>


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a><span data-ttu-id="9783c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9783c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9783c-107">*pTokenType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9783c-107">*pTokenType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9783c-108">Tipo del token dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="9783c-108">The type of the endpoint token.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9783c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9783c-109">Return value</span></span>

<span data-ttu-id="9783c-110">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9783c-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="9783c-111">In caso contrario, restituisce un codice di errore COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="9783c-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9783c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9783c-112">Requirements</span></span>



| <span data-ttu-id="9783c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9783c-113">Requirement</span></span> | <span data-ttu-id="9783c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9783c-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9783c-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9783c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9783c-116">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="9783c-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="9783c-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9783c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9783c-118">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="9783c-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="9783c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9783c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9783c-120"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="9783c-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="9783c-121">IDL</span><span class="sxs-lookup"><span data-stu-id="9783c-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9783c-122"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9783c-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="9783c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="9783c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9783c-124"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9783c-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="9783c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9783c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9783c-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9783c-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9783c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9783c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9783c-128">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="9783c-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




