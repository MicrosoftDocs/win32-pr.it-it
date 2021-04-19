---
description: ID3DXInclude è un'interfaccia implementata dall'utente per fornire callback per le \# direttive include durante la compilazione dello shader.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interfaccia ID3DXInclude (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323531"
---
# <a name="id3dxinclude-interface"></a><span data-ttu-id="e9daa-103">Interfaccia ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="e9daa-103">ID3DXInclude interface</span></span>

<span data-ttu-id="e9daa-104">ID3DXInclude è un'interfaccia implementata dall'utente per fornire callback per le \# direttive include durante la compilazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="e9daa-104">ID3DXInclude is a user-implemented interface to provide callbacks for \#include directives during shader compilation.</span></span> <span data-ttu-id="e9daa-105">Ognuno dei metodi in questa interfaccia deve essere implementato dall'utente che verrà quindi utilizzato come callback all'applicazione quando si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9daa-105">Each of the methods in this interface must be implemented by the user which will then be used as callbacks to the application when one of the following occurs:</span></span>

-   <span data-ttu-id="e9daa-106">Uno shader HLSL che contiene un' \# inclusione viene compilato chiamando una delle \* \* \* funzioni D3DXCompileShader.</span><span class="sxs-lookup"><span data-stu-id="e9daa-106">An HLSL shader that contains a \#include is compiled by calling one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="e9daa-107">Un assembly shader \# include viene assemblato chiamando qualsiasi \* \* \* funzione D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="e9daa-107">An assembly shader \#include is assembled by calling any of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="e9daa-108">Un effetto che contiene un' \# inclusione viene compilato da chiamando una delle funzioni D3DXCreateEffect \* \* \* o D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="e9daa-108">An effect that contains a \#include is compiled by by calling any of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="members"></a><span data-ttu-id="e9daa-109">Membri</span><span class="sxs-lookup"><span data-stu-id="e9daa-109">Members</span></span>

<span data-ttu-id="e9daa-110">L'interfaccia **ID3DXInclude** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e9daa-110">The **ID3DXInclude** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e9daa-111">**ID3DXInclude** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e9daa-111">**ID3DXInclude** also has these types of members:</span></span>

-   [<span data-ttu-id="e9daa-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="e9daa-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e9daa-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="e9daa-113">Methods</span></span>

<span data-ttu-id="e9daa-114">L'interfaccia **ID3DXInclude** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e9daa-114">The **ID3DXInclude** interface has these methods.</span></span>



| <span data-ttu-id="e9daa-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="e9daa-115">Method</span></span>                               | <span data-ttu-id="e9daa-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9daa-116">Description</span></span>                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9daa-117">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="e9daa-117">**Close**</span></span>](id3dxinclude--close.md) | <span data-ttu-id="e9daa-118">Metodo implementato dall'utente per la chiusura di un \# file di inclusione dello shader.</span><span class="sxs-lookup"><span data-stu-id="e9daa-118">A user-implemented method for closing a shader \#include file.</span></span><br/>                             |
| [<span data-ttu-id="e9daa-119">**Aprire**</span><span class="sxs-lookup"><span data-stu-id="e9daa-119">**Open**</span></span>](id3dxinclude--open.md)   | <span data-ttu-id="e9daa-120">Metodo implementato dall'utente per l'apertura e la lettura del contenuto di un \# file di inclusione dello shader.</span><span class="sxs-lookup"><span data-stu-id="e9daa-120">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9daa-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9daa-121">Remarks</span></span>

<span data-ttu-id="e9daa-122">Un utente crea un'interfaccia ID3DXInclude implementando una classe che deriva da questa interfaccia e implementando tutti i metodi di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e9daa-122">A user creates an ID3DXInclude interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span>

<span data-ttu-id="e9daa-123">Il tipo LPD3DXINCLUDE è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e9daa-123">The LPD3DXINCLUDE type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a><span data-ttu-id="e9daa-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9daa-124">Requirements</span></span>



| <span data-ttu-id="e9daa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9daa-125">Requirement</span></span> | <span data-ttu-id="e9daa-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e9daa-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9daa-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9daa-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e9daa-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9daa-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e9daa-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9daa-129">Library</span></span><br/> | <dl> <span data-ttu-id="e9daa-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9daa-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e9daa-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9daa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9daa-132">Interfacce degli effetti</span><span class="sxs-lookup"><span data-stu-id="e9daa-132">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
