---
description: L'oggetto GetFiles recupera i file necessari in una determinata lingua del modulo. Richiede che alcune azioni vengano eseguite tramite l'oggetto merge prima che tutte le parti di questa interfaccia restituiscono risultati validi.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: Oggetto GetFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332848"
---
# <a name="getfiles-object"></a><span data-ttu-id="37efe-104">GetFiles (oggetto)</span><span class="sxs-lookup"><span data-stu-id="37efe-104">GetFiles object</span></span>

<span data-ttu-id="37efe-105">L'oggetto **GetFiles** recupera i file necessari in una determinata lingua del modulo.</span><span class="sxs-lookup"><span data-stu-id="37efe-105">The **GetFiles** object retrieves the files needed in a particular language of the module.</span></span> <span data-ttu-id="37efe-106">Richiede che alcune azioni vengano eseguite tramite l' [oggetto merge](merge-object.md) prima che tutte le parti di questa interfaccia restituiscono risultati validi.</span><span class="sxs-lookup"><span data-stu-id="37efe-106">Requires certain actions be performed through the [Merge object](merge-object.md) before all parts of this interface returns valid results.</span></span>

## <a name="members"></a><span data-ttu-id="37efe-107">Membri</span><span class="sxs-lookup"><span data-stu-id="37efe-107">Members</span></span>

<span data-ttu-id="37efe-108">L'oggetto **GetFiles** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="37efe-108">The **GetFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="37efe-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37efe-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37efe-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37efe-110">Properties</span></span>

<span data-ttu-id="37efe-111">L'oggetto **GetFiles** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="37efe-111">The **GetFiles** object has these properties.</span></span>



| <span data-ttu-id="37efe-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37efe-112">Property</span></span>                                               | <span data-ttu-id="37efe-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37efe-113">Description</span></span>                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37efe-114">**ModuleFiles**</span><span class="sxs-lookup"><span data-stu-id="37efe-114">**ModuleFiles**</span></span>](getfiles-modulefiles.md)<br/> | <span data-ttu-id="37efe-115">La proprietà [**ModuleFiles**](getfiles-modulefiles.md) restituisce tutte le chiavi primarie della [tabella file](file-table.md) per il modulo attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="37efe-115">[**ModuleFiles**](getfiles-modulefiles.md) property returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span><br/> |



 

## <a name="c"></a><span data-ttu-id="37efe-116">C++</span><span class="sxs-lookup"><span data-stu-id="37efe-116">C++</span></span>

<span data-ttu-id="37efe-117">interfaccia **IMsmGetFiles: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="37efe-117">interface **IMsmGetFiles : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="37efe-118">ID interfaccia</span><span class="sxs-lookup"><span data-stu-id="37efe-118">Interface ID</span></span>



| <span data-ttu-id="37efe-119">Costante</span><span class="sxs-lookup"><span data-stu-id="37efe-119">Constant</span></span>              | <span data-ttu-id="37efe-120">Valore</span><span class="sxs-lookup"><span data-stu-id="37efe-120">Value</span></span>                                  |
|-----------------------|----------------------------------------|
| <span data-ttu-id="37efe-121">**\_IMSMGETFILES IID**</span><span class="sxs-lookup"><span data-stu-id="37efe-121">**IID\_IMsmGetFiles**</span></span> | <span data-ttu-id="37efe-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="37efe-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="37efe-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37efe-123">Requirements</span></span>



| <span data-ttu-id="37efe-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="37efe-124">Requirement</span></span> | <span data-ttu-id="37efe-125">Valore</span><span class="sxs-lookup"><span data-stu-id="37efe-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37efe-126">Versione</span><span class="sxs-lookup"><span data-stu-id="37efe-126">Version</span></span><br/> | <span data-ttu-id="37efe-127">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="37efe-127">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="37efe-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37efe-128">Header</span></span><br/>  | <dl> <span data-ttu-id="37efe-129"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="37efe-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="37efe-130">DLL</span><span class="sxs-lookup"><span data-stu-id="37efe-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="37efe-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37efe-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




