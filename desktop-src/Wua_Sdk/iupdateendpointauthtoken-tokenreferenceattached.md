---
description: Ottiene il formato XML di un riferimento associato al token.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'Metodo IUpdateEndpointAuthToken:: TokenReferenceAttached (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307618"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a><span data-ttu-id="86d7a-103">Metodo IUpdateEndpointAuthToken:: TokenReferenceAttached</span><span class="sxs-lookup"><span data-stu-id="86d7a-103">IUpdateEndpointAuthToken::TokenReferenceAttached method</span></span>

<span data-ttu-id="86d7a-104">Ottiene il formato XML di un riferimento associato al token.</span><span class="sxs-lookup"><span data-stu-id="86d7a-104">Gets the XML format of an attached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="86d7a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86d7a-105">Syntax</span></span>


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="86d7a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86d7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86d7a-107">*pszTokenReference* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="86d7a-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86d7a-108">Puntatore al riferimento al token collegato.</span><span class="sxs-lookup"><span data-stu-id="86d7a-108">Pointer to the attached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86d7a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86d7a-109">Return value</span></span>

<span data-ttu-id="86d7a-110">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="86d7a-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="86d7a-111">In caso contrario, restituisce un codice di errore COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="86d7a-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="86d7a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="86d7a-112">Remarks</span></span>

<span data-ttu-id="86d7a-113">Un riferimento collegato fa riferimento a un Referece, ad esempio signiture che usa il token, che si trova nello stesso messaggio in cui risiede il token.</span><span class="sxs-lookup"><span data-stu-id="86d7a-113">An attached reference refers a referece (such as the signiture that is using the token) that is in the same message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="86d7a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86d7a-114">Requirements</span></span>



| <span data-ttu-id="86d7a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="86d7a-115">Requirement</span></span> | <span data-ttu-id="86d7a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="86d7a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86d7a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86d7a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="86d7a-118">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="86d7a-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="86d7a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86d7a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="86d7a-120">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="86d7a-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="86d7a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86d7a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="86d7a-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="86d7a-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="86d7a-123">IDL</span><span class="sxs-lookup"><span data-stu-id="86d7a-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="86d7a-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="86d7a-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="86d7a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="86d7a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="86d7a-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86d7a-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="86d7a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="86d7a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86d7a-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86d7a-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86d7a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86d7a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d7a-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="86d7a-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




