---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileData per compilare o accedere alla gerarchia immediata dell'oggetto dati. Le restrizioni del modello determinano la gerarchia.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: Interfaccia ID3DXFileData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235100"
---
# <a name="id3dxfiledata-interface"></a><span data-ttu-id="29f90-104">Interfaccia ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="29f90-104">ID3DXFileData interface</span></span>

<span data-ttu-id="29f90-105">Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileData per compilare o accedere alla gerarchia immediata dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="29f90-105">Applications use the methods of the ID3DXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="29f90-106">Le restrizioni del modello determinano la gerarchia.</span><span class="sxs-lookup"><span data-stu-id="29f90-106">Template restrictions determine the hierarchy.</span></span>

## <a name="members"></a><span data-ttu-id="29f90-107">Membri</span><span class="sxs-lookup"><span data-stu-id="29f90-107">Members</span></span>

<span data-ttu-id="29f90-108">L'interfaccia **ID3DXFileData** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="29f90-108">The **ID3DXFileData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="29f90-109">**ID3DXFileData** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="29f90-109">**ID3DXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="29f90-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="29f90-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="29f90-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="29f90-111">Methods</span></span>

<span data-ttu-id="29f90-112">L'interfaccia **ID3DXFileData** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="29f90-112">The **ID3DXFileData** interface has these methods.</span></span>



| <span data-ttu-id="29f90-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="29f90-113">Method</span></span>                                            | <span data-ttu-id="29f90-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29f90-114">Description</span></span>                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29f90-115">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="29f90-115">**GetChild**</span></span>](id3dxfiledata--getchild.md)       | <span data-ttu-id="29f90-116">Recupera un oggetto figlio in questo oggetto dati del file.</span><span class="sxs-lookup"><span data-stu-id="29f90-116">Retrieves a child object in this file data object.</span></span><br/>                                                        |
| [<span data-ttu-id="29f90-117">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="29f90-117">**GetChildren**</span></span>](id3dxfiledata--getchildren.md) | <span data-ttu-id="29f90-118">Recupera il numero di elementi figlio in questo oggetto dati del file.</span><span class="sxs-lookup"><span data-stu-id="29f90-118">Retrieves the number of children in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="29f90-119">**Getenum**</span><span class="sxs-lookup"><span data-stu-id="29f90-119">**GetEnum**</span></span>](id3dxfiledata--getenum.md)         | <span data-ttu-id="29f90-120">Recupera l'oggetto di enumerazione in questo oggetto dati del file.</span><span class="sxs-lookup"><span data-stu-id="29f90-120">Retrieves the enumeration object in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="29f90-121">**GetId**</span><span class="sxs-lookup"><span data-stu-id="29f90-121">**GetId**</span></span>](id3dxfiledata--getid.md)             | <span data-ttu-id="29f90-122">Recupera il GUID di questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="29f90-122">Retrieves the GUID of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="29f90-123">**GetName**</span><span class="sxs-lookup"><span data-stu-id="29f90-123">**GetName**</span></span>](id3dxfiledata--getname.md)         | <span data-ttu-id="29f90-124">Recupera il nome di questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="29f90-124">Retrieves the name of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="29f90-125">**GetType**</span><span class="sxs-lookup"><span data-stu-id="29f90-125">**GetType**</span></span>](id3dxfiledata--gettype.md)         | <span data-ttu-id="29f90-126">Recupera l'ID modello in questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="29f90-126">Retrieves the template ID in this file data object.</span></span><br/>                                                       |
| [<span data-ttu-id="29f90-127">**IsReference**</span><span class="sxs-lookup"><span data-stu-id="29f90-127">**IsReference**</span></span>](id3dxfiledata--isreference.md) | <span data-ttu-id="29f90-128">Indica se questo oggetto dati del file è un oggetto di riferimento che punta a un altro oggetto dati figlio.</span><span class="sxs-lookup"><span data-stu-id="29f90-128">Indicates whether this file data object is a reference object that points to another child data object.</span></span><br/>   |
| [<span data-ttu-id="29f90-129">**Lock**</span><span class="sxs-lookup"><span data-stu-id="29f90-129">**Lock**</span></span>](id3dxfiledata--lock.md)               | <span data-ttu-id="29f90-130">Accede ai dati del file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="29f90-130">Accesses the .x file data.</span></span><br/>                                                                                |
| [<span data-ttu-id="29f90-131">**Sblocca**</span><span class="sxs-lookup"><span data-stu-id="29f90-131">**Unlock**</span></span>](id3dxfiledata--unlock.md)           | <span data-ttu-id="29f90-132">Termina la durata del puntatore *ppData* restituito da [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).</span><span class="sxs-lookup"><span data-stu-id="29f90-132">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="29f90-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="29f90-133">Remarks</span></span>

<span data-ttu-id="29f90-134">I tipi di dati consentiti dal modello vengono denominati membri facoltativi.</span><span class="sxs-lookup"><span data-stu-id="29f90-134">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="29f90-135">I membri facoltativi non sono obbligatori, ma un oggetto potrebbe perdere informazioni importanti senza di esse.</span><span class="sxs-lookup"><span data-stu-id="29f90-135">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="29f90-136">Questi membri facoltativi vengono salvati come elementi figlio dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="29f90-136">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="29f90-137">Un elemento figlio può essere un altro oggetto dati o un riferimento a un oggetto dati precedente.</span><span class="sxs-lookup"><span data-stu-id="29f90-137">A child can be another data object or a reference to an earlier data object.</span></span>

<span data-ttu-id="29f90-138">Il GUID per l'interfaccia ID3DXFileData è IID \_ ID3DXFileData.</span><span class="sxs-lookup"><span data-stu-id="29f90-138">The GUID for the ID3DXFileData interface is IID\_ID3DXFileData.</span></span>

<span data-ttu-id="29f90-139">Il tipo LPD3DXFILEDATA è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="29f90-139">The LPD3DXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="29f90-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29f90-140">Requirements</span></span>



| <span data-ttu-id="29f90-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="29f90-141">Requirement</span></span> | <span data-ttu-id="29f90-142">Valore</span><span class="sxs-lookup"><span data-stu-id="29f90-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29f90-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29f90-143">Header</span></span><br/>  | <dl> <span data-ttu-id="29f90-144"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="29f90-144"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="29f90-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="29f90-145">Library</span></span><br/> | <dl> <span data-ttu-id="29f90-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29f90-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="29f90-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29f90-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29f90-148">Interfacce di file D3DX X</span><span class="sxs-lookup"><span data-stu-id="29f90-148">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
