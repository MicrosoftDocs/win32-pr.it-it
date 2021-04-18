---
description: L'interfaccia ID3DXBuffer viene utilizzata come buffer di dati, archiviando vertici, adiacenza e informazioni sul materiale durante le operazioni di ottimizzazione e caricamento della rete.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Interfaccia ID3DXBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322841"
---
# <a name="id3dxbuffer-interface"></a><span data-ttu-id="720c9-103">Interfaccia ID3DXBuffer</span><span class="sxs-lookup"><span data-stu-id="720c9-103">ID3DXBuffer interface</span></span>

<span data-ttu-id="720c9-104">L'interfaccia ID3DXBuffer viene utilizzata come buffer di dati, archiviando vertici, adiacenza e informazioni sul materiale durante le operazioni di ottimizzazione e caricamento della rete.</span><span class="sxs-lookup"><span data-stu-id="720c9-104">The ID3DXBuffer interface is used as a data buffer, storing vertex, adjacency, and material information during mesh optimization and loading operations.</span></span> <span data-ttu-id="720c9-105">L'oggetto buffer viene utilizzato per restituire dati di lunghezza arbitraria.</span><span class="sxs-lookup"><span data-stu-id="720c9-105">The buffer object is used to return arbitrary length data.</span></span> <span data-ttu-id="720c9-106">Inoltre, gli oggetti buffer vengono utilizzati per restituire il codice oggetto e i messaggi di errore nei metodi che assemblano vertex shader e pixel shader.</span><span class="sxs-lookup"><span data-stu-id="720c9-106">Also, buffer objects are used to return object code and error messages in methods that assemble vertex and pixel shaders.</span></span>

## <a name="members"></a><span data-ttu-id="720c9-107">Membri</span><span class="sxs-lookup"><span data-stu-id="720c9-107">Members</span></span>

<span data-ttu-id="720c9-108">L'interfaccia **ID3DXBuffer** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="720c9-108">The **ID3DXBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="720c9-109">**ID3DXBuffer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="720c9-109">**ID3DXBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="720c9-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="720c9-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="720c9-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="720c9-111">Methods</span></span>

<span data-ttu-id="720c9-112">L'interfaccia **ID3DXBuffer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="720c9-112">The **ID3DXBuffer** interface has these methods.</span></span>



| <span data-ttu-id="720c9-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="720c9-113">Method</span></span>                                                    | <span data-ttu-id="720c9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="720c9-114">Description</span></span>                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="720c9-115">**GetBufferPointer**</span><span class="sxs-lookup"><span data-stu-id="720c9-115">**GetBufferPointer**</span></span>](id3dxbuffer--getbufferpointer.md) | <span data-ttu-id="720c9-116">Recupera un puntatore ai dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="720c9-116">Retrieves a pointer to the data in the buffer.</span></span><br/>      |
| [<span data-ttu-id="720c9-117">**GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="720c9-117">**GetBufferSize**</span></span>](id3dxbuffer--getbuffersize.md)       | <span data-ttu-id="720c9-118">Recupera le dimensioni totali dei dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="720c9-118">Retrieves the total size of the data in the buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="720c9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="720c9-119">Remarks</span></span>

<span data-ttu-id="720c9-120">L'interfaccia **ID3DXBuffer** viene ottenuta chiamando la funzione [**D3DXCreateBuffer**](d3dxcreatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="720c9-120">The **ID3DXBuffer** interface is obtained by calling the [**D3DXCreateBuffer**](d3dxcreatebuffer.md) function.</span></span>

<span data-ttu-id="720c9-121">Il tipo LPD3DXBUFFER è definito come puntatore all'interfaccia **ID3DXBuffer** .</span><span class="sxs-lookup"><span data-stu-id="720c9-121">The LPD3DXBUFFER type is defined as a pointer to the **ID3DXBuffer** interface.</span></span>


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="720c9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="720c9-122">Requirements</span></span>



| <span data-ttu-id="720c9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="720c9-123">Requirement</span></span> | <span data-ttu-id="720c9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="720c9-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="720c9-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="720c9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="720c9-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="720c9-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="720c9-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="720c9-127">Library</span></span><br/> | <dl> <span data-ttu-id="720c9-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="720c9-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="720c9-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="720c9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="720c9-130">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="720c9-130">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
