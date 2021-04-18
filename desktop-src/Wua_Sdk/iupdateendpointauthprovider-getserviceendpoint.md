---
description: Richiede un endpoint utilizzato per connettersi a un servizio.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'Metodo IUpdateEndpointProvider:: getserviceendpoint (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307624"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a><span data-ttu-id="b48f1-103">Metodo IUpdateEndpointProvider:: getserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="b48f1-103">IUpdateEndpointProvider::GetServiceEndpoint method</span></span>

<span data-ttu-id="b48f1-104">Richiede un endpoint utilizzato per connettersi a un servizio.</span><span class="sxs-lookup"><span data-stu-id="b48f1-104">Requests an endpoint that is used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b48f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b48f1-105">Syntax</span></span>


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a><span data-ttu-id="b48f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b48f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b48f1-107">*ServiceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b48f1-107">*ServiceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b48f1-108">Identifica il servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="b48f1-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="b48f1-109">*EndpointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b48f1-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b48f1-110">Identifica il tipo di endpoint implementato dal servizio.</span><span class="sxs-lookup"><span data-stu-id="b48f1-110">Identifies the type of endpoint implemented by the service.</span></span>

<span data-ttu-id="b48f1-111">L'enumerazione [**UpdateEndpointType**](updateendpointtype.md) definisce le costanti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b48f1-111">The [**UpdateEndpointType**](updateendpointtype.md) enumeration defines the following constants.</span></span>

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span data-ttu-id="b48f1-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span><span class="sxs-lookup"><span data-stu-id="b48f1-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>


</dt> <dd>

<span data-ttu-id="b48f1-113">Endpoint client-server utilizzato per la connessione al servizio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b48f1-113">A client-server endpoint that is used to connect to the update service.</span></span>

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span data-ttu-id="b48f1-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span><span class="sxs-lookup"><span data-stu-id="b48f1-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>


</dt> <dd>

<span data-ttu-id="b48f1-115">Un endpoint di Reporting utilizzato quando il client segnala i risultati di analisi, download e installazioni di nuovo nel servizio di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b48f1-115">A Reporting endpoint that is used used when the client reports the results of scans, downloads, and installs back to the update service</span></span>

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span data-ttu-id="b48f1-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span><span class="sxs-lookup"><span data-stu-id="b48f1-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>


</dt> <dd>

<span data-ttu-id="b48f1-117">Un endpoint Self-Update utilizzato quando il computer client contatta un servizio di aggiornamento per verificare se è presente una nuova versione del software client di Windows Update Agent.</span><span class="sxs-lookup"><span data-stu-id="b48f1-117">A Self-Update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span data-ttu-id="b48f1-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span><span class="sxs-lookup"><span data-stu-id="b48f1-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>


</dt> <dd>

<span data-ttu-id="b48f1-119">Un endpoint del regolamento utilizzato quando il computer client contatta il servizio di regolamentazione per agire su un particolare aggiornamento applicabile al computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b48f1-119">A Regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span data-ttu-id="b48f1-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span><span class="sxs-lookup"><span data-stu-id="b48f1-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>


</dt> <dd>

<span data-ttu-id="b48f1-121">Un Simple-Targeting che viene utilizzato solo con servizi privati (server WSUS negli ambienti aziendali).</span><span class="sxs-lookup"><span data-stu-id="b48f1-121">A Simple-Targeting endoint that is used only with private services (WSUS servers in corporate environments).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b48f1-122">*proxySettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b48f1-122">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b48f1-123">Identifica le impostazioni utilizzate per la connessione a un server proxy.</span><span class="sxs-lookup"><span data-stu-id="b48f1-123">Identifies the settings that are used when connecting to a proxy server.</span></span>

</dd> <dt>

<span data-ttu-id="b48f1-124">*hUserToken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b48f1-124">*hUserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b48f1-125">Contiene un oggetto handle di token che rappresenta l'utente.</span><span class="sxs-lookup"><span data-stu-id="b48f1-125">Contains a token handle object that represents the user.</span></span> <span data-ttu-id="b48f1-126">Il provider di endpoint utilizza questo token per determinare quali impostazioni e credenziali del proxy utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b48f1-126">The endpoint provider uses this token to determine which proxy settings and credentials to use.</span></span>

