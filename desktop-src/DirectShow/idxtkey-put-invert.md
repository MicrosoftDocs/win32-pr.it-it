---
description: Il \_ metodo Put Invert specifica se l'operazione di chiave è invertita. Questa proprietà si applica a tutti i tipi di chiave ad eccezione di DXTKEY \_ alfa.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: 'IDxtKey: metodo:p ut_Invert (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3e4b807770d0eeb985c982b61b8390695cc42327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326907"
---
# <a name="idxtkeyput_invert-method"></a><span data-ttu-id="6a001-104">IDxtKey: metodo di \_ inversione:p UT</span><span class="sxs-lookup"><span data-stu-id="6a001-104">IDxtKey::put\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="6a001-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6a001-105">\[Deprecated.</span></span> <span data-ttu-id="6a001-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6a001-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6a001-107">Il `put_Invert` metodo specifica se l'operazione chiave è invertita.</span><span class="sxs-lookup"><span data-stu-id="6a001-107">The `put_Invert` method specifies whether the key operation is inverted.</span></span> <span data-ttu-id="6a001-108">Questa proprietà si applica a tutti i tipi di chiave ad eccezione di DXTKEY \_ alfa.</span><span class="sxs-lookup"><span data-stu-id="6a001-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a001-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a001-109">Syntax</span></span>


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="6a001-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a001-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a001-111">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a001-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a001-112">Specifica un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="6a001-112">Specifies a Boolean value.</span></span> <span data-ttu-id="6a001-113">Se **true**, i pixel nell'immagine di sovrastanti vengono invertiti rispetto all'operazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6a001-113">If **TRUE**, pixels in the overlying image are inverted with respect to the default operation.</span></span> <span data-ttu-id="6a001-114">Se **false**, i pixel nell'immagine di sovrastanti vengono resi trasparenti nel modo predefinito.</span><span class="sxs-lookup"><span data-stu-id="6a001-114">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a001-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a001-115">Return value</span></span>

<span data-ttu-id="6a001-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6a001-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a001-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a001-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a001-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a001-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a001-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6a001-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6a001-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6a001-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6a001-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6a001-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a001-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a001-122">Requirements</span></span>



| <span data-ttu-id="6a001-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a001-123">Requirement</span></span> | <span data-ttu-id="6a001-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6a001-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a001-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a001-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6a001-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a001-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6a001-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a001-127">Library</span></span><br/> | <dl> <span data-ttu-id="6a001-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a001-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a001-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a001-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a001-130">**Interfaccia IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="6a001-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="6a001-131">**IDxtKey: tipo di:p di \_ tipo UT**</span><span class="sxs-lookup"><span data-stu-id="6a001-131">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




