---
description: Crea un'istanza di un oggetto DirectXFile. Deprecato.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: Funzione DirectXFileCreate (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322296"
---
# <a name="directxfilecreate-function"></a><span data-ttu-id="04ea9-104">DirectXFileCreate (funzione)</span><span class="sxs-lookup"><span data-stu-id="04ea9-104">DirectXFileCreate function</span></span>

<span data-ttu-id="04ea9-105">Crea un'istanza di un oggetto DirectXFile.</span><span class="sxs-lookup"><span data-stu-id="04ea9-105">Creates an instance of a DirectXFile object.</span></span> <span data-ttu-id="04ea9-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="04ea9-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ea9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04ea9-107">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="04ea9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="04ea9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04ea9-109">*lplpDirectXFile*</span><span class="sxs-lookup"><span data-stu-id="04ea9-109">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="04ea9-110">Tipo: **[ **LPDIRECTXFILE**](idirectxfile.md)\***</span><span class="sxs-lookup"><span data-stu-id="04ea9-110">Type: **[**LPDIRECTXFILE**](idirectxfile.md)\***</span></span>

<span data-ttu-id="04ea9-111">Indirizzo di un puntatore a un'interfaccia [**IDirectXFile**](idirectxfile.md) , che rappresenta l'oggetto DirectXFile creato.</span><span class="sxs-lookup"><span data-stu-id="04ea9-111">Address of a pointer to an [**IDirectXFile**](idirectxfile.md) interface, representing the created DirectXFile object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04ea9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04ea9-112">Return value</span></span>

<span data-ttu-id="04ea9-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04ea9-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04ea9-114">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04ea9-114">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="04ea9-115">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="04ea9-115">If the function fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="04ea9-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="04ea9-116">Remarks</span></span>

<span data-ttu-id="04ea9-117">Dopo aver usato questa funzione, usare [**RegisterTemplates**](idirectxfile--registertemplates.md) per registrare i modelli, [**CreateEnumObject**](idirectxfile--createenumobject.md) per creare un oggetto enumeratore o [**CreateSaveObject**](idirectxfile--createsaveobject.md) per creare un oggetto Save.</span><span class="sxs-lookup"><span data-stu-id="04ea9-117">After using this function, use [**RegisterTemplates**](idirectxfile--registertemplates.md) to register templates, [**CreateEnumObject**](idirectxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](idirectxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ea9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04ea9-118">Requirements</span></span>



| <span data-ttu-id="04ea9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ea9-119">Requirement</span></span> | <span data-ttu-id="04ea9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="04ea9-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04ea9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04ea9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="04ea9-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="04ea9-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="04ea9-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="04ea9-123">Library</span></span><br/> | <dl> <span data-ttu-id="04ea9-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04ea9-124"><dt>D3dxof.lib</dt></span></span> </dl> |
| <span data-ttu-id="04ea9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="04ea9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="04ea9-126"><dt>D3dxof.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04ea9-126"><dt>D3dxof.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ea9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04ea9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ea9-128">Funzioni file X</span><span class="sxs-lookup"><span data-stu-id="04ea9-128">X File Functions</span></span>](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="04ea9-129">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="04ea9-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="04ea9-130">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="04ea9-130">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="04ea9-131">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="04ea9-131">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




