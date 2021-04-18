---
title: Metodo IWMDRMSecurity GetContentEnablersForRevocations (wmdrmsdk. h)
description: Il metodo GetContentEnablersForRevocations recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati revocati.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Metodo GetContentEnablersForRevocations Windows Media Format
- Metodo GetContentEnablersForRevocations Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetContentEnablersForRevocations
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327461"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a><span data-ttu-id="5ba76-106">Metodo IWMDRMSecurity:: GetContentEnablersForRevocations</span><span class="sxs-lookup"><span data-stu-id="5ba76-106">IWMDRMSecurity::GetContentEnablersForRevocations method</span></span>

<span data-ttu-id="5ba76-107">Il metodo **GetContentEnablersForRevocations** recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati revocati.</span><span class="sxs-lookup"><span data-stu-id="5ba76-107">The **GetContentEnablersForRevocations** method retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ba76-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ba76-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="5ba76-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ba76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ba76-110">*rgpbCerts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ba76-110">*rgpbCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba76-111">Matrice di certificati per cui recuperare gli abilitatori del contenuto.</span><span class="sxs-lookup"><span data-stu-id="5ba76-111">Array of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="5ba76-112">Il numero di elementi nella matrice deve essere specificato da *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="5ba76-112">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="5ba76-113">*rgpdwCertSizes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ba76-113">*rgpdwCertSizes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba76-114">Matrice contenente le dimensioni dei certificati nella matrice *rgpbCerts* .</span><span class="sxs-lookup"><span data-stu-id="5ba76-114">Array containing the sizes of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="5ba76-115">Il numero di elementi nella matrice deve essere specificato da *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="5ba76-115">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="5ba76-116">*rgpguidCerts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ba76-116">*rgpguidCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba76-117">Matrice contenente i tipi di certificati nella matrice *rgpbCerts* .</span><span class="sxs-lookup"><span data-stu-id="5ba76-117">Array containing the types of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="5ba76-118">Il numero di elementi nella matrice deve essere specificato da *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="5ba76-118">The number of elements in the array must be specified by *cCerts*.</span></span> <span data-ttu-id="5ba76-119">Per ogni elemento della matrice, usare uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5ba76-119">For each element of the array, use one of the following values.</span></span>



| <span data-ttu-id="5ba76-120">Costante GUID</span><span class="sxs-lookup"><span data-stu-id="5ba76-120">GUID constant</span></span>                 | <span data-ttu-id="5ba76-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ba76-121">Description</span></span>                                                    |
|-------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5ba76-122">\_app WMDRM REVOCATIONTYPE \_</span><span class="sxs-lookup"><span data-stu-id="5ba76-122">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="5ba76-123">Specifica un certificato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5ba76-123">Specifies an application certificate.</span></span>                          |
| <span data-ttu-id="5ba76-124">\_dispositivo REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="5ba76-124">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="5ba76-125">Specifica un certificato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5ba76-125">Specifies a device certificate.</span></span>                                |
| <span data-ttu-id="5ba76-126">WMDRM \_ REVOCATIONTYPE \_ Cardea</span><span class="sxs-lookup"><span data-stu-id="5ba76-126">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="5ba76-127">Specifica un certificato Windows Media DRM per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="5ba76-127">Specifies a Windows Media DRM for Network Devices certificate.</span></span> |



 

</dd> <dt>

<span data-ttu-id="5ba76-128">*cCerts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ba76-128">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba76-129">Numero di certificati per i quali recuperare gli abilitatori del contenuto.</span><span class="sxs-lookup"><span data-stu-id="5ba76-129">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="5ba76-130">Questo è il numero di elementi nella matrice *rgpbCerts* , la matrice *rgpdwCertSizes* e la matrice *rgpguidCerts* .</span><span class="sxs-lookup"><span data-stu-id="5ba76-130">This is the number of elements in the *rgpbCerts* array, the *rgpdwCertSizes* array, and the *rgpguidCerts* array.</span></span>

</dd> <dt>

<span data-ttu-id="5ba76-131">*hResultHint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ba76-131">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba76-132">Valore restituito ricevuto dall'operazione non riuscita a causa di un certificato revocato.</span><span class="sxs-lookup"><span data-stu-id="5ba76-132">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="5ba76-133">Se non si chiama in risposta a una chiamata al metodo non riuscita, impostare su S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ba76-133">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="5ba76-134">*prgContentEnablers* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5ba76-134">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba76-135">Matrice che riceve gli indirizzi delle interfacce **IMFContentEnabler** appena create.</span><span class="sxs-lookup"><span data-stu-id="5ba76-135">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="5ba76-136">Impostare su **null** per ottenere il numero di abilitatori del contenuto nel parametro *pcContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="5ba76-136">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5ba76-137">*pcContentEnablers* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5ba76-137">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba76-138">Numero di elementi nella matrice *prgContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="5ba76-138">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="5ba76-139">Se *prgContentEnablers* è **null**, questo valore viene impostato sul numero di abilitatori di contenuto necessari nell'output.</span><span class="sxs-lookup"><span data-stu-id="5ba76-139">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ba76-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ba76-140">Return value</span></span>

<span data-ttu-id="5ba76-141">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5ba76-141">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5ba76-142">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5ba76-142">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5ba76-143">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5ba76-143">Return code</span></span>                                                                          | <span data-ttu-id="5ba76-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ba76-144">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5ba76-145"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba76-145"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5ba76-146">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5ba76-146">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ba76-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ba76-147">Remarks</span></span>

<span data-ttu-id="5ba76-148">Se si utilizza l'interfaccia **IMFContentEnabler** per rinnovare i componenti revocati, è necessario chiarire il processo all'utente.</span><span class="sxs-lookup"><span data-stu-id="5ba76-148">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="5ba76-149">Questo chiarimento deve essere effettuato perché il processo di aggiornamento Invia le informazioni dal computer client a un sito Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5ba76-149">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="5ba76-150">Quando si chiama **IMFContentEnabler:: AutomaticEnable**, l'attivatore del contenuto avvia il browser predefinito con l'indirizzo del servizio di aggiornamento sul sito Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5ba76-150">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="5ba76-151">Un identificatore univoco che identifica il componente revocato viene inviato al servizio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5ba76-151">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="5ba76-152">Il servizio reindirizza quindi il browser a una pagina Web da cui l'utente potrebbe essere in grado di scaricare e installare la nuova versione del componente revocato.</span><span class="sxs-lookup"><span data-stu-id="5ba76-152">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ba76-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ba76-153">Requirements</span></span>



| <span data-ttu-id="5ba76-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ba76-154">Requirement</span></span> | <span data-ttu-id="5ba76-155">Valore</span><span class="sxs-lookup"><span data-stu-id="5ba76-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ba76-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ba76-156">Header</span></span><br/>  | <dl> <span data-ttu-id="5ba76-157"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ba76-157"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ba76-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ba76-158">Library</span></span><br/> | <dl> <span data-ttu-id="5ba76-159"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ba76-159"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ba76-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ba76-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ba76-161">**Revoca e rinnovo automatici dei componenti**</span><span class="sxs-lookup"><span data-stu-id="5ba76-161">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="5ba76-162">**Interfaccia IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="5ba76-162">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





