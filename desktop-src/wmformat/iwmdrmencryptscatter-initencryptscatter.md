---
title: Metodo IWMDRMEncryptScatter InitEncryptScatter (wmdrmsdk. h)
description: Il metodo InitEncryptScatter Inizializza l'interfaccia IWMDRMEncryptScatter per l'utilizzo.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Metodo InitEncryptScatter Windows Media Format
- Metodo InitEncryptScatter Windows Media Format, interfaccia IWMDRMEncryptScatter
- Interfaccia IWMDRMEncryptScatter-formato Windows Media, metodo InitEncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328536"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a><span data-ttu-id="12426-106">Metodo IWMDRMEncryptScatter:: InitEncryptScatter</span><span class="sxs-lookup"><span data-stu-id="12426-106">IWMDRMEncryptScatter::InitEncryptScatter method</span></span>

<span data-ttu-id="12426-107">Il metodo **InitEncryptScatter** Inizializza l'interfaccia **IWMDRMEncryptScatter** per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="12426-107">The **InitEncryptScatter** method initializes the **IWMDRMEncryptScatter** interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="12426-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12426-108">Syntax</span></span>


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a><span data-ttu-id="12426-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="12426-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12426-110">*cStreams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12426-110">*cStreams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12426-111">Numero di elementi nella matrice *rgInfos* .</span><span class="sxs-lookup"><span data-stu-id="12426-111">Number of elements in the *rgInfos* array.</span></span> <span data-ttu-id="12426-112">Questo è anche il numero di flussi inclusi nei dati da crittografare.</span><span class="sxs-lookup"><span data-stu-id="12426-112">This is also the number of streams that are included in the data to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="12426-113">*rgInfos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12426-113">*rgInfos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12426-114">Matrice di una o più strutture di [**\_ \_ \_ informazioni di dispersione crittografate WMDRM**](wmdrm-encrypt-scatter-info.md) .</span><span class="sxs-lookup"><span data-stu-id="12426-114">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_INFO**](wmdrm-encrypt-scatter-info.md) structures.</span></span> <span data-ttu-id="12426-115">Ogni elemento contiene informazioni di crittografia per un flusso.</span><span class="sxs-lookup"><span data-stu-id="12426-115">Each element contains encryption information for a stream.</span></span> <span data-ttu-id="12426-116">Il numero di elementi nella matrice deve essere uguale al valore di *cStreams*.</span><span class="sxs-lookup"><span data-stu-id="12426-116">The number of elements in this array must be equal to the value of *cStreams*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12426-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12426-117">Return value</span></span>

<span data-ttu-id="12426-118">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="12426-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="12426-119">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="12426-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="12426-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="12426-120">Return code</span></span>                                                                          | <span data-ttu-id="12426-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12426-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="12426-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="12426-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="12426-123">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="12426-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="12426-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="12426-124">Remarks</span></span>

<span data-ttu-id="12426-125">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="12426-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="12426-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12426-126">Requirements</span></span>



| <span data-ttu-id="12426-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="12426-127">Requirement</span></span> | <span data-ttu-id="12426-128">Valore</span><span class="sxs-lookup"><span data-stu-id="12426-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12426-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12426-129">Header</span></span><br/> | <dl> <span data-ttu-id="12426-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="12426-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12426-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12426-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12426-132">**EncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="12426-132">**EncryptScatter**</span></span>](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[<span data-ttu-id="12426-133">**Interfaccia IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="12426-133">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





