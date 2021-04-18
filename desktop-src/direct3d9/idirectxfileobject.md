---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileObject per recuperare informazioni sugli oggetti file Microsoft DirectX. Deprecato.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Interfaccia IDirectXFileObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322533"
---
# <a name="idirectxfileobject-interface"></a><span data-ttu-id="33ec0-104">Interfaccia IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="33ec0-104">IDirectXFileObject interface</span></span>

<span data-ttu-id="33ec0-105">Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileObject per recuperare informazioni sugli oggetti file Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="33ec0-105">Applications use the methods of the IDirectXFileObject interface to retrieve information about Microsoft DirectX file objects.</span></span> <span data-ttu-id="33ec0-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="33ec0-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="33ec0-107">Membri</span><span class="sxs-lookup"><span data-stu-id="33ec0-107">Members</span></span>

<span data-ttu-id="33ec0-108">L'interfaccia **IDirectXFileObject** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="33ec0-108">The **IDirectXFileObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="33ec0-109">**IDirectXFileObject** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="33ec0-109">**IDirectXFileObject** also has these types of members:</span></span>

-   [<span data-ttu-id="33ec0-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="33ec0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="33ec0-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="33ec0-111">Methods</span></span>

<span data-ttu-id="33ec0-112">L'interfaccia **IDirectXFileObject** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="33ec0-112">The **IDirectXFileObject** interface has these methods.</span></span>



| <span data-ttu-id="33ec0-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="33ec0-113">Method</span></span>                                         | <span data-ttu-id="33ec0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33ec0-114">Description</span></span>                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33ec0-115">**GetId**</span><span class="sxs-lookup"><span data-stu-id="33ec0-115">**GetId**</span></span>](idirectxfileobject--getid.md)     | <span data-ttu-id="33ec0-116">Recupera un puntatore al GUID che identifica un oggetto file DirectX.</span><span class="sxs-lookup"><span data-stu-id="33ec0-116">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="33ec0-117">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="33ec0-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="33ec0-118">**GetName**</span><span class="sxs-lookup"><span data-stu-id="33ec0-118">**GetName**</span></span>](idirectxfileobject--getname.md) | <span data-ttu-id="33ec0-119">Recupera un puntatore al nome di un oggetto file DirectX.</span><span class="sxs-lookup"><span data-stu-id="33ec0-119">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="33ec0-120">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="33ec0-120">Deprecated.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="33ec0-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="33ec0-121">Remarks</span></span>

<span data-ttu-id="33ec0-122">Il GUID per l'interfaccia IDirectXFileObject è IID \_ IDirectXFileObject.</span><span class="sxs-lookup"><span data-stu-id="33ec0-122">The GUID for the IDirectXFileObject interface is IID\_IDirectXFileObject.</span></span>

<span data-ttu-id="33ec0-123">Il tipo LPDIRECTXFILEOBJECT è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="33ec0-123">The LPDIRECTXFILEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="33ec0-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33ec0-124">Requirements</span></span>



| <span data-ttu-id="33ec0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ec0-125">Requirement</span></span> | <span data-ttu-id="33ec0-126">Valore</span><span class="sxs-lookup"><span data-stu-id="33ec0-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33ec0-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33ec0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="33ec0-128"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="33ec0-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="33ec0-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="33ec0-129">Library</span></span><br/> | <dl> <span data-ttu-id="33ec0-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33ec0-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ec0-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33ec0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ec0-132">Interfacce di file X</span><span class="sxs-lookup"><span data-stu-id="33ec0-132">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
