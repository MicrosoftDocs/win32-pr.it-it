---
title: Metodo IWMDRMEncryptScatter EncryptScatter (wmdrmsdk. h)
description: Il metodo EncryptScatter consente di decodificare e crittografare i dati.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Metodo EncryptScatter Windows Media Format
- Metodo EncryptScatter Windows Media Format, interfaccia IWMDRMEncryptScatter
- Interfaccia IWMDRMEncryptScatter-formato Windows Media, metodo EncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324286"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a><span data-ttu-id="a0f34-106">Metodo IWMDRMEncryptScatter:: EncryptScatter</span><span class="sxs-lookup"><span data-stu-id="a0f34-106">IWMDRMEncryptScatter::EncryptScatter method</span></span>

<span data-ttu-id="a0f34-107">Il metodo **EncryptScatter** consente di decodificare e crittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="a0f34-107">The **EncryptScatter** method unscrambles and encrypts data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f34-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0f34-108">Syntax</span></span>


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a><span data-ttu-id="a0f34-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0f34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f34-110">*cBlocks* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f34-110">*cBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f34-111">Numero di elementi nella matrice *rgBlocks* .</span><span class="sxs-lookup"><span data-stu-id="a0f34-111">Number of elements in the *rgBlocks* array.</span></span>

</dd> <dt>

<span data-ttu-id="a0f34-112">*rgBlocks* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f34-112">*rgBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f34-113">Matrice di una o più strutture di [**\_ \_ \_ blocco a dispersione crittografate WMDRM**](wmdrm-encrypt-scatter-block.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f34-113">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_BLOCK**](wmdrm-encrypt-scatter-block.md) structures.</span></span> <span data-ttu-id="a0f34-114">Ogni elemento descrive un blocco di dati da non codificare e crittografare.</span><span class="sxs-lookup"><span data-stu-id="a0f34-114">Each element describes a block of data to be unscrambled and encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="a0f34-115">*pWMCryptoData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f34-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f34-116">Puntatore a una struttura [**WMDRMCryptoData**](wmdrmcryptodata.md) che contiene i parametri di crittografia.</span><span class="sxs-lookup"><span data-stu-id="a0f34-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure that contains encryption parameters.</span></span> <span data-ttu-id="a0f34-117">Impostare su **null** per usare i parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a0f34-117">Set to **NULL** to use the default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="a0f34-118">*cbOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f34-118">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f34-119">Dimensioni del buffer dei dati di output passati come *pbOutput*.</span><span class="sxs-lookup"><span data-stu-id="a0f34-119">Size of the output data buffer passed as *pbOutput*.</span></span>

</dd> <dt>

<span data-ttu-id="a0f34-120">*pbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a0f34-120">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f34-121">Buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a0f34-121">Output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f34-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0f34-122">Return value</span></span>

<span data-ttu-id="a0f34-123">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a0f34-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a0f34-124">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a0f34-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a0f34-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a0f34-125">Return code</span></span>                                                                          | <span data-ttu-id="a0f34-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0f34-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a0f34-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f34-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a0f34-128">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a0f34-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a0f34-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0f34-129">Remarks</span></span>

<span data-ttu-id="a0f34-130">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="a0f34-130">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f34-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0f34-131">Requirements</span></span>



| <span data-ttu-id="a0f34-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f34-132">Requirement</span></span> | <span data-ttu-id="a0f34-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a0f34-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f34-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0f34-134">Header</span></span><br/> | <dl> <span data-ttu-id="a0f34-135"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f34-135"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0f34-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0f34-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f34-137">**InitEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="a0f34-137">**InitEncryptScatter**</span></span>](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[<span data-ttu-id="a0f34-138">**Interfaccia IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="a0f34-138">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





