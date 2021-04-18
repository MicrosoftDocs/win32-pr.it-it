---
description: L'oggetto Dependency restituisce un modulo dal quale dipende il modulo corrente e che non è ancora stato unito al database di installazione corrente.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Oggetto Dependency (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328775"
---
# <a name="dependency-object"></a><span data-ttu-id="6408d-103">Oggetto Dependency</span><span class="sxs-lookup"><span data-stu-id="6408d-103">Dependency object</span></span>

<span data-ttu-id="6408d-104">L'oggetto **Dependency** restituisce un modulo dal quale dipende il modulo corrente e che non è ancora stato unito al database di installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="6408d-104">The **Dependency** object returns a module that the current module is dependent upon and which has not yet been merged into the current installation database.</span></span>

## <a name="members"></a><span data-ttu-id="6408d-105">Membri</span><span class="sxs-lookup"><span data-stu-id="6408d-105">Members</span></span>

<span data-ttu-id="6408d-106">L'oggetto di **dipendenza** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6408d-106">The **Dependency** object has these types of members:</span></span>

-   [<span data-ttu-id="6408d-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6408d-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6408d-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6408d-108">Properties</span></span>

<span data-ttu-id="6408d-109">L'oggetto di **dipendenza** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6408d-109">The **Dependency** object has these properties.</span></span>



| <span data-ttu-id="6408d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6408d-110">Property</span></span>                                           | <span data-ttu-id="6408d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6408d-111">Description</span></span>                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="6408d-112">**Lingua**</span><span class="sxs-lookup"><span data-stu-id="6408d-112">**Language**</span></span>](dependency-language.md)<br/> | <span data-ttu-id="6408d-113">Restituisce la lingua del modulo.</span><span class="sxs-lookup"><span data-stu-id="6408d-113">Return the language of the module.</span></span><br/>           |
| [<span data-ttu-id="6408d-114">**Modulo**</span><span class="sxs-lookup"><span data-stu-id="6408d-114">**Module**</span></span>](dependency-module.md)<br/>     | <span data-ttu-id="6408d-115">Restituisce l'ID del modulo richiesto.</span><span class="sxs-lookup"><span data-stu-id="6408d-115">Return the module ID of the required module.</span></span><br/> |
| [<span data-ttu-id="6408d-116">**Versione**</span><span class="sxs-lookup"><span data-stu-id="6408d-116">**Version**</span></span>](dependency-version.md)<br/>   | <span data-ttu-id="6408d-117">Restituisce la versione del modulo richiesto.</span><span class="sxs-lookup"><span data-stu-id="6408d-117">Return the version of the required module.</span></span><br/>   |



 

## <a name="c"></a><span data-ttu-id="6408d-118">C++</span><span class="sxs-lookup"><span data-stu-id="6408d-118">C++</span></span>

<span data-ttu-id="6408d-119">interfaccia **IMsmDependency: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="6408d-119">interface **IMsmDependency : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="6408d-120">ID interfaccia</span><span class="sxs-lookup"><span data-stu-id="6408d-120">Interface ID</span></span>



| <span data-ttu-id="6408d-121">Costante</span><span class="sxs-lookup"><span data-stu-id="6408d-121">Constant</span></span>                | <span data-ttu-id="6408d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6408d-122">Value</span></span>                                  |
|-------------------------|----------------------------------------|
| <span data-ttu-id="6408d-123">**\_IMSMDEPENDENCY IID**</span><span class="sxs-lookup"><span data-stu-id="6408d-123">**IID\_IMsmDependency**</span></span> | <span data-ttu-id="6408d-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="6408d-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6408d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6408d-125">Requirements</span></span>



| <span data-ttu-id="6408d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6408d-126">Requirement</span></span> | <span data-ttu-id="6408d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6408d-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6408d-128">Versione</span><span class="sxs-lookup"><span data-stu-id="6408d-128">Version</span></span><br/> | <span data-ttu-id="6408d-129">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6408d-129">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6408d-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6408d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6408d-131"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="6408d-131"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6408d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6408d-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="6408d-133"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6408d-133"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




