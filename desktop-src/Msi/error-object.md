---
description: L'oggetto Error restituisce le informazioni di un singolo errore di merge.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Oggetto Error (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326381"
---
# <a name="error-object"></a><span data-ttu-id="5ea56-103">Oggetto errore</span><span class="sxs-lookup"><span data-stu-id="5ea56-103">Error object</span></span>

<span data-ttu-id="5ea56-104">L'oggetto **Error** restituisce le informazioni di un singolo errore di merge.</span><span class="sxs-lookup"><span data-stu-id="5ea56-104">The **Error** object returns the information of a single merge error.</span></span>

## <a name="members"></a><span data-ttu-id="5ea56-105">Membri</span><span class="sxs-lookup"><span data-stu-id="5ea56-105">Members</span></span>

<span data-ttu-id="5ea56-106">L'oggetto **Error** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ea56-106">The **Error** object has these types of members:</span></span>

-   [<span data-ttu-id="5ea56-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ea56-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ea56-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ea56-108">Properties</span></span>

<span data-ttu-id="5ea56-109">L'oggetto **Error** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ea56-109">The **Error** object has these properties.</span></span>



| <span data-ttu-id="5ea56-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ea56-110">Property</span></span>                                                | <span data-ttu-id="5ea56-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ea56-111">Description</span></span>                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ea56-112">**DatabaseKeys**</span><span class="sxs-lookup"><span data-stu-id="5ea56-112">**DatabaseKeys**</span></span>](error-databasekeys.md)<br/>   | <span data-ttu-id="5ea56-113">Restituisce le chiavi primarie della riga nella tabella di database che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="5ea56-113">Returns the primary keys of the row in the database table that caused the error.</span></span><br/> |
| [<span data-ttu-id="5ea56-114">**DatabaseTable**</span><span class="sxs-lookup"><span data-stu-id="5ea56-114">**DatabaseTable**</span></span>](error-databasetable.md)<br/> | <span data-ttu-id="5ea56-115">Restituisce il nome della tabella del database che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="5ea56-115">Returns the table name of the table in the database causing the error.</span></span><br/>           |
| [<span data-ttu-id="5ea56-116">**Linguaggio**</span><span class="sxs-lookup"><span data-stu-id="5ea56-116">**Language**</span></span>](error-language.md)<br/>           | <span data-ttu-id="5ea56-117">Restituisce la lingua dell'errore.</span><span class="sxs-lookup"><span data-stu-id="5ea56-117">Return the language of the error.</span></span><br/>                                                |
| [<span data-ttu-id="5ea56-118">**ModuleKeys**</span><span class="sxs-lookup"><span data-stu-id="5ea56-118">**ModuleKeys**</span></span>](error-modulekeys.md)<br/>       | <span data-ttu-id="5ea56-119">Restituisce le chiavi primarie della riga nella tabella dei moduli che hanno causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="5ea56-119">Returns the primary keys of the row in the module table that caused the error.</span></span><br/>   |
| [<span data-ttu-id="5ea56-120">**ModuleTable**</span><span class="sxs-lookup"><span data-stu-id="5ea56-120">**ModuleTable**</span></span>](error-moduletable.md)<br/>     | <span data-ttu-id="5ea56-121">Restituisce il nome della tabella del modulo che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="5ea56-121">Returns the table name of the table in the module causing the error.</span></span><br/>             |
| [<span data-ttu-id="5ea56-122">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="5ea56-122">**Path**</span></span>](error-path.md)<br/>                   | <span data-ttu-id="5ea56-123">Restituisce il percorso del file o della directory che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="5ea56-123">Return the path to the file or directory causing the error.</span></span> <span data-ttu-id="5ea56-124">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="5ea56-124">Currently unused.</span></span><br/>    |
| [<span data-ttu-id="5ea56-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5ea56-125">**Type**</span></span>](error-type.md)<br/>                   | <span data-ttu-id="5ea56-126">Restituisce il tipo di errore.</span><span class="sxs-lookup"><span data-stu-id="5ea56-126">Return the type of error.</span></span><br/>                                                        |



 

## <a name="c"></a><span data-ttu-id="5ea56-127">C++</span><span class="sxs-lookup"><span data-stu-id="5ea56-127">C++</span></span>

<span data-ttu-id="5ea56-128">interfaccia **IMsmError: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="5ea56-128">interface **IMsmError : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="5ea56-129">ID interfaccia</span><span class="sxs-lookup"><span data-stu-id="5ea56-129">Interface ID</span></span>



| <span data-ttu-id="5ea56-130">Costante</span><span class="sxs-lookup"><span data-stu-id="5ea56-130">Constant</span></span>           | <span data-ttu-id="5ea56-131">Valore</span><span class="sxs-lookup"><span data-stu-id="5ea56-131">Value</span></span>                                  |
|--------------------|----------------------------------------|
| <span data-ttu-id="5ea56-132">**\_IMSMERROR IID**</span><span class="sxs-lookup"><span data-stu-id="5ea56-132">**IID\_IMsmError**</span></span> | <span data-ttu-id="5ea56-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="5ea56-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5ea56-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ea56-134">Requirements</span></span>



| <span data-ttu-id="5ea56-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ea56-135">Requirement</span></span> | <span data-ttu-id="5ea56-136">Valore</span><span class="sxs-lookup"><span data-stu-id="5ea56-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea56-137">Versione</span><span class="sxs-lookup"><span data-stu-id="5ea56-137">Version</span></span><br/> | <span data-ttu-id="5ea56-138">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5ea56-138">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5ea56-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ea56-139">Header</span></span><br/>  | <dl> <span data-ttu-id="5ea56-140"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ea56-140"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ea56-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5ea56-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ea56-142"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ea56-142"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




