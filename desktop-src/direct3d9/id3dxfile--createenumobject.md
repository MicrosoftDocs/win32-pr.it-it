---
description: Crea un oggetto enumeratore in grado di leggere un file con estensione x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'Metodo ID3DXFile:: CreateEnumObject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323074"
---
# <a name="id3dxfilecreateenumobject-method"></a><span data-ttu-id="20a61-103">Metodo ID3DXFile:: CreateEnumObject</span><span class="sxs-lookup"><span data-stu-id="20a61-103">ID3DXFile::CreateEnumObject method</span></span>

<span data-ttu-id="20a61-104">Crea un oggetto enumeratore in grado di leggere un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="20a61-104">Creates an enumerator object that will read a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="20a61-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20a61-105">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="20a61-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20a61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20a61-107">*pvSource* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="20a61-107">*pvSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20a61-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20a61-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20a61-109">Origine dati.</span><span class="sxs-lookup"><span data-stu-id="20a61-109">The data source.</span></span> <span data-ttu-id="20a61-110">Una delle due versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="20a61-110">Either:</span></span>

-   <span data-ttu-id="20a61-111">Un nome file</span><span class="sxs-lookup"><span data-stu-id="20a61-111">A file name</span></span>
-   <span data-ttu-id="20a61-112">Struttura [**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)</span><span class="sxs-lookup"><span data-stu-id="20a61-112">A [**D3DXF\_FILELOADMEMORY**](d3dxf-fileloadmemory.md) structure</span></span>
-   <span data-ttu-id="20a61-113">Struttura [**D3DXF \_ FILELOADRESOURCE**](d3dxf-fileloadresource.md)</span><span class="sxs-lookup"><span data-stu-id="20a61-113">A [**D3DXF\_FILELOADRESOURCE**](d3dxf-fileloadresource.md) structure</span></span>

<span data-ttu-id="20a61-114">A seconda del valore di loadflags.</span><span class="sxs-lookup"><span data-stu-id="20a61-114">Depending on the value of loadflags.</span></span>

</dd> <dt>

<span data-ttu-id="20a61-115">*loadflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20a61-115">*loadflags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20a61-116">Tipo: **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="20a61-116">Type: **[D3DXF\_FILELOADOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="20a61-117">Valore che specifica l'origine dei dati.</span><span class="sxs-lookup"><span data-stu-id="20a61-117">Value that specifies the source of the data.</span></span> <span data-ttu-id="20a61-118">Questo valore può essere uno dei flag [ \_ FILELOADOPTIONS di D3DXF](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="20a61-118">This value can be one of the [D3DXF\_FILELOADOPTIONS](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="20a61-119">*ppEnumObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="20a61-119">*ppEnumObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20a61-120">Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="20a61-120">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="20a61-121">Indirizzo di un puntatore a un'interfaccia [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , che rappresenta l'oggetto enumeratore creato.</span><span class="sxs-lookup"><span data-stu-id="20a61-121">Address of a pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20a61-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20a61-122">Return value</span></span>

<span data-ttu-id="20a61-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20a61-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20a61-124">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20a61-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="20a61-125">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="20a61-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="20a61-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="20a61-126">Remarks</span></span>

<span data-ttu-id="20a61-127">Dopo aver utilizzato questo metodo, utilizzare uno dei metodi [**ID3DXFileEnumObject**](id3dxfileenumobject.md) per recuperare un oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="20a61-127">After using this method, use one of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="20a61-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20a61-128">Requirements</span></span>



| <span data-ttu-id="20a61-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="20a61-129">Requirement</span></span> | <span data-ttu-id="20a61-130">Valore</span><span class="sxs-lookup"><span data-stu-id="20a61-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20a61-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20a61-131">Header</span></span><br/>  | <dl> <span data-ttu-id="20a61-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="20a61-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="20a61-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="20a61-133">Library</span></span><br/> | <dl> <span data-ttu-id="20a61-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20a61-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="20a61-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20a61-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a61-136">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="20a61-136">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="20a61-137">**ID3DXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="20a61-137">**ID3DXFileEnumObject**</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
