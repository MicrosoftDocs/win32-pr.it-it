---
description: Richiedere un token per l'endpoint del servizio usando le credenziali specificate.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'Metodo IUpdateEndpointAuthProvider:: GetEndpointToken (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752079"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a><span data-ttu-id="c7fbc-103">Metodo IUpdateEndpointAuthProvider:: GetEndpointToken</span><span class="sxs-lookup"><span data-stu-id="c7fbc-103">IUpdateEndpointAuthProvider::GetEndpointToken method</span></span>

<span data-ttu-id="c7fbc-104">Richiedere un token per l'endpoint del servizio usando le credenziali specificate.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-104">Request a token for the endpoint of the service using the specified credentials.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fbc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7fbc-105">Syntax</span></span>


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a><span data-ttu-id="c7fbc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7fbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7fbc-107">*ServiceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fbc-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fbc-108">Identifica il servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="c7fbc-109">*EndpointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fbc-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fbc-110">Identifica il tipo di endpoint implementato dal servizio.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-110">Identifies the type of endpoint that is implemented by the service.</span></span>

</dd> <dt>

<span data-ttu-id="c7fbc-111">*proxySettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fbc-111">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fbc-112">Impostazioni da utilizzare per la connessione a un server proxy.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-112">The settings to be used when connecting to a proxy server.</span></span> <span data-ttu-id="c7fbc-113">Per ulteriori informazioni, vedere la struttura [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) .</span><span class="sxs-lookup"><span data-stu-id="c7fbc-113">See the [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) structure for more details.</span></span>

</dd> <dt>

<span data-ttu-id="c7fbc-114">*hUserToken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fbc-114">*hUserToken* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c7fbc-115">*TokenType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fbc-115">*tokenType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fbc-116">Identifica il tipo di token di autenticazione utilizzato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-116">Identifies the type of authentication token that is used for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="c7fbc-117">*fRefreshOnline* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fbc-117">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fbc-118">Indica che WUA Weather richiede un nuovo token.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-118">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="c7fbc-119">True indica che è richiesto un nuovo token.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-119">True indicates that a new token is requested.</span></span> <span data-ttu-id="c7fbc-120">False indica che è richiesto un token nuovo o memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-120">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="c7fbc-121">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-121">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="c7fbc-122">*ppEndpointToken* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c7fbc-122">*ppEndpointToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fbc-123">Specificare il token dell'endpoint da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-123">Specifiy the endpoint token to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7fbc-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7fbc-124">Return value</span></span>

<span data-ttu-id="c7fbc-125">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-125">Returns S\_OK if successful.</span></span> <span data-ttu-id="c7fbc-126">In caso contrario, restituisce un codice di errore COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-126">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7fbc-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7fbc-127">Remarks</span></span>

<span data-ttu-id="c7fbc-128">WUA imposta in genere il parametro fRefreshOnline su false quando il metodo viene chiamato per la prima volta, quindi se si verifica un errore di connessione WUA imposta tale parametro su true quando il metodo viene chiamato nuovamente.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-128">WUA typically sets the fRefreshOnline parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="c7fbc-129">Tuttavia, l'implementazione di questo metodo può richiedere un nuovo token da un servizio token di sicurezza (STS) o fornire un token memorizzato nella cache in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-129">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fbc-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7fbc-130">Requirements</span></span>



| <span data-ttu-id="c7fbc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7fbc-131">Requirement</span></span> | <span data-ttu-id="c7fbc-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c7fbc-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fbc-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7fbc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c7fbc-134">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c7fbc-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="c7fbc-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7fbc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c7fbc-136">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c7fbc-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="c7fbc-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7fbc-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7fbc-138"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7fbc-138"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7fbc-139">IDL</span><span class="sxs-lookup"><span data-stu-id="c7fbc-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7fbc-140"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7fbc-140"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7fbc-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="c7fbc-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7fbc-142"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7fbc-142"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="c7fbc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c7fbc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7fbc-144"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7fbc-144"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fbc-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7fbc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fbc-146">**IUpdateEndpointAuthProvider**</span><span class="sxs-lookup"><span data-stu-id="c7fbc-146">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




