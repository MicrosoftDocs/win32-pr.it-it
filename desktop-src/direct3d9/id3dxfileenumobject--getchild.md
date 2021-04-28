---
description: 'Metodo ID3DXFileEnumObject::GetChild: recupera un oggetto figlio in questo oggetto dati file.'
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: Metodo ID3DXFileEnumObject::GetChild (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b26cf058b31d1016c68cccf3dde6ade9f84cde1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090359"
---
# <a name="id3dxfileenumobjectgetchild-method"></a><span data-ttu-id="58619-103">Metodo ID3DXFileEnumObject::GetChild</span><span class="sxs-lookup"><span data-stu-id="58619-103">ID3DXFileEnumObject::GetChild method</span></span>

<span data-ttu-id="58619-104">Recupera un oggetto figlio in questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="58619-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="58619-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58619-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="58619-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58619-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58619-107">*id* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58619-107">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58619-108">Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58619-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58619-109">ID dell'oggetto figlio da recuperare.</span><span class="sxs-lookup"><span data-stu-id="58619-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="58619-110">*ppObj* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="58619-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58619-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="58619-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="58619-112">Indirizzo di un puntatore a ricevere il puntatore a interfaccia dell'oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="58619-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58619-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58619-113">Return value</span></span>

<span data-ttu-id="58619-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58619-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58619-115">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58619-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="58619-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="58619-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="58619-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58619-117">Requirements</span></span>



| <span data-ttu-id="58619-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="58619-118">Requirement</span></span> | <span data-ttu-id="58619-119">Valore</span><span class="sxs-lookup"><span data-stu-id="58619-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58619-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58619-120">Header</span></span><br/>  | <dl> <span data-ttu-id="58619-121"><dt>D3DX9Xof.h</dt></span><span class="sxs-lookup"><span data-stu-id="58619-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="58619-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="58619-122">Library</span></span><br/> | <dl> <span data-ttu-id="58619-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="58619-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="58619-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58619-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58619-125">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="58619-125">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
