---
description: Ottiene il formato XML di un riferimento non associato al token.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'Metodo IUpdateEndpointAuthToken:: TokenReferenceUnattached (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307616"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a><span data-ttu-id="a75c9-103">Metodo IUpdateEndpointAuthToken:: TokenReferenceUnattached</span><span class="sxs-lookup"><span data-stu-id="a75c9-103">IUpdateEndpointAuthToken::TokenReferenceUnattached method</span></span>

<span data-ttu-id="a75c9-104">Ottiene il formato XML di un riferimento non associato al token.</span><span class="sxs-lookup"><span data-stu-id="a75c9-104">Gets the XML format of an unattached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="a75c9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a75c9-105">Syntax</span></span>


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="a75c9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a75c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a75c9-107">*pszTokenReference* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a75c9-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a75c9-108">Puntatore al riferimento al token non collegato.</span><span class="sxs-lookup"><span data-stu-id="a75c9-108">Pointer to the unattached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a75c9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a75c9-109">Return value</span></span>

<span data-ttu-id="a75c9-110">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a75c9-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="a75c9-111">In caso contrario, restituisce un codice di errore COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="a75c9-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a75c9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a75c9-112">Remarks</span></span>

<span data-ttu-id="a75c9-113">Un riferimento non collegato fa riferimento a un Referece, ad esempio signiture che usa il token, che non è presente nel messaggio in cui risiede il token.</span><span class="sxs-lookup"><span data-stu-id="a75c9-113">An unattached reference refers a referece (such as the signiture that is using the token) that is not in the message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75c9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a75c9-114">Requirements</span></span>



| <span data-ttu-id="a75c9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a75c9-115">Requirement</span></span> | <span data-ttu-id="a75c9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a75c9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a75c9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a75c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a75c9-118">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="a75c9-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="a75c9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a75c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a75c9-120">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="a75c9-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a75c9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a75c9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a75c9-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="a75c9-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="a75c9-123">IDL</span><span class="sxs-lookup"><span data-stu-id="a75c9-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a75c9-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a75c9-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="a75c9-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="a75c9-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a75c9-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a75c9-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="a75c9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a75c9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a75c9-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a75c9-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a75c9-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a75c9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a75c9-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="a75c9-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




