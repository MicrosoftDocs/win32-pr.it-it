---
description: Ottiene i dati XML (inviati in rete) che rappresenta il token.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'Metodo IUpdateEndpointAuthToken:: TokenData (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307620"
---
# <a name="iupdateendpointauthtokentokendata-method"></a><span data-ttu-id="5747c-103">Metodo IUpdateEndpointAuthToken:: TokenData</span><span class="sxs-lookup"><span data-stu-id="5747c-103">IUpdateEndpointAuthToken::TokenData method</span></span>

<span data-ttu-id="5747c-104">Ottiene i dati XML (inviati in rete) che rappresenta il token.</span><span class="sxs-lookup"><span data-stu-id="5747c-104">Gets the XML data (sent over the wire) that represents the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="5747c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5747c-105">Syntax</span></span>


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a><span data-ttu-id="5747c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5747c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5747c-107">*pszTokenData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5747c-107">*pszTokenData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5747c-108">Dati XML (inviati in rete) che rappresentano il token.</span><span class="sxs-lookup"><span data-stu-id="5747c-108">The XML data (sent over the wire) that represents the token.</span></span> <span data-ttu-id="5747c-109">Ad esempio, i dati per un token WS-Security SAML (Security Assertion Markup Language) 1,1 sono il codice SAML aggiunto alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="5747c-109">For example, the data for a WS-Security SAML (Security Assertion Markup Language) 1.1 token is the SAML code that is added to the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5747c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5747c-110">Return value</span></span>

<span data-ttu-id="5747c-111">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5747c-111">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="5747c-112">In caso contrario, restituisce un codice di errore COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="5747c-112">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5747c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5747c-113">Requirements</span></span>



| <span data-ttu-id="5747c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5747c-114">Requirement</span></span> | <span data-ttu-id="5747c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5747c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5747c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5747c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5747c-117">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="5747c-117">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="5747c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5747c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5747c-119">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="5747c-119">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="5747c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5747c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5747c-121"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="5747c-121"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="5747c-122">IDL</span><span class="sxs-lookup"><span data-stu-id="5747c-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5747c-123"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5747c-123"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="5747c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="5747c-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="5747c-125"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5747c-125"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="5747c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5747c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5747c-127"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5747c-127"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5747c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5747c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5747c-129">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="5747c-129">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




