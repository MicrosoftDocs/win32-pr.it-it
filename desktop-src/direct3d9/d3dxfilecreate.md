---
description: Crea un'istanza di un oggetto ID3DXFile.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: Funzione D3DXFileCreate (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132342"
---
# <a name="d3dxfilecreate-function"></a><span data-ttu-id="dec05-103">D3DXFileCreate (funzione)</span><span class="sxs-lookup"><span data-stu-id="dec05-103">D3DXFileCreate function</span></span>

<span data-ttu-id="dec05-104">Crea un'istanza di un oggetto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="dec05-104">Creates an instance of an [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec05-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dec05-105">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="dec05-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dec05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec05-107">*lplpDirectXFile*</span><span class="sxs-lookup"><span data-stu-id="dec05-107">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="dec05-108">Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="dec05-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="dec05-109">Indirizzo di un puntatore a un'interfaccia [**ID3DXFile**](id3dxfile.md) , che rappresenta l'oggetto file con estensione x creato.</span><span class="sxs-lookup"><span data-stu-id="dec05-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the created .x file object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dec05-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dec05-110">Return value</span></span>

<span data-ttu-id="dec05-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dec05-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dec05-112">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dec05-112">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dec05-113">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: E \_ pointer, e \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="dec05-113">If the function fails, the return value can be one of the following: E\_POINTER, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dec05-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="dec05-114">Remarks</span></span>

<span data-ttu-id="dec05-115">Dopo aver utilizzato questa funzione, utilizzare [**RegisterTemplates**](id3dxfile--registertemplates.md) o [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) per registrare i modelli, [**CreateEnumObject**](id3dxfile--createenumobject.md) per creare un oggetto enumeratore o [**CreateSaveObject**](id3dxfile--createsaveobject.md) per creare un oggetto Save.</span><span class="sxs-lookup"><span data-stu-id="dec05-115">After using this function, use [**RegisterTemplates**](id3dxfile--registertemplates.md) or [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) to register templates, [**CreateEnumObject**](id3dxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](id3dxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec05-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dec05-116">Requirements</span></span>



| <span data-ttu-id="dec05-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec05-117">Requirement</span></span> | <span data-ttu-id="dec05-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dec05-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dec05-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dec05-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dec05-120"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="dec05-120"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="dec05-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="dec05-121">Library</span></span><br/> | <dl> <span data-ttu-id="dec05-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dec05-122"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dec05-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dec05-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec05-124">Funzioni file D3DX X</span><span class="sxs-lookup"><span data-stu-id="dec05-124">D3DX X File Functions</span></span>](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="dec05-125">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="dec05-125">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="dec05-126">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="dec05-126">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="dec05-127">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="dec05-127">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[<span data-ttu-id="dec05-128">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="dec05-128">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




