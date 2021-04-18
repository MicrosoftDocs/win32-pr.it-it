---
description: Accede ai dati del file con estensione x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'Metodo ID3DXFileData:: Lock (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 27ef18fcb12b00f0b778ee15d582610ffe52fe54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323068"
---
# <a name="id3dxfiledatalock-method"></a><span data-ttu-id="da7da-103">Metodo ID3DXFileData:: Lock</span><span class="sxs-lookup"><span data-stu-id="da7da-103">ID3DXFileData::Lock method</span></span>

<span data-ttu-id="da7da-104">Accede ai dati del file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="da7da-104">Accesses the .x file data.</span></span>

## <a name="syntax"></a><span data-ttu-id="da7da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da7da-105">Syntax</span></span>


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="da7da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da7da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da7da-107">*psize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da7da-107">*pSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da7da-108">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="da7da-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="da7da-109">Puntatore alla dimensione dei dati del file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="da7da-109">Pointer to the size of the .x file data.</span></span>

</dd> <dt>

<span data-ttu-id="da7da-110">*ppData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da7da-110">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da7da-111">Tipo: **const \* \* void**</span><span class="sxs-lookup"><span data-stu-id="da7da-111">Type: **const VOID\*\***</span></span>

<span data-ttu-id="da7da-112">Indirizzo di un puntatore per ricevere il puntatore all'interfaccia dell'oggetto dati del file [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="da7da-112">Address of a pointer to receive the [**ID3DXFileData**](id3dxfiledata.md) file data object's interface pointer.</span></span> <span data-ttu-id="da7da-113">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="da7da-113">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da7da-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da7da-114">Return value</span></span>

<span data-ttu-id="da7da-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da7da-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da7da-116">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da7da-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="da7da-117">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="da7da-117">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="da7da-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="da7da-118">Remarks</span></span>

<span data-ttu-id="da7da-119">Il puntatore *ppData* è valido solo durante un **ID3DXFileData:: Lock** ... Sequenza [**ID3DXFileData:: Unlock**](id3dxfiledata--unlock.md) .</span><span class="sxs-lookup"><span data-stu-id="da7da-119">The *ppData* pointer is only valid during a **ID3DXFileData::Lock** ... [**ID3DXFileData::Unlock**](id3dxfiledata--unlock.md) sequence.</span></span> <span data-ttu-id="da7da-120">È possibile effettuare più chiamate di blocco.</span><span class="sxs-lookup"><span data-stu-id="da7da-120">You can make multiple lock calls.</span></span> <span data-ttu-id="da7da-121">Tuttavia, è necessario assicurarsi che il numero di chiamate di blocco corrisponda al numero di chiamate di sblocco.</span><span class="sxs-lookup"><span data-stu-id="da7da-121">However, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="da7da-122">Poiché non è garantito che i dati del file siano allineati correttamente con i limiti di byte, è necessario accedere a *ppData* con puntatori non allineati.</span><span class="sxs-lookup"><span data-stu-id="da7da-122">Because file data is not guaranteed to be aligned properly with byte boundaries, you should access *ppData* with UNALIGNED pointers.</span></span>

<span data-ttu-id="da7da-123">Non è garantito che i valori dei parametri restituiti siano validi a causa del possibile danneggiamento del file. Pertanto, il codice deve verificare i valori dei parametri restituiti.</span><span class="sxs-lookup"><span data-stu-id="da7da-123">Returned parameter values are not guaranteed to be valid due to possible file corruption; therefore, your code should verify the returned parameter values.</span></span>

## <a name="requirements"></a><span data-ttu-id="da7da-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da7da-124">Requirements</span></span>



| <span data-ttu-id="da7da-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="da7da-125">Requirement</span></span> | <span data-ttu-id="da7da-126">Valore</span><span class="sxs-lookup"><span data-stu-id="da7da-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da7da-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da7da-127">Header</span></span><br/>  | <dl> <span data-ttu-id="da7da-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="da7da-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="da7da-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="da7da-129">Library</span></span><br/> | <dl> <span data-ttu-id="da7da-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da7da-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="da7da-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da7da-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da7da-132">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="da7da-132">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
