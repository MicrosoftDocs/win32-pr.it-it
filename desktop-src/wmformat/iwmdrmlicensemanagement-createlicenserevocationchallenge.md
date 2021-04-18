---
title: Metodo IWMDRMLicenseManagement CreateLicenseRevocationChallenge (wmdrmsdk. h)
description: Il metodo CreateLicenseRevocationChallenge genera una richiesta di revoca delle licenze.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Metodo CreateLicenseRevocationChallenge Windows Media Format
- Metodo CreateLicenseRevocationChallenge Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo CreateLicenseRevocationChallenge
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328189"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a><span data-ttu-id="e28e6-106">Metodo IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge</span><span class="sxs-lookup"><span data-stu-id="e28e6-106">IWMDRMLicenseManagement::CreateLicenseRevocationChallenge method</span></span>

<span data-ttu-id="e28e6-107">Il metodo **CreateLicenseRevocationChallenge** genera una richiesta di revoca delle licenze.</span><span class="sxs-lookup"><span data-stu-id="e28e6-107">The **CreateLicenseRevocationChallenge** method generates a license revocation challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="e28e6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e28e6-108">Syntax</span></span>


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a><span data-ttu-id="e28e6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e28e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e28e6-110">*pbMachineID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e28e6-110">*pbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-111">Identificatore computer specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e28e6-111">User-specified machine identifier.</span></span> <span data-ttu-id="e28e6-112">Questo valore viene utilizzato per eseguire una query per una licenza nel server e deve essere conforme a qualsiasi formato utilizzato dal server licenze.</span><span class="sxs-lookup"><span data-stu-id="e28e6-112">This value is used to query for a license on the server and must conform to whatever format the license server uses.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-113">*cbMachineID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e28e6-113">*cbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-114">Dimensione, in byte, dell'identificatore del computer.</span><span class="sxs-lookup"><span data-stu-id="e28e6-114">Size, in bytes, of the machine identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-115">*pbChallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e28e6-115">*pbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-116">Dati di richiesta specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e28e6-116">User-specified challenge data.</span></span> <span data-ttu-id="e28e6-117">Questi dati, oltre all'identificatore del computer, vengono utilizzati per eseguire una query sul server licenze per la revoca delle licenze.</span><span class="sxs-lookup"><span data-stu-id="e28e6-117">This data, in addition to the machine identifier, is used to query the license server for licenses to be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-118">*cbChallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e28e6-118">*cbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-119">Dimensioni, in byte, dei dati della richiesta di verifica.</span><span class="sxs-lookup"><span data-stu-id="e28e6-119">Size, in bytes, of the challenge data.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-120">*ppbChallengeOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e28e6-120">*ppbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-121">Indirizzo di un puntatore che riceve l'indirizzo dell'output della richiesta di verifica.</span><span class="sxs-lookup"><span data-stu-id="e28e6-121">Address of a pointer that receives the address of the challenge output.</span></span> <span data-ttu-id="e28e6-122">Questo buffer corrisponde ai dati inviati al servizio di revoca delle licenze.</span><span class="sxs-lookup"><span data-stu-id="e28e6-122">This buffer is the data that is sent to the license revocation service.</span></span> <span data-ttu-id="e28e6-123">Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="e28e6-123">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-124">*pcbChallengeOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e28e6-124">*pcbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-125">Indirizzo di una variabile che riceve la dimensione dei dati di output della richiesta di verifica allocata, in byte.</span><span class="sxs-lookup"><span data-stu-id="e28e6-125">Address of a variable that receives the size of the allocated challenge output data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e28e6-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e28e6-126">Return value</span></span>

<span data-ttu-id="e28e6-127">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e28e6-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e28e6-128">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e28e6-128">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e28e6-129">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e28e6-129">Return code</span></span>                                                                          | <span data-ttu-id="e28e6-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e28e6-130">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e28e6-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e28e6-131"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e28e6-132">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e28e6-132">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e28e6-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="e28e6-133">Remarks</span></span>

<span data-ttu-id="e28e6-134">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="e28e6-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e28e6-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e28e6-135">Requirements</span></span>



| <span data-ttu-id="e28e6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e28e6-136">Requirement</span></span> | <span data-ttu-id="e28e6-137">Valore</span><span class="sxs-lookup"><span data-stu-id="e28e6-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e28e6-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e28e6-138">Header</span></span><br/> | <dl> <span data-ttu-id="e28e6-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e28e6-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e28e6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e28e6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e28e6-141">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="e28e6-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





