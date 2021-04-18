---
description: Il metodo LoadFromBlob carica i dati delle proprietà da un formato di persistenza.
ms.assetid: b314a844-2190-469a-a030-4494e2140ce6
title: 'Metodo IPropertySetter:: LoadFromBlob (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadFromBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a1e58aa5802e8fcb05c2464fc1f121ee1e86f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325478"
---
# <a name="ipropertysetterloadfromblob-method"></a><span data-ttu-id="0970a-103">Metodo IPropertySetter:: LoadFromBlob</span><span class="sxs-lookup"><span data-stu-id="0970a-103">IPropertySetter::LoadFromBlob method</span></span>

> [!Note]  
> <span data-ttu-id="0970a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0970a-104">\[Deprecated.</span></span> <span data-ttu-id="0970a-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0970a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0970a-106">Il `LoadFromBlob` metodo carica i dati della proprietà da un formato di persistenza.</span><span class="sxs-lookup"><span data-stu-id="0970a-106">The `LoadFromBlob` method loads property data from a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="0970a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0970a-107">Syntax</span></span>


```C++
HRESULT LoadFromBlob(
  [in] LONG cSize,
  [in] BYTE *pb
);
```



## <a name="parameters"></a><span data-ttu-id="0970a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0970a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0970a-109">*cSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0970a-109">*cSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0970a-110">Dimensioni dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="0970a-110">Size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0970a-111">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0970a-111">*pb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0970a-112">Puntatore a una matrice di byte che contiene i dati.</span><span class="sxs-lookup"><span data-stu-id="0970a-112">Pointer to an array of bytes that contains the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0970a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0970a-113">Return value</span></span>

<span data-ttu-id="0970a-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0970a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0970a-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0970a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0970a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0970a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0970a-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="0970a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0970a-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0970a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0970a-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0970a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0970a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0970a-120">Requirements</span></span>



| <span data-ttu-id="0970a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0970a-121">Requirement</span></span> | <span data-ttu-id="0970a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0970a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0970a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0970a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0970a-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0970a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0970a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="0970a-125">Library</span></span><br/> | <dl> <span data-ttu-id="0970a-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0970a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0970a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0970a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0970a-128">**Interfaccia IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="0970a-128">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="0970a-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="0970a-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




