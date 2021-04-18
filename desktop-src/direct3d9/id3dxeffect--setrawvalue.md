---
description: Impostare un intervallo contiguo di costanti dello shader con una copia di memoria.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'Metodo ID3DXEffect:: SetRawValue (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322353"
---
# <a name="id3dxeffectsetrawvalue-method"></a><span data-ttu-id="b8b63-103">Metodo ID3DXEffect:: SetRawValue</span><span class="sxs-lookup"><span data-stu-id="b8b63-103">ID3DXEffect::SetRawValue method</span></span>

<span data-ttu-id="b8b63-104">Impostare un intervallo contiguo di costanti dello shader con una copia di memoria.</span><span class="sxs-lookup"><span data-stu-id="b8b63-104">Set a contiguous range of shader constants with a memory copy.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b63-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8b63-105">Syntax</span></span>


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="b8b63-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8b63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b63-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8b63-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b63-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b8b63-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b8b63-109">Handle per il valore da impostare o il nome del valore passato come stringa.</span><span class="sxs-lookup"><span data-stu-id="b8b63-109">Handle to the value to set, or the name of the value passed in as a string.</span></span> <span data-ttu-id="b8b63-110">Il passaggio di un handle è più efficiente.</span><span class="sxs-lookup"><span data-stu-id="b8b63-110">Passing in a handle is more efficient.</span></span> <span data-ttu-id="b8b63-111">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b8b63-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b63-112">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8b63-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b63-113">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="b8b63-113">Type: **void\***</span></span>

<span data-ttu-id="b8b63-114">Puntatore a un buffer contenente i dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="b8b63-114">Pointer to a buffer containing the data to be set.</span></span> <span data-ttu-id="b8b63-115">SetRawValue verifica la presenza di memoria valida, ma non esegue alcuna verifica dei dati validi.</span><span class="sxs-lookup"><span data-stu-id="b8b63-115">SetRawValue checks for valid memory, but does not do any checking for valid data.</span></span>

</dd> <dt>

<span data-ttu-id="b8b63-116">*OffsetInBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8b63-116">*OffsetInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b63-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8b63-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8b63-118">Numero di byte compresi tra l'inizio dei dati degli effetti e l'inizio delle costanti degli effetti che si intende impostare.</span><span class="sxs-lookup"><span data-stu-id="b8b63-118">Number of bytes between the beginning of the effect data and the beginning of the effect constants you are going to set.</span></span>

</dd> <dt>

<span data-ttu-id="b8b63-119">*Byte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8b63-119">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b63-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8b63-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8b63-121">Dimensioni del buffer da impostare, in byte.</span><span class="sxs-lookup"><span data-stu-id="b8b63-121">The size of the buffer to be set, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8b63-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8b63-122">Return value</span></span>

<span data-ttu-id="b8b63-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8b63-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8b63-124">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8b63-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b8b63-125">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: E \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b8b63-125">If the method fails, the return value can be one of the following:E\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8b63-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8b63-126">Remarks</span></span>

<span data-ttu-id="b8b63-127">SetRawValue è un modo molto rapido per impostare le costanti degli effetti poiché esegue una copia di memoria senza eseguire la convalida o la conversione dei dati, ad esempio la conversione di una matrice row-major in una matrice column-major.</span><span class="sxs-lookup"><span data-stu-id="b8b63-127">SetRawValue is a very fast way to set effect constants since it performs a memory copy without performing validation or any data conversion (like converting a row-major matrix to a column-major matrix).</span></span> <span data-ttu-id="b8b63-128">Usare SetRawValue per impostare una serie di costanti di effetto contigue.</span><span class="sxs-lookup"><span data-stu-id="b8b63-128">Use SetRawValue to set a series of contiguous effect constants.</span></span> <span data-ttu-id="b8b63-129">Ad esempio, è possibile impostare una matrice di venti matrici con 20 chiamate a [**ID3DXBaseEffect:: sematrix**](id3dxbaseeffect--setmatrix.md) o usando un singolo SetRawValue.</span><span class="sxs-lookup"><span data-stu-id="b8b63-129">For instance, you could set an array of twenty matrices with 20 calls to [**ID3DXBaseEffect::SetMatrix**](id3dxbaseeffect--setmatrix.md) or by using a single SetRawValue.</span></span>

<span data-ttu-id="b8b63-130">Si prevede che tutti i valori siano matrix4x4s o float4s e che tutte le matrici siano in ordine colonna-Major.</span><span class="sxs-lookup"><span data-stu-id="b8b63-130">All values are expected to be either matrix4x4s or float4s and all matrices are expected to be in column-major order.</span></span> <span data-ttu-id="b8b63-131">Viene eseguito il cast dei valori int o float in un float4; è quindi consigliabile usare SetRawValue solo con i dati float4 o matrix4x4.</span><span class="sxs-lookup"><span data-stu-id="b8b63-131">Int or float values are cast into a float4; therefore, it is highly recommended that you use SetRawValue with only float4 or matrix4x4 data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b63-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8b63-132">Requirements</span></span>



| <span data-ttu-id="b8b63-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8b63-133">Requirement</span></span> | <span data-ttu-id="b8b63-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b8b63-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b63-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8b63-135">Header</span></span><br/>  | <dl> <span data-ttu-id="b8b63-136"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8b63-136"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b8b63-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="b8b63-137">Library</span></span><br/> | <dl> <span data-ttu-id="b8b63-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8b63-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b8b63-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8b63-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b63-140">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="b8b63-140">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
