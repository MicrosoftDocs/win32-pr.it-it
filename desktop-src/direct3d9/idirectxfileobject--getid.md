---
description: Recupera un puntatore al GUID che identifica un oggetto file DirectX. Deprecato.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'Metodo IDirectXFileObject:: GetId (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322536"
---
# <a name="idirectxfileobjectgetid-method"></a><span data-ttu-id="e258d-104">Metodo IDirectXFileObject:: GetId</span><span class="sxs-lookup"><span data-stu-id="e258d-104">IDirectXFileObject::GetId method</span></span>

<span data-ttu-id="e258d-105">Recupera un puntatore al GUID che identifica un oggetto file DirectX.</span><span class="sxs-lookup"><span data-stu-id="e258d-105">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="e258d-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e258d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="e258d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e258d-107">Syntax</span></span>


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="e258d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e258d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e258d-109">*pGuid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e258d-109">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e258d-110">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="e258d-110">Type: **LPGUID**</span></span>

<span data-ttu-id="e258d-111">Puntatore a un GUID per ricevere l'ID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e258d-111">Pointer to a GUID to receive the object's ID.</span></span> <span data-ttu-id="e258d-112">La funzione imposterà il GUID su un GUID **null** se l'oggetto non dispone di un ID.</span><span class="sxs-lookup"><span data-stu-id="e258d-112">The function will set the GUID to a **NULL** GUID if the object does not have an ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e258d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e258d-113">Return value</span></span>

<span data-ttu-id="e258d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e258d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e258d-115">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e258d-115">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="e258d-116">Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="e258d-116">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e258d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e258d-117">Requirements</span></span>



| <span data-ttu-id="e258d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e258d-118">Requirement</span></span> | <span data-ttu-id="e258d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e258d-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e258d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e258d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e258d-121"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="e258d-121"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="e258d-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="e258d-122">Library</span></span><br/> | <dl> <span data-ttu-id="e258d-123"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e258d-123"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e258d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e258d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e258d-125">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="e258d-125">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 




