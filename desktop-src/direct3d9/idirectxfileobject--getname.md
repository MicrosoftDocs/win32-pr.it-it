---
description: Recupera un puntatore al nome di un oggetto file DirectX. Deprecato.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'Metodo IDirectXFileObject:: GetName (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322534"
---
# <a name="idirectxfileobjectgetname-method"></a><span data-ttu-id="34192-104">Metodo IDirectXFileObject:: GetName</span><span class="sxs-lookup"><span data-stu-id="34192-104">IDirectXFileObject::GetName method</span></span>

<span data-ttu-id="34192-105">Recupera un puntatore al nome di un oggetto file DirectX.</span><span class="sxs-lookup"><span data-stu-id="34192-105">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="34192-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="34192-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="34192-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34192-107">Syntax</span></span>


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="34192-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="34192-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34192-109">*pstrNameBuf* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="34192-109">*pstrNameBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34192-110">Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34192-110">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34192-111">Puntatore al buffer in cui verrà copiato il nome dell'oggetto file DirectX.</span><span class="sxs-lookup"><span data-stu-id="34192-111">Pointer to the buffer in which the DirectX file object's name will be copied.</span></span> <span data-ttu-id="34192-112">Impostare su **null** se è necessaria solo la lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="34192-112">Set to **NULL** if only the buffer length is needed.</span></span>

</dd> <dt>

<span data-ttu-id="34192-113">*pdwBufLen* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="34192-113">*pdwBufLen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34192-114">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34192-114">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34192-115">Puntatore a un valore DWORD che specifica la lunghezza del buffer a cui punta pstrNameBuf.</span><span class="sxs-lookup"><span data-stu-id="34192-115">Pointer to a DWORD specifying the length of the buffer pointed to by pstrNameBuf.</span></span> <span data-ttu-id="34192-116">Il valore del parametro pdwBufLen verrà modificato in base alla lunghezza del buffer necessaria per contenere il nome dell'oggetto anche se pstrNameBuf è **null**.</span><span class="sxs-lookup"><span data-stu-id="34192-116">The pdwBufLen parameter value will be modified to the buffer length needed to hold the object's name even if pstrNameBuf is **NULL**.</span></span> <span data-ttu-id="34192-117">In entrambi i casi, la funzione restituirà DXFILEERR \_ BADVALUE se il valore originale di pdwBufLen non è grande o maggiore della lunghezza necessaria per conservare il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="34192-117">In either case, the function will return DXFILEERR\_BADVALUE if the original value of pdwBufLen is not as large as or larger than the length needed to hold the object's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34192-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34192-118">Return value</span></span>

<span data-ttu-id="34192-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="34192-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="34192-120">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="34192-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="34192-121">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="34192-121">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="34192-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34192-122">Requirements</span></span>



| <span data-ttu-id="34192-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="34192-123">Requirement</span></span> | <span data-ttu-id="34192-124">Valore</span><span class="sxs-lookup"><span data-stu-id="34192-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34192-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34192-125">Header</span></span><br/>  | <dl> <span data-ttu-id="34192-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="34192-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="34192-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="34192-127">Library</span></span><br/> | <dl> <span data-ttu-id="34192-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34192-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34192-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34192-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34192-130">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="34192-130">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 
