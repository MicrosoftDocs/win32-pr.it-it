---
description: Recupera il GUID del modello dell'oggetto. Deprecato.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'Metodo IDirectXFileData:: GetType (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 463391c661b2d166a6fba773e3b01590daf0ebd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132378"
---
# <a name="idirectxfiledatagettype-method"></a><span data-ttu-id="d49dd-104">Metodo IDirectXFileData:: GetType</span><span class="sxs-lookup"><span data-stu-id="d49dd-104">IDirectXFileData::GetType method</span></span>

<span data-ttu-id="d49dd-105">Recupera il GUID del modello dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d49dd-105">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="d49dd-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="d49dd-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d49dd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d49dd-107">Syntax</span></span>


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a><span data-ttu-id="d49dd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d49dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d49dd-109">*ppGUID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d49dd-109">*ppguid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d49dd-110">Tipo: **[**GUID**](guid.md) \* \* const**</span><span class="sxs-lookup"><span data-stu-id="d49dd-110">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="d49dd-111">Indirizzo di un puntatore per ricevere il GUID del modello dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d49dd-111">Address of a pointer to receive the GUID of the object's template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d49dd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d49dd-112">Return value</span></span>

<span data-ttu-id="d49dd-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d49dd-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d49dd-114">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d49dd-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="d49dd-115">Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d49dd-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d49dd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d49dd-116">Requirements</span></span>



| <span data-ttu-id="d49dd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d49dd-117">Requirement</span></span> | <span data-ttu-id="d49dd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d49dd-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d49dd-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d49dd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d49dd-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d49dd-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d49dd-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d49dd-121">Library</span></span><br/> | <dl> <span data-ttu-id="d49dd-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d49dd-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d49dd-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d49dd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d49dd-124">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="d49dd-124">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 




