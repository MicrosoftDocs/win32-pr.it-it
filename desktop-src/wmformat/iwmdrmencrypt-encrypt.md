---
title: Metodo Encrypt IWMDRMEncrypt (wmdrmsdk. h)
description: Il metodo Encrypt crittografa un buffer di dati sul posto.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Metodo Encrypt formato Windows Media
- Metodo Encrypt formato Windows Media, interfaccia IWMDRMEncrypt
- Interfaccia IWMDRMEncrypt-formato Windows Media, metodo Encrypt
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324287"
---
# <a name="iwmdrmencryptencrypt-method"></a><span data-ttu-id="21cde-106">Metodo IWMDRMEncrypt:: Encrypt</span><span class="sxs-lookup"><span data-stu-id="21cde-106">IWMDRMEncrypt::Encrypt method</span></span>

<span data-ttu-id="21cde-107">Il metodo **Encrypt** crittografa un buffer di dati sul posto.</span><span class="sxs-lookup"><span data-stu-id="21cde-107">The **Encrypt** method encrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="21cde-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21cde-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="21cde-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="21cde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21cde-110">*pbData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="21cde-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="21cde-111">Dati da crittografare.</span><span class="sxs-lookup"><span data-stu-id="21cde-111">Data to encrypt.</span></span> <span data-ttu-id="21cde-112">Se il metodo ha esito positivo, i dati vengono crittografati al ritorno.</span><span class="sxs-lookup"><span data-stu-id="21cde-112">If the method succeeds, the data is encrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="21cde-113">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21cde-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21cde-114">Dimensioni dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="21cde-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="21cde-115">*pWMCryptoData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21cde-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21cde-116">Puntatore a una struttura [**WMDRMCryptoData**](wmdrmcryptodata.md) che contiene parametri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="21cde-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="21cde-117">Impostare su **null** per usare i valori di crittografia predefiniti.</span><span class="sxs-lookup"><span data-stu-id="21cde-117">Set to **NULL** to use the default encryption values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21cde-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21cde-118">Return value</span></span>

<span data-ttu-id="21cde-119">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="21cde-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="21cde-120">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="21cde-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="21cde-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="21cde-121">Return code</span></span>                                                                          | <span data-ttu-id="21cde-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21cde-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="21cde-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21cde-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="21cde-124">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="21cde-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="21cde-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="21cde-125">Remarks</span></span>

<span data-ttu-id="21cde-126">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="21cde-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="21cde-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21cde-127">Requirements</span></span>



| <span data-ttu-id="21cde-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="21cde-128">Requirement</span></span> | <span data-ttu-id="21cde-129">Valore</span><span class="sxs-lookup"><span data-stu-id="21cde-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21cde-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21cde-130">Header</span></span><br/> | <dl> <span data-ttu-id="21cde-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="21cde-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21cde-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21cde-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21cde-133">**Interfaccia IWMDRMEncrypt**</span><span class="sxs-lookup"><span data-stu-id="21cde-133">**IWMDRMEncrypt Interface**</span></span>](iwmdrmencrypt.md)
</dt> <dt>

[<span data-ttu-id="21cde-134">**WMDRMCryptoData**</span><span class="sxs-lookup"><span data-stu-id="21cde-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





