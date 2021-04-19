---
description: L'oggetto ConfigureModule è un'interfaccia implementata dal client.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Oggetto ConfigureModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332624"
---
# <a name="configuremodule-object"></a><span data-ttu-id="6bd69-103">Oggetto ConfigureModule</span><span class="sxs-lookup"><span data-stu-id="6bd69-103">ConfigureModule object</span></span>

<span data-ttu-id="6bd69-104">L' **oggetto ConfigureModule** è un'interfaccia implementata dal client.</span><span class="sxs-lookup"><span data-stu-id="6bd69-104">The **ConfigureModule object** is an interface implemented by the client.</span></span> <span data-ttu-id="6bd69-105">Mergemod.dllchiama i metodi sull'interfaccia **IMsmConfigureModule** per richiedere che lo strumento client fornisca informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6bd69-105">Mergemod.dllcalls methods on the **IMsmConfigureModule** interface to request that the client tool provide configuration information.</span></span> <span data-ttu-id="6bd69-106">Il modulo è configurato in base alle risposte del client alle chiamate su questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6bd69-106">The module is configured based on the client's responses to calls on this interface.</span></span>

## <a name="members"></a><span data-ttu-id="6bd69-107">Membri</span><span class="sxs-lookup"><span data-stu-id="6bd69-107">Members</span></span>

<span data-ttu-id="6bd69-108">L'oggetto **ConfigureModule** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6bd69-108">The **ConfigureModule** object has these types of members:</span></span>

-   [<span data-ttu-id="6bd69-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="6bd69-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6bd69-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6bd69-110">Methods</span></span>

<span data-ttu-id="6bd69-111">L'oggetto **ConfigureModule** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6bd69-111">The **ConfigureModule** object has these methods.</span></span>



| <span data-ttu-id="6bd69-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="6bd69-112">Method</span></span>                                                           | <span data-ttu-id="6bd69-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6bd69-113">Description</span></span>                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="6bd69-114">**ProvideIntegerData**</span><span class="sxs-lookup"><span data-stu-id="6bd69-114">**ProvideIntegerData**</span></span>](configuremodule-provideintegerdata.md) | <span data-ttu-id="6bd69-115">Chiamato da Mergemod.dll per ottenere numeri interi utilizzati per configurare il modulo.</span><span class="sxs-lookup"><span data-stu-id="6bd69-115">Called by Mergemod.dll to obtain integers used to configure the module.</span></span><br/> |
| [<span data-ttu-id="6bd69-116">**ProvideTextData**</span><span class="sxs-lookup"><span data-stu-id="6bd69-116">**ProvideTextData**</span></span>](configuremodule-providetextdata.md)       | <span data-ttu-id="6bd69-117">Chiamato da Mergemod.dll per ottenere il testo utilizzato per configurare il modulo.</span><span class="sxs-lookup"><span data-stu-id="6bd69-117">Called by Mergemod.dll to obtain text used to configure the module.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="6bd69-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bd69-118">Remarks</span></span>

### <a name="c"></a><span data-ttu-id="6bd69-119">C++</span><span class="sxs-lookup"><span data-stu-id="6bd69-119">C++</span></span>

<span data-ttu-id="6bd69-120">interfaccia **IMsmConfigureModule: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="6bd69-120">interface **IMsmConfigureModule : IDispatch**</span></span>

### <a name="interface-id"></a><span data-ttu-id="6bd69-121">ID interfaccia</span><span class="sxs-lookup"><span data-stu-id="6bd69-121">Interface ID</span></span>



| <span data-ttu-id="6bd69-122">Costante</span><span class="sxs-lookup"><span data-stu-id="6bd69-122">Constant</span></span>                     | <span data-ttu-id="6bd69-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6bd69-123">Value</span></span>                                  |
|------------------------------|----------------------------------------|
| <span data-ttu-id="6bd69-124">**\_IMSMCONFIGUREMODULE IID**</span><span class="sxs-lookup"><span data-stu-id="6bd69-124">**IID\_IMsmConfigureModule**</span></span> | <span data-ttu-id="6bd69-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span><span class="sxs-lookup"><span data-stu-id="6bd69-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6bd69-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bd69-126">Requirements</span></span>



| <span data-ttu-id="6bd69-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bd69-127">Requirement</span></span> | <span data-ttu-id="6bd69-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6bd69-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd69-129">Versione</span><span class="sxs-lookup"><span data-stu-id="6bd69-129">Version</span></span><br/> | <span data-ttu-id="6bd69-130">Mergemod.dll 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6bd69-130">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6bd69-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6bd69-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6bd69-132"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bd69-132"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6bd69-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6bd69-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="6bd69-134"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bd69-134"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




