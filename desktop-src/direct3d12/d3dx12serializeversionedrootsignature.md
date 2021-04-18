---
title: Funzione D3DX12SerializeVersionedRootSignature (D3dx12. h)
description: Consente di abilitare le funzionalità della firma radice 1,1 quando sono disponibili e non richiede la gestione di due percorsi di codice per la creazione di firme radice. Questo metodo helper ricostruisce una firma radice della versione 1,0 quando la versione 1,1 non è supportata.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- D3DX12SerializeVersionedRootSignature (funzione)
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322166"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a><span data-ttu-id="be621-105">D3DX12SerializeVersionedRootSignature (funzione)</span><span class="sxs-lookup"><span data-stu-id="be621-105">D3DX12SerializeVersionedRootSignature function</span></span>

<span data-ttu-id="be621-106">Consente di abilitare le funzionalità della firma radice 1,1 quando sono disponibili e non richiede la gestione di due percorsi di codice per la creazione di firme radice.</span><span class="sxs-lookup"><span data-stu-id="be621-106">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="be621-107">Questo metodo helper ricostruisce una firma radice della versione 1,0 quando la versione 1,1 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="be621-107">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="be621-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be621-108">Syntax</span></span>


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="be621-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="be621-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be621-110">*pRootSignatureDesc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be621-110">*pRootSignatureDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be621-111">Tipo: **const D3D12 \_ versione \_ della \_ firma \_ radice \* desc**</span><span class="sxs-lookup"><span data-stu-id="be621-111">Type: **const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC\***</span></span>

<span data-ttu-id="be621-112">Specifica una descrizione della [**\_ \_ firma radice \_ \_ con versione D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) che contiene una descrizione di qualsiasi versione di una firma radice.</span><span class="sxs-lookup"><span data-stu-id="be621-112">Specifies a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) that contains a description of any version of a root signature.</span></span>

</dd> <dt>

<span data-ttu-id="be621-113">*MaxVersion*</span><span class="sxs-lookup"><span data-stu-id="be621-113">*MaxVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="be621-114">Tipo: **\_ versione della \_ firma \_ radice D3D**</span><span class="sxs-lookup"><span data-stu-id="be621-114">Type: **D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>

<span data-ttu-id="be621-115">Specifica la versione massima supportata della [**\_ \_ firma \_ radice D3D**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span><span class="sxs-lookup"><span data-stu-id="be621-115">Specifies the maximum supported [**D3D\_ROOT\_SIGNATURE\_VERSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span></span>

</dd> <dt>

<span data-ttu-id="be621-116">*ppBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="be621-116">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be621-117">Tipo: **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="be621-117">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="be621-118">Puntatore a un blocco di memoria che riceve un puntatore all'interfaccia [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) che è possibile usare per accedere alla firma radice serializzata.</span><span class="sxs-lookup"><span data-stu-id="be621-118">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the serialized root signature.</span></span>

</dd> <dt>

<span data-ttu-id="be621-119">*ppErrorBlob* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="be621-119">*ppErrorBlob* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be621-120">Tipo: **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="be621-120">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="be621-121">Puntatore a un blocco di memoria che riceve un puntatore all'interfaccia [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) che è possibile utilizzare per accedere ai messaggi di errore del serializzatore oppure **null** se non sono presenti errori.</span><span class="sxs-lookup"><span data-stu-id="be621-121">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access serializer error messages, or **NULL** if there are no errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be621-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be621-122">Return value</span></span>

<span data-ttu-id="be621-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be621-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be621-124">Restituisce **\_ OK** se ha esito positivo; in caso contrario, restituisce uno dei [codici restituiti Direct3D 12](d3d12-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="be621-124">Returns **S\_OK** if successful; otherwise, returns one of the [Direct3D 12 Return Codes](d3d12-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be621-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="be621-125">Remarks</span></span>

<span data-ttu-id="be621-126">Questa funzione è stata rilasciata in concomitanza con l'aggiornamento dell'anniversario di Windows 10 (14393).</span><span class="sxs-lookup"><span data-stu-id="be621-126">This function was released to coincide with the Windows 10 Anniversary Update (14393).</span></span> <span data-ttu-id="be621-127">Per supportare versioni di Windows 10 precedenti, l'uso di questa funzione richiede la configurazione di d3d12. lib per il *caricamento ritardato*.</span><span class="sxs-lookup"><span data-stu-id="be621-127">In order to support Windows 10 versions prior to this, use of this function requires d3d12.lib be set up for *delay loading*.</span></span>

## <a name="requirements"></a><span data-ttu-id="be621-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be621-128">Requirements</span></span>



| <span data-ttu-id="be621-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="be621-129">Requirement</span></span> | <span data-ttu-id="be621-130">Valore</span><span class="sxs-lookup"><span data-stu-id="be621-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="be621-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be621-131">Header</span></span><br/>  | <dl> <span data-ttu-id="be621-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="be621-132"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="be621-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="be621-133">Library</span></span><br/> | <dl> <span data-ttu-id="be621-134"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be621-134"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="be621-135">DLL</span><span class="sxs-lookup"><span data-stu-id="be621-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="be621-136"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be621-136"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be621-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be621-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be621-138">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="be621-138">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[<span data-ttu-id="be621-139">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="be621-139">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

