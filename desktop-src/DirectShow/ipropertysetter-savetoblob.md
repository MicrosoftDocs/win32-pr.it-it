---
description: Il metodo SaveToBlob Salva i dati della proprietà in un formato di persistenza.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'Metodo IPropertySetter:: SaveToBlob (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329623"
---
# <a name="ipropertysettersavetoblob-method"></a><span data-ttu-id="572bb-103">Metodo IPropertySetter:: SaveToBlob</span><span class="sxs-lookup"><span data-stu-id="572bb-103">IPropertySetter::SaveToBlob method</span></span>

> [!Note]  
> <span data-ttu-id="572bb-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="572bb-104">\[Deprecated.</span></span> <span data-ttu-id="572bb-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="572bb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="572bb-106">Il `SaveToBlob` metodo salva i dati della proprietà in un formato di persistenza.</span><span class="sxs-lookup"><span data-stu-id="572bb-106">The `SaveToBlob` method saves the property data to a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="572bb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="572bb-107">Syntax</span></span>


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a><span data-ttu-id="572bb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="572bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="572bb-109">*pcSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="572bb-109">*pcSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="572bb-110">Riceve le dimensioni dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="572bb-110">Receives the size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="572bb-111">*PPB* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="572bb-111">*ppb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="572bb-112">Riceve un puntatore a una matrice di byte che riceve i dati.</span><span class="sxs-lookup"><span data-stu-id="572bb-112">Receives a pointer to an array of bytes that receives the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="572bb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="572bb-113">Return value</span></span>

<span data-ttu-id="572bb-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="572bb-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="572bb-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="572bb-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="572bb-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="572bb-116">Remarks</span></span>

<span data-ttu-id="572bb-117">Il metodo alloca memoria per la matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="572bb-117">The method allocates memory for the byte array.</span></span> <span data-ttu-id="572bb-118">Il chiamante deve liberarlo, usando la funzione **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="572bb-118">The caller must free it, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="572bb-119">Tutti i nomi e i valori delle proprietà vengono troncati con una lunghezza di 40 caratteri.</span><span class="sxs-lookup"><span data-stu-id="572bb-119">All property names and values are truncated to 40 characters in length.</span></span> <span data-ttu-id="572bb-120">Per questo motivo, XML è il formato di persistenza preferito.</span><span class="sxs-lookup"><span data-stu-id="572bb-120">For this reason, XML is the preferred persistence format.</span></span> <span data-ttu-id="572bb-121">Vedere [**interfaccia IXml2Dex**](ixml2dex.md).</span><span class="sxs-lookup"><span data-stu-id="572bb-121">See [**IXml2Dex Interface**](ixml2dex.md).</span></span>

> [!Note]  
> <span data-ttu-id="572bb-122">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="572bb-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="572bb-123">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="572bb-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="572bb-124">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="572bb-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="572bb-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="572bb-125">Requirements</span></span>



| <span data-ttu-id="572bb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="572bb-126">Requirement</span></span> | <span data-ttu-id="572bb-127">Valore</span><span class="sxs-lookup"><span data-stu-id="572bb-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="572bb-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="572bb-128">Header</span></span><br/>  | <dl> <span data-ttu-id="572bb-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="572bb-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="572bb-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="572bb-130">Library</span></span><br/> | <dl> <span data-ttu-id="572bb-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="572bb-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="572bb-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="572bb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="572bb-133">**Interfaccia IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="572bb-133">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="572bb-134">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="572bb-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




