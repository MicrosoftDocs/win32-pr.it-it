---
description: Recupera un oggetto figlio in questo oggetto dati del file.
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: 'Metodo ID3DXFileEnumObject:: GetChild (D3DX9Xof. h)'
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
ms.openlocfilehash: b5b8d535a9060e80318d4043af6362810023b9d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323065"
---
# <a name="id3dxfileenumobjectgetchild-method"></a><span data-ttu-id="f1e2a-103">Metodo ID3DXFileEnumObject:: GetChild</span><span class="sxs-lookup"><span data-stu-id="f1e2a-103">ID3DXFileEnumObject::GetChild method</span></span>

<span data-ttu-id="f1e2a-104">Recupera un oggetto figlio in questo oggetto dati del file.</span><span class="sxs-lookup"><span data-stu-id="f1e2a-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e2a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1e2a-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="f1e2a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1e2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1e2a-107">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1e2a-107">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1e2a-108">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1e2a-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1e2a-109">ID dell'oggetto figlio da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f1e2a-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f1e2a-110">*ppObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f1e2a-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1e2a-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f1e2a-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="f1e2a-112">Indirizzo di un puntatore per la ricezione del puntatore a interfaccia dell'oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="f1e2a-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1e2a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1e2a-113">Return value</span></span>

<span data-ttu-id="f1e2a-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1e2a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1e2a-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f1e2a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f1e2a-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="f1e2a-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e2a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1e2a-117">Requirements</span></span>



| <span data-ttu-id="f1e2a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1e2a-118">Requirement</span></span> | <span data-ttu-id="f1e2a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e2a-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e2a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1e2a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f1e2a-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1e2a-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="f1e2a-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="f1e2a-122">Library</span></span><br/> | <dl> <span data-ttu-id="f1e2a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1e2a-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f1e2a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1e2a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e2a-125">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="f1e2a-125">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
