---
description: Il \_ metodo Get somiglianza recupera l'intervallo di dati del colore che diventa trasparente. Con valori superiori, una gamma più ampia di colori simili è trasparente. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB o DXTKEY \_ NONRED.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'Metodo IDxtKey:: get_Similarity (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e53898a1f9c5175fdf7a42ba6de68e3173f02afe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326915"
---
# <a name="idxtkeyget_similarity-method"></a><span data-ttu-id="46d94-105">Metodo di somiglianza IDxtKey:: Get \_</span><span class="sxs-lookup"><span data-stu-id="46d94-105">IDxtKey::get\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="46d94-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="46d94-106">\[Deprecated.</span></span> <span data-ttu-id="46d94-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46d94-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="46d94-108">Il `get_Similarity` metodo recupera l'intervallo di dati del colore che diventa trasparente.</span><span class="sxs-lookup"><span data-stu-id="46d94-108">The `get_Similarity` method retrieves the range of color data that becomes transparent.</span></span> <span data-ttu-id="46d94-109">Con valori superiori, una gamma più ampia di colori simili è trasparente.</span><span class="sxs-lookup"><span data-stu-id="46d94-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="46d94-110">Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB o DXTKEY \_ NONRED.</span><span class="sxs-lookup"><span data-stu-id="46d94-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d94-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46d94-111">Syntax</span></span>


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="46d94-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="46d94-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d94-113">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="46d94-113">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="46d94-114">Riceve il valore di somiglianza.</span><span class="sxs-lookup"><span data-stu-id="46d94-114">Receives the similarity value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d94-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46d94-115">Return value</span></span>

<span data-ttu-id="46d94-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="46d94-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46d94-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46d94-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46d94-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="46d94-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46d94-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="46d94-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="46d94-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="46d94-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="46d94-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="46d94-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46d94-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46d94-122">Requirements</span></span>



| <span data-ttu-id="46d94-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="46d94-123">Requirement</span></span> | <span data-ttu-id="46d94-124">Valore</span><span class="sxs-lookup"><span data-stu-id="46d94-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46d94-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46d94-125">Header</span></span><br/>  | <dl> <span data-ttu-id="46d94-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="46d94-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="46d94-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="46d94-127">Library</span></span><br/> | <dl> <span data-ttu-id="46d94-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46d94-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d94-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46d94-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d94-130">**Interfaccia IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="46d94-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="46d94-131">**Tipo di IDxtKey:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="46d94-131">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