</dd> <dt>

<span data-ttu-id="b48f1-127">*fRefreshOnline* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b48f1-127">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b48f1-128">Indica che WUA Weather richiede un nuovo token.</span><span class="sxs-lookup"><span data-stu-id="b48f1-128">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="b48f1-129">True indica che è richiesto un nuovo token.</span><span class="sxs-lookup"><span data-stu-id="b48f1-129">True indicates that a new token is requested.</span></span> <span data-ttu-id="b48f1-130">False indica che è richiesto un token nuovo o memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="b48f1-130">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="b48f1-131">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b48f1-131">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="b48f1-132">*pbstrEndpointLoc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b48f1-132">*pbstrEndpointLoc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b48f1-133">Specificare l'URL usato per comunicare con il servizio.</span><span class="sxs-lookup"><span data-stu-id="b48f1-133">Specify the URL used to communicate with the service.</span></span> <span data-ttu-id="b48f1-134">Per un endpoint sicuri-server, ad esempio, si tratta dell'URL del servizio server client.</span><span class="sxs-lookup"><span data-stu-id="b48f1-134">For example, for a cleint-server endpoint this would be the URL to the client server service.</span></span> <span data-ttu-id="b48f1-135">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b48f1-135">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b48f1-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b48f1-136">Return value</span></span>

<span data-ttu-id="b48f1-137">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b48f1-137">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="b48f1-138">In caso contrario, restituisce un codice di errore COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="b48f1-138">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b48f1-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="b48f1-139">Remarks</span></span>

<span data-ttu-id="b48f1-140">WUA imposta in genere il parametro *fRefreshOnline* su false quando il metodo viene chiamato per la prima volta, quindi se si verifica un errore di connessione WUA imposta tale parametro su true quando il metodo viene chiamato nuovamente.</span><span class="sxs-lookup"><span data-stu-id="b48f1-140">WUA typically sets the *fRefreshOnline* parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="b48f1-141">Tuttavia, l'implementazione di questo metodo può richiedere un nuovo token da un servizio token di sicurezza (STS) o fornire un token memorizzato nella cache in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="b48f1-141">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

<span data-ttu-id="b48f1-142">Se l'endpoint non richiede l'autenticazione, il chiamante può connettersi al servizio usando solo l'URL specificato dal parametro *pbstrEndpointLoc* .</span><span class="sxs-lookup"><span data-stu-id="b48f1-142">If the endpoint does not need authentication, then the caller can connect to the service using only the URL specified by the *pbstrEndpointLoc* parameter.</span></span>

<span data-ttu-id="b48f1-143">Se l'endpoint necessita di autenticazione, il chiamante può usare l'URL specificato dal parametro *pbstrEndpointLoc* e i dati forniti dagli altri parametri.</span><span class="sxs-lookup"><span data-stu-id="b48f1-143">If the endpoint does need authentication, then the caller can use the URL specified by the *pbstrEndpointLoc* parameter and the data provided by the other parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b48f1-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b48f1-144">Requirements</span></span>



| <span data-ttu-id="b48f1-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="b48f1-145">Requirement</span></span> | <span data-ttu-id="b48f1-146">Valore</span><span class="sxs-lookup"><span data-stu-id="b48f1-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b48f1-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b48f1-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b48f1-148">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="b48f1-148">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="b48f1-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b48f1-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b48f1-150">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="b48f1-150">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="b48f1-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b48f1-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="b48f1-152"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="b48f1-152"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="b48f1-153">IDL</span><span class="sxs-lookup"><span data-stu-id="b48f1-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b48f1-154"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b48f1-154"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="b48f1-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="b48f1-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="b48f1-156"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b48f1-156"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="b48f1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="b48f1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b48f1-158"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b48f1-158"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b48f1-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b48f1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48f1-160">**IUpdateEndpointProvider**</span><span class="sxs-lookup"><span data-stu-id="b48f1-160">**IUpdateEndpointProvider**</span></span>](iupdateendpointprovider.md)
</dt> </dl>

 

 




