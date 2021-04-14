---
description: Registra i modelli personalizzati, dato un oggetto di enumerazione ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'Metodo ID3DXFile:: RegisterEnumTemplates (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401988"
---
# <a name="id3dxfileregisterenumtemplates-method"></a><span data-ttu-id="1fcbd-103">Metodo ID3DXFile:: RegisterEnumTemplates</span><span class="sxs-lookup"><span data-stu-id="1fcbd-103">ID3DXFile::RegisterEnumTemplates method</span></span>

<span data-ttu-id="1fcbd-104">Registra i modelli personalizzati, dato un oggetto di enumerazione [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcbd-104">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fcbd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fcbd-105">Syntax</span></span>


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="1fcbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1fcbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fcbd-107">*pEnum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fcbd-107">*pEnum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcbd-108">Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="1fcbd-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span></span>

<span data-ttu-id="1fcbd-109">Puntatore a un oggetto di enumerazione [**ID3DXFileEnumObject**](id3dxfileenumobject.md) contenente i modelli.</span><span class="sxs-lookup"><span data-stu-id="1fcbd-109">Pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object that contains templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fcbd-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1fcbd-110">Return value</span></span>

<span data-ttu-id="1fcbd-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fcbd-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fcbd-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1fcbd-112">If the method succeeds, the return value is S\_OK .</span></span>

<span data-ttu-id="1fcbd-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="1fcbd-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fcbd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fcbd-114">Remarks</span></span>

<span data-ttu-id="1fcbd-115">Quando questo metodo viene chiamato, copia i modelli archiviati con ID3DXFileEnumObject, che rappresenta il file, nell'archivio dei modelli locale dell'oggetto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcbd-115">When this method is called, it copies templates stored with the ID3DXFileEnumObject, representing the file, to the local template store of the [**ID3DXFile**](id3dxfile.md) object.</span></span>

<span data-ttu-id="1fcbd-116">Se non è disponibile un puntatore [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , chiamare invece il metodo [**RegisterTemplates**](id3dxfile--registertemplates.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcbd-116">If an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) pointer is not available, call the [**RegisterTemplates**](id3dxfile--registertemplates.md) method instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcbd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fcbd-117">Requirements</span></span>



| <span data-ttu-id="1fcbd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fcbd-118">Requirement</span></span> | <span data-ttu-id="1fcbd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1fcbd-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcbd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1fcbd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1fcbd-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fcbd-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="1fcbd-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="1fcbd-122">Library</span></span><br/> | <dl> <span data-ttu-id="1fcbd-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fcbd-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1fcbd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fcbd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcbd-125">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="1fcbd-125">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="1fcbd-126">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="1fcbd-126">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




