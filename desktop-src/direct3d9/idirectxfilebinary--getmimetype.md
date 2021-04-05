---
description: Recupera il tipo di Multipurpose Internet Mail Extensions (MIME) per i dati binari. Deprecato.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'Metodo IDirectXFileBinary:: GetMimeType (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969340"
---
# <a name="idirectxfilebinarygetmimetype-method"></a><span data-ttu-id="ed986-104">Metodo IDirectXFileBinary:: GetMimeType</span><span class="sxs-lookup"><span data-stu-id="ed986-104">IDirectXFileBinary::GetMimeType method</span></span>

<span data-ttu-id="ed986-105">Recupera il tipo di Multipurpose Internet Mail Extensions (MIME) per i dati binari.</span><span class="sxs-lookup"><span data-stu-id="ed986-105">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="ed986-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ed986-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed986-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed986-107">Syntax</span></span>


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a><span data-ttu-id="ed986-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed986-109">*pszMimeType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed986-109">*pszMimeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed986-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed986-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ed986-111">Indirizzo di un puntatore per la ricezione della stringa di tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="ed986-111">Address of a pointer to receive the MIME type string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed986-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed986-112">Return value</span></span>

<span data-ttu-id="ed986-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed986-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed986-114">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed986-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="ed986-115">Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="ed986-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed986-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed986-116">Remarks</span></span>

<span data-ttu-id="ed986-117">Quando non è specificato alcun tipo MIME in un file DirectX per un oggetto binario, la funzione imposterà pszMimeType su **null**.</span><span class="sxs-lookup"><span data-stu-id="ed986-117">When there is no MIME type specified in a DirectX file for a binary object, the function will set pszMimeType to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed986-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed986-118">Requirements</span></span>



| <span data-ttu-id="ed986-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed986-119">Requirement</span></span> | <span data-ttu-id="ed986-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ed986-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed986-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed986-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ed986-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed986-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed986-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="ed986-123">Library</span></span><br/> | <dl> <span data-ttu-id="ed986-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed986-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed986-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed986-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed986-126">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="ed986-126">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
