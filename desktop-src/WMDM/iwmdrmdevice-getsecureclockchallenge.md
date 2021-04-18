---
title: Metodo IWMDRMDevice GetSecureClockChallenge
description: Il metodo GetSecureClockChallenge Recupera il risultato della verifica del clock protetto.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Metodo GetSecureClockChallenge Windows Media Gestione dispositivi
- Metodo GetSecureClockChallenge Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo GetSecureClockChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e57165f75a23d13d847e028deb69de383e2855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324111"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a><span data-ttu-id="54d28-106">Metodo IWMDRMDevice:: GetSecureClockChallenge</span><span class="sxs-lookup"><span data-stu-id="54d28-106">IWMDRMDevice::GetSecureClockChallenge method</span></span>

<span data-ttu-id="54d28-107">Il metodo **GetSecureClockChallenge** Recupera il risultato della verifica del clock protetto.</span><span class="sxs-lookup"><span data-stu-id="54d28-107">The **GetSecureClockChallenge** method retrieves the secure clock challenge result.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d28-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54d28-108">Syntax</span></span>


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="54d28-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="54d28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54d28-110">*ppbChallenge* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="54d28-110">*ppbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54d28-111">Risultato della richiesta di verifica recuperato.</span><span class="sxs-lookup"><span data-stu-id="54d28-111">Retrieved challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="54d28-112">*pcbChallenge* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="54d28-112">*pcbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54d28-113">Dimensioni del risultato della richiesta, in byte.</span><span class="sxs-lookup"><span data-stu-id="54d28-113">Size of the challenge result, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54d28-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54d28-114">Return value</span></span>

<span data-ttu-id="54d28-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="54d28-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="54d28-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="54d28-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="54d28-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="54d28-117">Return code</span></span>                                                                          | <span data-ttu-id="54d28-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54d28-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="54d28-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="54d28-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="54d28-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="54d28-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="54d28-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54d28-121">Requirements</span></span>



| <span data-ttu-id="54d28-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="54d28-122">Requirement</span></span> | <span data-ttu-id="54d28-123">Valore</span><span class="sxs-lookup"><span data-stu-id="54d28-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54d28-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54d28-124">Header</span></span><br/>  | <dl> <span data-ttu-id="54d28-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54d28-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="54d28-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="54d28-126">Library</span></span><br/> | <dl> <span data-ttu-id="54d28-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54d28-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54d28-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54d28-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d28-129">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="54d28-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="54d28-130">**Interfaccia IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="54d28-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





