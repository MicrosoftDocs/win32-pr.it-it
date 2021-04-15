---
description: Esegue i controlli di sicurezza sull'oggetto ActiveX specificato e restituisce il percorso in cui è stato scaricato il file con estensione CAB corrispondente.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'Metodo IeAxiServiceCallback:: VerifyFile'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529880"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a><span data-ttu-id="89eee-103">Metodo IeAxiServiceCallback:: VerifyFile</span><span class="sxs-lookup"><span data-stu-id="89eee-103">IeAxiServiceCallback::VerifyFile method</span></span>

<span data-ttu-id="89eee-104">Il metodo **VerifyFile** esegue i controlli di sicurezza sull'oggetto ActiveX specificato e restituisce il percorso in cui è stato scaricato il file con estensione CAB corrispondente.</span><span class="sxs-lookup"><span data-stu-id="89eee-104">The **VerifyFile** method performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="89eee-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89eee-105">Syntax</span></span>


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a><span data-ttu-id="89eee-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89eee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89eee-107">*bstrFileUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89eee-107">*bstrFileUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89eee-108">URL dell'oggetto ActiveX da verificare.</span><span class="sxs-lookup"><span data-stu-id="89eee-108">The URL of the ActiveX object to check.</span></span>

</dd> <dt>

<span data-ttu-id="89eee-109">*bstrApprovedFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89eee-109">*bstrApprovedFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89eee-110">Nome del file in cui è stato scaricato il file con estensione cab associato all'oggetto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="89eee-110">The name of the file where the .cab file associated with the ActiveX object was downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89eee-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89eee-111">Return value</span></span>

<span data-ttu-id="89eee-112">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="89eee-112">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="89eee-113">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="89eee-113">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="89eee-114">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="89eee-114">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="89eee-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89eee-115">Requirements</span></span>



| <span data-ttu-id="89eee-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="89eee-116">Requirement</span></span> | <span data-ttu-id="89eee-117">Valore</span><span class="sxs-lookup"><span data-stu-id="89eee-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89eee-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89eee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="89eee-119">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="89eee-119">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89eee-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89eee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="89eee-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="89eee-121">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="89eee-122">IID</span><span class="sxs-lookup"><span data-stu-id="89eee-122">IID</span></span><br/>                      | <span data-ttu-id="89eee-123">IID \_ IeAxiServiceCallback è definito come 1823E7BA-EC36-447A-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="89eee-123">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="89eee-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89eee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89eee-125">**IeAxiServiceCallback**</span><span class="sxs-lookup"><span data-stu-id="89eee-125">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

