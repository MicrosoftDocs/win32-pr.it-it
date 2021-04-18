---
title: Metodo IWMDRMDevice GetSecureClock
description: Il metodo GetSecureClock Recupera il clock sicuro, quindi è possibile applicare licenze basate sul tempo.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Metodo GetSecureClock Windows Media Gestione dispositivi
- Metodo GetSecureClock Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo GetSecureClock
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324117"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a><span data-ttu-id="725ba-106">Metodo IWMDRMDevice:: GetSecureClock</span><span class="sxs-lookup"><span data-stu-id="725ba-106">IWMDRMDevice::GetSecureClock method</span></span>

<span data-ttu-id="725ba-107">Il metodo **GetSecureClock** Recupera il clock sicuro, quindi è possibile applicare licenze basate sul tempo.</span><span class="sxs-lookup"><span data-stu-id="725ba-107">The **GetSecureClock** method retrieves the secure clock, so time-based licenses can be enforced.</span></span>

## <a name="syntax"></a><span data-ttu-id="725ba-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="725ba-108">Syntax</span></span>


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="725ba-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="725ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="725ba-110">*ppbSecureClock* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="725ba-110">*ppbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="725ba-111">Clock protetto recuperato.</span><span class="sxs-lookup"><span data-stu-id="725ba-111">Retrieved secure clock.</span></span>

</dd> <dt>

<span data-ttu-id="725ba-112">*pcbSecureClock* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="725ba-112">*pcbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="725ba-113">Dimensioni del clock sicuro, in byte.</span><span class="sxs-lookup"><span data-stu-id="725ba-113">Size of the secure clock, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="725ba-114">*pdwFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="725ba-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="725ba-115">Flag di stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="725ba-115">Device status flags.</span></span> <span data-ttu-id="725ba-116">Questo valore deve essere uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="725ba-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="725ba-117">Flag</span><span class="sxs-lookup"><span data-stu-id="725ba-117">Flag</span></span>                     | <span data-ttu-id="725ba-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="725ba-118">Description</span></span>                            |
|--------------------------|----------------------------------------|
| <span data-ttu-id="725ba-119">\_ISWMDRM del dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="725ba-119">WMDRM\_DEVICE\_ISWMDRM</span></span>   | <span data-ttu-id="725ba-120">Il dispositivo supporta Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="725ba-120">The device supports Windows Media DRM.</span></span> |
| <span data-ttu-id="725ba-121">\_NEEDCLOCK del dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="725ba-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span> | <span data-ttu-id="725ba-122">Il dispositivo deve essere clock.</span><span class="sxs-lookup"><span data-stu-id="725ba-122">The device needs clock.</span></span>                |
| <span data-ttu-id="725ba-123">il dispositivo WMDRM è stato \_ \_ revocato</span><span class="sxs-lookup"><span data-stu-id="725ba-123">WMDRM\_DEVICE\_REVOKED</span></span>   | <span data-ttu-id="725ba-124">Il dispositivo è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="725ba-124">The device has been revoked.</span></span>           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="725ba-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="725ba-125">Return value</span></span>

<span data-ttu-id="725ba-126">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="725ba-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="725ba-127">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="725ba-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="725ba-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="725ba-128">Return code</span></span>                                                                          | <span data-ttu-id="725ba-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="725ba-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="725ba-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="725ba-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="725ba-131">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="725ba-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="725ba-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="725ba-132">Requirements</span></span>



| <span data-ttu-id="725ba-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="725ba-133">Requirement</span></span> | <span data-ttu-id="725ba-134">Valore</span><span class="sxs-lookup"><span data-stu-id="725ba-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="725ba-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="725ba-135">Header</span></span><br/>  | <dl> <span data-ttu-id="725ba-136"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="725ba-136"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="725ba-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="725ba-137">Library</span></span><br/> | <dl> <span data-ttu-id="725ba-138"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="725ba-138"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="725ba-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="725ba-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725ba-140">**GetSecureClockChallenge**</span><span class="sxs-lookup"><span data-stu-id="725ba-140">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[<span data-ttu-id="725ba-141">**Interfaccia IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="725ba-141">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> <dt>

[<span data-ttu-id="725ba-142">**SetSecureClockResponse**</span><span class="sxs-lookup"><span data-stu-id="725ba-142">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





