---
description: Restituisce il tipo preferito di token di autenticazione per l'endpoint del servizio.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'Metodo IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226227"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a><span data-ttu-id="dcf36-103">Metodo IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType</span><span class="sxs-lookup"><span data-stu-id="dcf36-103">IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType method</span></span>

<span data-ttu-id="dcf36-104">Restituisce il tipo preferito di token di autenticazione per l'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="dcf36-104">Returns the preferred type of authentication token for the endpoint of the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcf36-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcf36-105">Syntax</span></span>


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a><span data-ttu-id="dcf36-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcf36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf36-107">*ServiceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcf36-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf36-108">Identifica il servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="dcf36-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="dcf36-109">*EndpointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcf36-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf36-110">Identifica il tipo di endpoint tneeded per la connessione al servizio.</span><span class="sxs-lookup"><span data-stu-id="dcf36-110">Identifies the type of endpoint tneeded to connect to the service.</span></span>

</dd> <dt>

<span data-ttu-id="dcf36-111">*ulRequestedTypes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcf36-111">*ulRequestedTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf36-112">Identifica il set di token ORed supportati dall'endpoint.</span><span class="sxs-lookup"><span data-stu-id="dcf36-112">Identifies the ORed set of tokens that are supported by the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="dcf36-113">*pulPreferredTokenTypes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dcf36-113">*pulPreferredTokenTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf36-114">Specificare il set di tipi di token di autenticazione ORed preferiti.</span><span class="sxs-lookup"><span data-stu-id="dcf36-114">Specify the ORed set of authentication token types that are preferred.</span></span> <span data-ttu-id="dcf36-115">(Impostare su 0 per indicare che non è necessario alcun token di autenticazione).</span><span class="sxs-lookup"><span data-stu-id="dcf36-115">(Set to 0 to indicate that no authentication token is needed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf36-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcf36-116">Return value</span></span>

<span data-ttu-id="dcf36-117">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="dcf36-117">Returns S\_OK if successful.</span></span> <span data-ttu-id="dcf36-118">In caso contrario, restituisce un codice di errore COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="dcf36-118">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcf36-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcf36-119">Remarks</span></span>

<span data-ttu-id="dcf36-120">Quando viene restituito questo metodo, WUA sceglie un tipo di token dai tipi preferiti e lo passa al parametro tokenType del metodo [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) .</span><span class="sxs-lookup"><span data-stu-id="dcf36-120">When this method is returned, WUA chooses a token type from the preferred types and passes it to the tokenType parameter of the [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcf36-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcf36-121">Requirements</span></span>



| <span data-ttu-id="dcf36-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf36-122">Requirement</span></span> | <span data-ttu-id="dcf36-123">Valore</span><span class="sxs-lookup"><span data-stu-id="dcf36-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf36-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcf36-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dcf36-125">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="dcf36-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="dcf36-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcf36-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dcf36-127">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="dcf36-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="dcf36-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcf36-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcf36-129"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcf36-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="dcf36-130">IDL</span><span class="sxs-lookup"><span data-stu-id="dcf36-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dcf36-131"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dcf36-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="dcf36-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="dcf36-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="dcf36-133"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcf36-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="dcf36-134">DLL</span><span class="sxs-lookup"><span data-stu-id="dcf36-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcf36-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcf36-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcf36-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcf36-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf36-137">**IUpdateEndpointAuthProvider**</span><span class="sxs-lookup"><span data-stu-id="dcf36-137">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> <dt>

[<span data-ttu-id="dcf36-138">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="dcf36-138">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




