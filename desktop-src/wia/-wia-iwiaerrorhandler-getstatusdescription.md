---
description: Restituisce una stringa che descrive il codice di stato.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'Metodo IWiaErrorHandler:: GetStatusDescription (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308224"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a><span data-ttu-id="e2db9-103">Metodo IWiaErrorHandler:: GetStatusDescription</span><span class="sxs-lookup"><span data-stu-id="e2db9-103">IWiaErrorHandler::GetStatusDescription method</span></span>

<span data-ttu-id="e2db9-104">Restituisce una stringa che descrive il codice di stato.</span><span class="sxs-lookup"><span data-stu-id="e2db9-104">Returns a string that describes the status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2db9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2db9-105">Syntax</span></span>


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a><span data-ttu-id="e2db9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2db9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2db9-107">*punkItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2db9-107">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2db9-108">Tipo: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="e2db9-108">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="e2db9-109">Puntatore all' [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'elemento da trasferire.</span><span class="sxs-lookup"><span data-stu-id="e2db9-109">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) of the item being transferred.</span></span> <span data-ttu-id="e2db9-110">Questo oggetto implementa almeno [_ *IWiaItem2* \*](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="e2db9-110">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="e2db9-111">*hrStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2db9-111">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2db9-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e2db9-112">Type: **HRESULT**</span></span>

<span data-ttu-id="e2db9-113">**HRESULT** che rappresenta il codice di stato ricevuto da [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="e2db9-113">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="e2db9-114">*cbResLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2db9-114">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2db9-115">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="e2db9-115">Type: **LONG**</span></span>

<span data-ttu-id="e2db9-116">**Long** che corrisponde alla dimensione dei dati a cui fa riferimento *pbData*.</span><span class="sxs-lookup"><span data-stu-id="e2db9-116">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="e2db9-117">*pbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2db9-117">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2db9-118">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="e2db9-118">Type: \**BYTE\** _</span></span>

<span data-ttu-id="e2db9-119">Puntatore al buffer di dati ricevuto da [_ *BandedDataCallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="e2db9-119">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="e2db9-120">*pbstrDescription* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e2db9-120">*pbstrDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2db9-121">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="e2db9-121">Type: \**BSTR\** _</span></span>

<span data-ttu-id="e2db9-122">_ *BSTR*\* che riceve una descrizione dello stato o dell'errore rilevato durante il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="e2db9-122">_ *BSTR*\* that receives a description of the status or error encountered during the data transfer.</span></span> <span data-ttu-id="e2db9-123">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e2db9-123">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="e2db9-124">Il chiamante deve liberare la stringa usando [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)e l'implementatore deve allocare la stringa usando [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span><span class="sxs-lookup"><span data-stu-id="e2db9-124">The caller must free the string using [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), and the implementor must allocate the string using [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2db9-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2db9-125">Return value</span></span>

<span data-ttu-id="e2db9-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e2db9-126">Type: **HRESULT**</span></span>

<span data-ttu-id="e2db9-127">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e2db9-127">Returns one of the following values.</span></span>



| <span data-ttu-id="e2db9-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e2db9-128">Return code</span></span>                                                                             | <span data-ttu-id="e2db9-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2db9-129">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2db9-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2db9-130"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e2db9-131">*pbstrDescription* contiene un puntatore **BSTR** valido.</span><span class="sxs-lookup"><span data-stu-id="e2db9-131">*pbstrDescription* contains a valid **BSTR** pointer.</span></span> <br/>  |
| <dl> <span data-ttu-id="e2db9-132"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e2db9-132"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e2db9-133">*hrStatus* è sconosciuto e non è disponibile alcuna descrizione.</span><span class="sxs-lookup"><span data-stu-id="e2db9-133">*hrStatus* is unknown and no description is available.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="e2db9-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2db9-134">Requirements</span></span>



| <span data-ttu-id="e2db9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2db9-135">Requirement</span></span> | <span data-ttu-id="e2db9-136">Valore</span><span class="sxs-lookup"><span data-stu-id="e2db9-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2db9-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2db9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e2db9-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2db9-138">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e2db9-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2db9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e2db9-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2db9-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e2db9-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2db9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2db9-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2db9-142"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="e2db9-143">IDL</span><span class="sxs-lookup"><span data-stu-id="e2db9-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2db9-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2db9-144"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="e2db9-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="e2db9-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2db9-146"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2db9-146"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
