---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileData per compilare o accedere alla gerarchia immediata dell'oggetto dati.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Interfaccia IDirectXFileData (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323229"
---
# <a name="idirectxfiledata-interface"></a><span data-ttu-id="9245d-103">Interfaccia IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="9245d-103">IDirectXFileData interface</span></span>

<span data-ttu-id="9245d-104">Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileData per compilare o accedere alla gerarchia immediata dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="9245d-104">Applications use the methods of the IDirectXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="9245d-105">Le restrizioni del modello determinano la gerarchia.</span><span class="sxs-lookup"><span data-stu-id="9245d-105">Template restrictions determine the hierarchy.</span></span> <span data-ttu-id="9245d-106">I tipi di dati consentiti dal modello vengono denominati membri facoltativi.</span><span class="sxs-lookup"><span data-stu-id="9245d-106">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="9245d-107">I membri facoltativi non sono obbligatori, ma un oggetto potrebbe perdere informazioni importanti senza di esse.</span><span class="sxs-lookup"><span data-stu-id="9245d-107">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="9245d-108">Questi membri facoltativi vengono salvati come elementi figlio dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="9245d-108">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="9245d-109">Gli elementi figlio possono essere un altro oggetto dati, un riferimento a un oggetto dati precedente o un oggetto binario.</span><span class="sxs-lookup"><span data-stu-id="9245d-109">The children can be another data object, a reference to an earlier data object, or a binary object.</span></span> <span data-ttu-id="9245d-110">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9245d-110">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="9245d-111">Membri</span><span class="sxs-lookup"><span data-stu-id="9245d-111">Members</span></span>

<span data-ttu-id="9245d-112">L'interfaccia **IDirectXFileData** eredita da [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="9245d-112">The **IDirectXFileData** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="9245d-113">**IDirectXFileData** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9245d-113">**IDirectXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="9245d-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="9245d-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9245d-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="9245d-115">Methods</span></span>

<span data-ttu-id="9245d-116">L'interfaccia **IDirectXFileData** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9245d-116">The **IDirectXFileData** interface has these methods.</span></span>



| <span data-ttu-id="9245d-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="9245d-117">Method</span></span>                                                         | <span data-ttu-id="9245d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9245d-118">Description</span></span>                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9245d-119">**AddBinaryObject**</span><span class="sxs-lookup"><span data-stu-id="9245d-119">**AddBinaryObject**</span></span>](idirectxfiledata--addbinaryobject.md)   | <span data-ttu-id="9245d-120">Crea un oggetto binario e lo aggiunge come oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="9245d-120">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="9245d-121">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9245d-121">Deprecated.</span></span><br/>                                             |
| [<span data-ttu-id="9245d-122">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="9245d-122">**AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)       | <span data-ttu-id="9245d-123">Aggiunge un oggetto dati come oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="9245d-123">Adds a data object as a child object.</span></span> <span data-ttu-id="9245d-124">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9245d-124">Deprecated.</span></span><br/>                                                              |
| [<span data-ttu-id="9245d-125">**AddDataReference**</span><span class="sxs-lookup"><span data-stu-id="9245d-125">**AddDataReference**</span></span>](idirectxfiledata--adddatareference.md) | <span data-ttu-id="9245d-126">Crea e aggiunge un oggetto riferimento ai dati come oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="9245d-126">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="9245d-127">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9245d-127">Deprecated.</span></span><br/>                                        |
| [<span data-ttu-id="9245d-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="9245d-128">**GetData**</span></span>](idirectxfiledata--getdata.md)                   | <span data-ttu-id="9245d-129">Recupera i dati per uno dei membri dell'oggetto o i dati per tutti i membri.</span><span class="sxs-lookup"><span data-stu-id="9245d-129">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="9245d-130">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9245d-130">Deprecated.</span></span><br/>                    |
| [<span data-ttu-id="9245d-131">**GetNextObject**</span><span class="sxs-lookup"><span data-stu-id="9245d-131">**GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)       | <span data-ttu-id="9245d-132">Recupera il successivo oggetto dati figlio, oggetto riferimento ai dati o oggetto binario nel file DirectX.</span><span class="sxs-lookup"><span data-stu-id="9245d-132">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="9245d-133">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9245d-133">Deprecated.</span></span><br/> |
| [<span data-ttu-id="9245d-134">**GetType**</span><span class="sxs-lookup"><span data-stu-id="9245d-134">**GetType**</span></span>](idirectxfiledata--gettype.md)                   | <span data-ttu-id="9245d-135">Recupera il GUID del modello dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9245d-135">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="9245d-136">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9245d-136">Deprecated.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="9245d-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="9245d-137">Remarks</span></span>

<span data-ttu-id="9245d-138">Il GUID per l'interfaccia IDirectXFileData è IID \_ IDirectXFileData.</span><span class="sxs-lookup"><span data-stu-id="9245d-138">The GUID for the IDirectXFileData interface is IID\_IDirectXFileData.</span></span>

<span data-ttu-id="9245d-139">Il tipo LPDIRECTXFILEDATA è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="9245d-139">The LPDIRECTXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="9245d-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9245d-140">Requirements</span></span>



| <span data-ttu-id="9245d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9245d-141">Requirement</span></span> | <span data-ttu-id="9245d-142">Valore</span><span class="sxs-lookup"><span data-stu-id="9245d-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9245d-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9245d-143">Header</span></span><br/>  | <dl> <span data-ttu-id="9245d-144"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="9245d-144"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="9245d-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="9245d-145">Library</span></span><br/> | <dl> <span data-ttu-id="9245d-146"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9245d-146"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9245d-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9245d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9245d-148">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="9245d-148">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="9245d-149">Interfacce di file X</span><span class="sxs-lookup"><span data-stu-id="9245d-149">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




