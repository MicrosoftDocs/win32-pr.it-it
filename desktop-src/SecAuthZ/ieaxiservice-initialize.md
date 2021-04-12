---
description: Verifica e Scarica un oggetto ActiveX.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'Metodo IeAxiService:: Initialize'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233694"
---
# <a name="ieaxiserviceinitialize-method"></a><span data-ttu-id="32729-103">Metodo IeAxiService:: Initialize</span><span class="sxs-lookup"><span data-stu-id="32729-103">IeAxiService::Initialize method</span></span>

<span data-ttu-id="32729-104">Il metodo **Initialize** controlla e Scarica un oggetto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="32729-104">The **Initialize** method checks and downloads an ActiveX object.</span></span> <span data-ttu-id="32729-105">Se l'oggetto soddisfa i requisiti dei criteri, questo metodo inizializza un oggetto di sistema che installa l'oggetto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="32729-105">If the object meets policy requirements, this method initializes a system object that installs the ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="32729-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32729-106">Syntax</span></span>


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a><span data-ttu-id="32729-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="32729-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32729-108">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32729-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32729-109">Handle per la finestra padre della finestra che tenta di installare il controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="32729-109">A handle to the parent window of the window that is attempting to install the ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="32729-110">*dwClientPID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32729-110">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32729-111">ID processo del processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="32729-111">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="32729-112">*bstrDesktop* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32729-112">*bstrDesktop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32729-113">Desktop per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="32729-113">The desktop for the object.</span></span>

</dd> <dt>

<span data-ttu-id="32729-114">*bstrClsID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32729-114">*bstrClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32729-115">ID classe dell'oggetto ActiveX da installare.</span><span class="sxs-lookup"><span data-stu-id="32729-115">The class ID of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="32729-116">*bstrURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32729-116">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32729-117">URL dell'oggetto ActiveX da installare.</span><span class="sxs-lookup"><span data-stu-id="32729-117">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="32729-118">*pbstrNonce* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="32729-118">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32729-119">Contesto che può essere utilizzato per condividere le informazioni sullo stato nelle chiamate ad altri metodi utilizzati per verificare e scaricare l'oggetto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="32729-119">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> <dt>

<span data-ttu-id="32729-120">*ppISyncBrokerInterface* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="32729-120">*ppISyncBrokerInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32729-121">Puntatore all'istanza dell'interfaccia [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) che installa il controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="32729-121">A pointer to the instance of the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface that installs the ActiveX control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32729-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32729-122">Return value</span></span>

<span data-ttu-id="32729-123">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="32729-123">If the function succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="32729-124">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici di errore.</span><span class="sxs-lookup"><span data-stu-id="32729-124">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="32729-125">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="32729-125">Return code/value</span></span>                                                                                                                                                              | <span data-ttu-id="32729-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32729-126">Description</span></span>                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="32729-127"><dt>**Attendibilità \_ E \_ soggetto \_ non \_ attendibile**</dt> <dt>0x800B0004</dt></span><span class="sxs-lookup"><span data-stu-id="32729-127"><dt>**TRUST\_E\_SUBJECT\_NOT\_TRUSTED**</dt> <dt>0x800B0004</dt></span></span> </dl> | <span data-ttu-id="32729-128">L'oggetto ActiveX non deve essere installato.</span><span class="sxs-lookup"><span data-stu-id="32729-128">The ActiveX object should not be installed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="32729-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32729-129">Requirements</span></span>



| <span data-ttu-id="32729-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="32729-130">Requirement</span></span> | <span data-ttu-id="32729-131">Valore</span><span class="sxs-lookup"><span data-stu-id="32729-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32729-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32729-132">Minimum supported client</span></span><br/> | <span data-ttu-id="32729-133">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="32729-133">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="32729-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32729-134">Minimum supported server</span></span><br/> | <span data-ttu-id="32729-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="32729-135">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="32729-136">IID</span><span class="sxs-lookup"><span data-stu-id="32729-136">IID</span></span><br/>                      | <span data-ttu-id="32729-137">IID \_ IeAxiService è definito come E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="32729-137">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="32729-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32729-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32729-139">**IeAxiService**</span><span class="sxs-lookup"><span data-stu-id="32729-139">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

 




