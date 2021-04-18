---
description: Recupera l'oggetto dati con il nome specificato.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'Metodo ID3DXFileEnumObject:: GetDataObjectByName (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41850615726ac15e890162c6e28df9b638c582a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323062"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="ce4d5-103">Metodo ID3DXFileEnumObject:: GetDataObjectByName</span><span class="sxs-lookup"><span data-stu-id="ce4d5-103">ID3DXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="ce4d5-104">Recupera l'oggetto dati con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="ce4d5-104">Retrieves the data object that has the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce4d5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce4d5-105">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="ce4d5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce4d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce4d5-107">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce4d5-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce4d5-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce4d5-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce4d5-109">Puntatore al nome richiesto.</span><span class="sxs-lookup"><span data-stu-id="ce4d5-109">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="ce4d5-110">*ppObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ce4d5-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce4d5-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ce4d5-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="ce4d5-112">Indirizzo di un puntatore a un'interfaccia [**ID3DXFileData**](id3dxfiledata.md) , che rappresenta l'oggetto dati di file restituito.</span><span class="sxs-lookup"><span data-stu-id="ce4d5-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce4d5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce4d5-113">Return value</span></span>

<span data-ttu-id="ce4d5-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce4d5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce4d5-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce4d5-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ce4d5-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="ce4d5-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce4d5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce4d5-117">Remarks</span></span>

<span data-ttu-id="ce4d5-118">Ottenere il nome szName dell'oggetto dati del file corrente con il metodo [**ID3DXFileData:: GetName**](id3dxfiledata--getname.md) .</span><span class="sxs-lookup"><span data-stu-id="ce4d5-118">Obtain the name szName of the current file data object with the [**ID3DXFileData::GetName**](id3dxfiledata--getname.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4d5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce4d5-119">Requirements</span></span>



| <span data-ttu-id="ce4d5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce4d5-120">Requirement</span></span> | <span data-ttu-id="ce4d5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ce4d5-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4d5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce4d5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ce4d5-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce4d5-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="ce4d5-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce4d5-124">Library</span></span><br/> | <dl> <span data-ttu-id="ce4d5-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce4d5-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ce4d5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce4d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce4d5-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="ce4d5-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
