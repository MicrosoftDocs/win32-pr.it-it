---
description: Ottiene l'identificatore del servizio da autenticare con il token dell'endpoint.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'Metodo IUpdateEndpointAuthToken:: ServiceID (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 8384baa0a4f8bb48e603e0f2f8bed417e783b7f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307622"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a><span data-ttu-id="df19b-103">Metodo IUpdateEndpointAuthToken:: ServiceID</span><span class="sxs-lookup"><span data-stu-id="df19b-103">IUpdateEndpointAuthToken::ServiceID method</span></span>

<span data-ttu-id="df19b-104">Ottiene l'identificatore del servizio da autenticare con il token dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="df19b-104">Gets the identifier of the service to be authenticated with the endpoint token.</span></span>

## <a name="syntax"></a><span data-ttu-id="df19b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df19b-105">Syntax</span></span>


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a><span data-ttu-id="df19b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df19b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df19b-107">*pServiceID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="df19b-107">*pServiceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df19b-108">Identificatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="df19b-108">The identifier of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df19b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df19b-109">Return value</span></span>

<span data-ttu-id="df19b-110">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="df19b-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="df19b-111">In caso contrario, restituisce un codice di errore COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="df19b-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="df19b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df19b-112">Requirements</span></span>



| <span data-ttu-id="df19b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="df19b-113">Requirement</span></span> | <span data-ttu-id="df19b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="df19b-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df19b-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df19b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="df19b-116">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="df19b-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="df19b-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df19b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="df19b-118">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="df19b-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="df19b-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df19b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="df19b-120"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="df19b-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="df19b-121">IDL</span><span class="sxs-lookup"><span data-stu-id="df19b-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="df19b-122"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="df19b-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="df19b-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="df19b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="df19b-124"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df19b-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="df19b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="df19b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df19b-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df19b-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df19b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df19b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df19b-128">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="df19b-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




