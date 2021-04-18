---
title: Metodo IWMDRMSecurity GetContentEnablersFromHashes (wmdrmsdk. h)
description: Il metodo GetContentEnablersFromHashes recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati con hash.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- Metodo GetContentEnablersFromHashes Windows Media Format
- Metodo GetContentEnablersFromHashes Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetContentEnablersFromHashes
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325539"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a><span data-ttu-id="ac07c-106">Metodo IWMDRMSecurity:: GetContentEnablersFromHashes</span><span class="sxs-lookup"><span data-stu-id="ac07c-106">IWMDRMSecurity::GetContentEnablersFromHashes method</span></span>

<span data-ttu-id="ac07c-107">Il metodo **GetContentEnablersFromHashes** recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati con hash.</span><span class="sxs-lookup"><span data-stu-id="ac07c-107">The **GetContentEnablersFromHashes** method retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac07c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac07c-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="ac07c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac07c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac07c-110">*rgpbCertHashes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac07c-110">*rgpbCertHashes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac07c-111">Matrice di hash del certificato per ottenere gli abilitatori del contenuto per.</span><span class="sxs-lookup"><span data-stu-id="ac07c-111">Array of certificate hashes to obtain content enablers for.</span></span>

</dd> <dt>

<span data-ttu-id="ac07c-112">*cCerts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac07c-112">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac07c-113">Numero di certificati per i quali recuperare gli abilitatori del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ac07c-113">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="ac07c-114">Questo è il numero di elementi nella matrice *rgpbCertHashes* .</span><span class="sxs-lookup"><span data-stu-id="ac07c-114">This is the number of elements in the *rgpbCertHashes* array.</span></span>

</dd> <dt>

<span data-ttu-id="ac07c-115">*hResultHint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac07c-115">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac07c-116">Valore restituito ricevuto dall'operazione non riuscita a causa di un certificato revocato.</span><span class="sxs-lookup"><span data-stu-id="ac07c-116">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="ac07c-117">Se non si chiama in risposta a una chiamata al metodo non riuscita, impostare su S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac07c-117">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="ac07c-118">*prgContentEnablers* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ac07c-118">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac07c-119">Matrice che riceve gli indirizzi delle interfacce **IMFContentEnabler** appena create.</span><span class="sxs-lookup"><span data-stu-id="ac07c-119">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="ac07c-120">Impostare su **null** per ottenere il numero di abilitatori del contenuto nel parametro *pcContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="ac07c-120">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ac07c-121">*pcContentEnablers* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ac07c-121">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac07c-122">Numero di elementi nella matrice *prgContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="ac07c-122">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="ac07c-123">Se *prgContentEnablers* è **null**, questo valore viene impostato sul numero di abilitatori di contenuto necessari nell'output.</span><span class="sxs-lookup"><span data-stu-id="ac07c-123">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac07c-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac07c-124">Return value</span></span>

<span data-ttu-id="ac07c-125">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ac07c-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ac07c-126">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ac07c-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ac07c-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ac07c-127">Return code</span></span>                                                                          | <span data-ttu-id="ac07c-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac07c-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ac07c-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac07c-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ac07c-130">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ac07c-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac07c-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac07c-131">Remarks</span></span>

<span data-ttu-id="ac07c-132">Se si utilizza l'interfaccia **IMFContentEnabler** per rinnovare i componenti revocati, è necessario chiarire il processo all'utente.</span><span class="sxs-lookup"><span data-stu-id="ac07c-132">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="ac07c-133">Questo chiarimento deve essere effettuato perché il processo di aggiornamento Invia le informazioni dal computer client a un sito Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac07c-133">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="ac07c-134">Quando si chiama **IMFContentEnabler:: AutomaticEnable**, l'attivatore del contenuto avvia il browser predefinito con l'indirizzo del servizio di aggiornamento sul sito Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac07c-134">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="ac07c-135">Un identificatore univoco che identifica il componente revocato viene inviato al servizio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ac07c-135">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="ac07c-136">Il servizio reindirizza quindi il browser a una pagina Web da cui l'utente potrebbe essere in grado di scaricare e installare la nuova versione del componente revocato.</span><span class="sxs-lookup"><span data-stu-id="ac07c-136">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac07c-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac07c-137">Requirements</span></span>



| <span data-ttu-id="ac07c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac07c-138">Requirement</span></span> | <span data-ttu-id="ac07c-139">Valore</span><span class="sxs-lookup"><span data-stu-id="ac07c-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac07c-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac07c-140">Header</span></span><br/>  | <dl> <span data-ttu-id="ac07c-141"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac07c-141"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac07c-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="ac07c-142">Library</span></span><br/> | <dl> <span data-ttu-id="ac07c-143"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac07c-143"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac07c-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac07c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac07c-145">**Interfaccia IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="ac07c-145">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





