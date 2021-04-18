---
title: Oggetto ErrorItem
description: L'oggetto ErrorItem fornisce un modo per accedere alle informazioni sugli errori.
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- Media Player di Windows oggetto ErrorItem
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c273d00477363c66c49dfa1f77a66dab42c711cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299127"
---
# <a name="erroritem-object"></a><span data-ttu-id="9bbfd-104">Oggetto ErrorItem</span><span class="sxs-lookup"><span data-stu-id="9bbfd-104">ErrorItem Object</span></span>

<span data-ttu-id="9bbfd-105">L'oggetto **ErrorItem** fornisce un modo per accedere alle informazioni sugli errori.</span><span class="sxs-lookup"><span data-stu-id="9bbfd-105">The **ErrorItem** object provides a way to access error information.</span></span>

<span data-ttu-id="9bbfd-106">L'oggetto **ErrorItem** supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="9bbfd-106">The **ErrorItem** object supports the following properties.</span></span>



| <span data-ttu-id="9bbfd-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9bbfd-107">Property</span></span>                                           | <span data-ttu-id="9bbfd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bbfd-108">Description</span></span>                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bbfd-109">condizione</span><span class="sxs-lookup"><span data-stu-id="9bbfd-109">condition</span></span>](erroritem-condition.md)               | <span data-ttu-id="9bbfd-110">Recupera un valore che indica la condizione per l'errore.</span><span class="sxs-lookup"><span data-stu-id="9bbfd-110">Retrieves a value indicating the condition for the error.</span></span>                                       |
| [<span data-ttu-id="9bbfd-111">customUrl</span><span class="sxs-lookup"><span data-stu-id="9bbfd-111">customUrl</span></span>](erroritem-customurl.md)               | <span data-ttu-id="9bbfd-112">Recupera l'URL di un sito Web che visualizza informazioni specifiche sull'errore di download del codec.</span><span class="sxs-lookup"><span data-stu-id="9bbfd-112">Retrieves the URL of a website that displays specific information about codec download failure.</span></span> |
| [<span data-ttu-id="9bbfd-113">errorCode</span><span class="sxs-lookup"><span data-stu-id="9bbfd-113">errorCode</span></span>](erroritem-errorcode.md)               | <span data-ttu-id="9bbfd-114">Recupera il codice di errore corrente.</span><span class="sxs-lookup"><span data-stu-id="9bbfd-114">Retrieves the current error code.</span></span>                                                               |
| [<span data-ttu-id="9bbfd-115">errorContext</span><span class="sxs-lookup"><span data-stu-id="9bbfd-115">errorContext</span></span>](erroritem-errorcontext.md)         | <span data-ttu-id="9bbfd-116">Recupera un valore che indica il contesto dell'errore.</span><span class="sxs-lookup"><span data-stu-id="9bbfd-116">Retrieves a value indicating the context of the error.</span></span>                                          |
| [<span data-ttu-id="9bbfd-117">errorDescription</span><span class="sxs-lookup"><span data-stu-id="9bbfd-117">errorDescription</span></span>](erroritem-errordescription.md) | <span data-ttu-id="9bbfd-118">Recupera una descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="9bbfd-118">Retrieves a description of the error.</span></span>                                                           |
| <span data-ttu-id="9bbfd-119">**risolvere**</span><span class="sxs-lookup"><span data-stu-id="9bbfd-119">**remedy**</span></span>                                         | <span data-ttu-id="9bbfd-120">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="9bbfd-120">Reserved for future use.</span></span>                                                                        |



 

<span data-ttu-id="9bbfd-121">È possibile accedere all'oggetto **ErrorItem** tramite i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="9bbfd-121">The **ErrorItem** object is accessed through the following methods.</span></span>



| <span data-ttu-id="9bbfd-122">Oggetto</span><span class="sxs-lookup"><span data-stu-id="9bbfd-122">Object</span></span>                    | <span data-ttu-id="9bbfd-123">Metodo</span><span class="sxs-lookup"><span data-stu-id="9bbfd-123">Method</span></span>                   |
|---------------------------|--------------------------|
| [<span data-ttu-id="9bbfd-124">Error (Errore) (Error (Errore)e)</span><span class="sxs-lookup"><span data-stu-id="9bbfd-124">Error</span></span>](error-object.md) | [<span data-ttu-id="9bbfd-125">item</span><span class="sxs-lookup"><span data-stu-id="9bbfd-125">item</span></span>](error-item.md)   |
| [<span data-ttu-id="9bbfd-126">Supporti</span><span class="sxs-lookup"><span data-stu-id="9bbfd-126">Media</span></span>](media-object.md) | [<span data-ttu-id="9bbfd-127">error</span><span class="sxs-lookup"><span data-stu-id="9bbfd-127">error</span></span>](media-error.md) |



 

<span data-ttu-id="9bbfd-128">Ai fini dell'illustrazione, *Player*. *errore*. l' *elemento*(*Indice*) viene usato nelle sezioni della sintassi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="9bbfd-128">For purposes of illustration, *player*.*error*.*item*(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bbfd-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bbfd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bbfd-130">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="9bbfd-130">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




