---
title: Funzione D3D12DecomposeSubresource (D3dx12. h)
description: Restituisce la sezione MIP, la sezione della matrice e la sezione del piano che corrispondono all'indice della sottorisorsa specificata.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- D3D12DecomposeSubresource (funzione)
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322179"
---
# <a name="d3d12decomposesubresource-function"></a><span data-ttu-id="dd96a-104">D3D12DecomposeSubresource (funzione)</span><span class="sxs-lookup"><span data-stu-id="dd96a-104">D3D12DecomposeSubresource function</span></span>

<span data-ttu-id="dd96a-105">Restituisce la sezione MIP, la sezione della matrice e la sezione del piano che corrispondono all'indice della sottorisorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="dd96a-105">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd96a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd96a-106">Syntax</span></span>


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a><span data-ttu-id="dd96a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd96a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd96a-108">*Sottorisorsa*</span><span class="sxs-lookup"><span data-stu-id="dd96a-108">*Subresource*</span></span> 
</dt> <dd>

<span data-ttu-id="dd96a-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dd96a-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dd96a-110">Indice della sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="dd96a-110">The index of the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="dd96a-111">*MipLevels*</span><span class="sxs-lookup"><span data-stu-id="dd96a-111">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="dd96a-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dd96a-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dd96a-113">Numero massimo di livelli di mipmap nella sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="dd96a-113">The maximum number of mipmap levels in the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="dd96a-114">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="dd96a-114">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="dd96a-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dd96a-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dd96a-116">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="dd96a-116">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="dd96a-117">*MipSlice* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="dd96a-117">*MipSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dd96a-118">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="dd96a-118">Type: **T**</span></span>

<span data-ttu-id="dd96a-119">Restituisce la sezione MIP che corrisponde all'indice della sottorisorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="dd96a-119">Outputs the mip slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="dd96a-120">*ArraySlice* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="dd96a-120">*ArraySlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dd96a-121">Tipo: **U**</span><span class="sxs-lookup"><span data-stu-id="dd96a-121">Type: **U**</span></span>

<span data-ttu-id="dd96a-122">Restituisce la sezione della matrice che corrisponde all'indice della sottorisorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="dd96a-122">Outputs the array slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="dd96a-123">*PlaneSlice* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="dd96a-123">*PlaneSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dd96a-124">Tipo: **V**</span><span class="sxs-lookup"><span data-stu-id="dd96a-124">Type: **V**</span></span>

<span data-ttu-id="dd96a-125">Restituisce la sezione del piano che corrisponde all'indice della sottorisorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="dd96a-125">Outputs the plane slice that corresponds to the given subresource index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd96a-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd96a-126">Return value</span></span>

<span data-ttu-id="dd96a-127">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="dd96a-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd96a-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd96a-128">Remarks</span></span>

<span data-ttu-id="dd96a-129">Questa funzione determina quali sezioni MIP, sezione della matrice e sezione del piano corrispondono a un indice di sottorisorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="dd96a-129">This function determines which mip slice, array slice, and plane slice correspond to a given subresource index.</span></span> <span data-ttu-id="dd96a-130">Si tratta di un'utilità utile, sebbene sia specifica di C++.</span><span class="sxs-lookup"><span data-stu-id="dd96a-130">This is a useful utility, though it is C++ specific.</span></span>

<span data-ttu-id="dd96a-131">Questa funzione viene dichiarata come segue, con i parametri C++ creato un modello per i tipi **T**, **U** e **V**:</span><span class="sxs-lookup"><span data-stu-id="dd96a-131">This function is declared as follows, with C++ templatized parameters for types **T**, **U**, and **V**:</span></span>


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a><span data-ttu-id="dd96a-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd96a-132">Requirements</span></span>



| <span data-ttu-id="dd96a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd96a-133">Requirement</span></span> | <span data-ttu-id="dd96a-134">Valore</span><span class="sxs-lookup"><span data-stu-id="dd96a-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dd96a-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd96a-135">Header</span></span><br/>  | <dl> <span data-ttu-id="dd96a-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd96a-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="dd96a-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="dd96a-137">Library</span></span><br/> | <dl> <span data-ttu-id="dd96a-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd96a-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="dd96a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dd96a-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd96a-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd96a-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd96a-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd96a-141">See also</span></span>

[<span data-ttu-id="dd96a-142">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="dd96a-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)

[<span data-ttu-id="dd96a-143">Sottorisorse</span><span class="sxs-lookup"><span data-stu-id="dd96a-143">Subresources</span></span>](subresources.md)
