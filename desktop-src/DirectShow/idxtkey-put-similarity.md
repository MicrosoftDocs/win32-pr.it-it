---
description: Il \_ metodo di somiglianza put specifica l'intervallo di dati del colore che diventa trasparente. Con valori superiori, una gamma più ampia di colori simili è trasparente. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB o DXTKEY \_ NONRED.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: 'IDxtKey: metodo:p ut_Similarity (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329629"
---
# <a name="idxtkeyput_similarity-method"></a><span data-ttu-id="192a2-105">IDxtKey: metodo di \_ somiglianza ut:p</span><span class="sxs-lookup"><span data-stu-id="192a2-105">IDxtKey::put\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="192a2-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="192a2-106">\[Deprecated.</span></span> <span data-ttu-id="192a2-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="192a2-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="192a2-108">Il `put_Similarity` metodo specifica l'intervallo di dati del colore che diventa trasparente.</span><span class="sxs-lookup"><span data-stu-id="192a2-108">The `put_Similarity` method specifies the range of color data that becomes transparent.</span></span> <span data-ttu-id="192a2-109">Con valori superiori, una gamma più ampia di colori simili è trasparente.</span><span class="sxs-lookup"><span data-stu-id="192a2-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="192a2-110">Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB o DXTKEY \_ NONRED.</span><span class="sxs-lookup"><span data-stu-id="192a2-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="192a2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="192a2-111">Syntax</span></span>


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="192a2-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="192a2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="192a2-113">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="192a2-113">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="192a2-114">Specifica il valore di somiglianza.</span><span class="sxs-lookup"><span data-stu-id="192a2-114">Specifies the similarity value.</span></span> <span data-ttu-id="192a2-115">L'intervallo valido è compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="192a2-115">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="192a2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="192a2-116">Return value</span></span>

<span data-ttu-id="192a2-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="192a2-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="192a2-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="192a2-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="192a2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="192a2-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="192a2-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="192a2-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="192a2-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="192a2-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="192a2-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="192a2-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="192a2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="192a2-123">Requirements</span></span>



| <span data-ttu-id="192a2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="192a2-124">Requirement</span></span> | <span data-ttu-id="192a2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="192a2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="192a2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="192a2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="192a2-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="192a2-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="192a2-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="192a2-128">Library</span></span><br/> | <dl> <span data-ttu-id="192a2-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="192a2-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="192a2-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="192a2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="192a2-131">**Interfaccia IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="192a2-131">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="192a2-132">**IDxtKey: tipo di:p di \_ tipo UT**</span><span class="sxs-lookup"><span data-stu-id="192a2-132">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




