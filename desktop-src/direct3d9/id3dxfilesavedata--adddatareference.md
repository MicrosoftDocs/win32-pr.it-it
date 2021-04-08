---
description: Aggiunge un riferimento ai dati come figlio del nodo dati del file ID3DXFileSaveData. Il riferimento ai dati punta a un oggetto dati di file.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'Metodo ID3DXFileSaveData:: AddDataReference (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969408"
---
# <a name="id3dxfilesavedataadddatareference-method"></a><span data-ttu-id="b1bfb-104">Metodo ID3DXFileSaveData:: AddDataReference</span><span class="sxs-lookup"><span data-stu-id="b1bfb-104">ID3DXFileSaveData::AddDataReference method</span></span>

<span data-ttu-id="b1bfb-105">Aggiunge un riferimento ai dati come figlio del nodo dati del file [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="b1bfb-105">Adds a data reference as a child of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span> <span data-ttu-id="b1bfb-106">Il riferimento ai dati punta a un oggetto dati di file.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-106">The data reference points to a file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1bfb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1bfb-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a><span data-ttu-id="b1bfb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1bfb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1bfb-109">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1bfb-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bfb-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1bfb-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1bfb-111">Puntatore al nome dell'oggetto dati da aggiungere per riferimento.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-111">Pointer to the name of the data object to add by reference.</span></span> <span data-ttu-id="b1bfb-112">Specificare **null** se l'oggetto dati non ha un nome.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-112">Specify **NULL** if the data object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="b1bfb-113">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1bfb-113">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bfb-114">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="b1bfb-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="b1bfb-115">Puntatore a un GUID che rappresenta l'oggetto dati da aggiungere per riferimento.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-115">Pointer to a GUID representing the data object to add by reference.</span></span> <span data-ttu-id="b1bfb-116">Se **null**, verrà aggiunto un riferimento che punta all'oggetto dati con il nome specificato da szName.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-116">If **NULL**, a reference will be added that points to the data object with the name given by szName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1bfb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1bfb-117">Return value</span></span>

<span data-ttu-id="b1bfb-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1bfb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1bfb-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b1bfb-120">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-120">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1bfb-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1bfb-121">Remarks</span></span>

<span data-ttu-id="b1bfb-122">L'oggetto dati di file a cui si fa riferimento deve avere un nome o un GUID.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-122">The file data object being referenced must have either a name or a GUID.</span></span> <span data-ttu-id="b1bfb-123">L'oggetto dati del file deve anche derivare da un altro oggetto padre [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="b1bfb-123">The file data object must also derive from a different parent [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1bfb-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1bfb-124">Requirements</span></span>



| <span data-ttu-id="b1bfb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1bfb-125">Requirement</span></span> | <span data-ttu-id="b1bfb-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b1bfb-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1bfb-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1bfb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b1bfb-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1bfb-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="b1bfb-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="b1bfb-129">Library</span></span><br/> | <dl> <span data-ttu-id="b1bfb-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1bfb-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b1bfb-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1bfb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bfb-132">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="b1bfb-132">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
