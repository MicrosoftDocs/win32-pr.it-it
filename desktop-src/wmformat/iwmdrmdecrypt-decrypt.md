---
title: Metodo Decrypt IWMDRMDecrypt (wmdrmsdk. h)
description: Il metodo Decrypt decrittografa un buffer di dati sul posto.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Metodo Decrypt Windows Media Format
- Metodo di decrittografia Windows Media Format, interfaccia IWMDRMDecrypt
- Interfaccia IWMDRMDecrypt-formato Windows Media, metodo Decrypt
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324294"
---
# <a name="iwmdrmdecryptdecrypt-method"></a><span data-ttu-id="ed314-106">IWMDRMDecrypt::D Metodo ecrypt</span><span class="sxs-lookup"><span data-stu-id="ed314-106">IWMDRMDecrypt::Decrypt method</span></span>

<span data-ttu-id="ed314-107">Il metodo **Decrypt** decrittografa un buffer di dati sul posto.</span><span class="sxs-lookup"><span data-stu-id="ed314-107">The **Decrypt** method decrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed314-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed314-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="ed314-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed314-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed314-110">*pbData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ed314-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed314-111">Dati da decrittografare.</span><span class="sxs-lookup"><span data-stu-id="ed314-111">Data to be decrypted.</span></span> <span data-ttu-id="ed314-112">Se il metodo ha esito positivo, questi dati vengono decrittografati al ritorno.</span><span class="sxs-lookup"><span data-stu-id="ed314-112">If the method succeeds, this data is decrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="ed314-113">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed314-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed314-114">Dimensioni dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="ed314-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ed314-115">*pWMCryptoData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed314-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed314-116">Puntatore a una struttura [**WMDRMCryptoData**](wmdrmcryptodata.md) che contiene parametri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="ed314-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="ed314-117">Può essere **null** se il contenuto è stato crittografato usando i parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="ed314-117">Can be **NULL** if the content was encrypted using the default parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed314-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed314-118">Return value</span></span>

<span data-ttu-id="ed314-119">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ed314-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ed314-120">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ed314-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ed314-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ed314-121">Return code</span></span>                                                                          | <span data-ttu-id="ed314-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed314-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ed314-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ed314-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ed314-124">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ed314-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed314-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed314-125">Remarks</span></span>

<span data-ttu-id="ed314-126">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="ed314-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed314-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed314-127">Requirements</span></span>



| <span data-ttu-id="ed314-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed314-128">Requirement</span></span> | <span data-ttu-id="ed314-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ed314-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed314-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed314-130">Header</span></span><br/> | <dl> <span data-ttu-id="ed314-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed314-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed314-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed314-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed314-133">**Interfaccia IWMDRMDecrypt**</span><span class="sxs-lookup"><span data-stu-id="ed314-133">**IWMDRMDecrypt Interface**</span></span>](iwmdrmdecrypt.md)
</dt> <dt>

[<span data-ttu-id="ed314-134">**WMDRMCryptoData**</span><span class="sxs-lookup"><span data-stu-id="ed314-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





