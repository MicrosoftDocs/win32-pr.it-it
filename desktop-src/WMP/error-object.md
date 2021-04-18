---
title: Oggetto Error (WMP SDK)
description: L'oggetto Error fornisce l'accesso a una raccolta di oggetti ErrorItem.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Finestra oggetto errore Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/09/2019
ms.locfileid: "106299317"
---
# <a name="error-object"></a><span data-ttu-id="1577c-104">Oggetto Error</span><span class="sxs-lookup"><span data-stu-id="1577c-104">Error Object</span></span>

<span data-ttu-id="1577c-105">L'oggetto **Error** fornisce l'accesso a una raccolta di oggetti [ErrorItem](erroritem-object.md) .</span><span class="sxs-lookup"><span data-stu-id="1577c-105">The **Error** object provides access to a collection of [ErrorItem](erroritem-object.md) objects.</span></span>

<span data-ttu-id="1577c-106">L'oggetto **Error** supporta la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="1577c-106">The **Error** object supports the following property.</span></span>



| <span data-ttu-id="1577c-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1577c-107">Property</span></span>                           | <span data-ttu-id="1577c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1577c-108">Description</span></span>                                        |
|------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="1577c-109">errorCount</span><span class="sxs-lookup"><span data-stu-id="1577c-109">errorCount</span></span>](error-errorcount.md) | <span data-ttu-id="1577c-110">Recupera il numero di errori nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="1577c-110">Retrieves the number of errors in the error queue.</span></span> |



 

<span data-ttu-id="1577c-111">L'oggetto **Error** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1577c-111">The **Error** object supports the following methods.</span></span>



| <span data-ttu-id="1577c-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="1577c-112">Method</span></span>                                       | <span data-ttu-id="1577c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1577c-113">Description</span></span>                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1577c-114">clearErrorQueue</span><span class="sxs-lookup"><span data-stu-id="1577c-114">clearErrorQueue</span></span>](error-clearerrorqueue.md) | <span data-ttu-id="1577c-115">Cancella gli errori dalla coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="1577c-115">Clears the errors from the error queue.</span></span>                                                         |
| [<span data-ttu-id="1577c-116">item</span><span class="sxs-lookup"><span data-stu-id="1577c-116">item</span></span>](error-item.md)                       | <span data-ttu-id="1577c-117">Recupera un oggetto [ErrorItem](erroritem-object.md) dalla coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="1577c-117">Retrieves an [ErrorItem](erroritem-object.md) object from the error queue.</span></span>                     |
| [<span data-ttu-id="1577c-118">webHelp</span><span class="sxs-lookup"><span data-stu-id="1577c-118">webHelp</span></span>](error-webhelp.md)                 | <span data-ttu-id="1577c-119">Avvia la pagina della Guida di Windows Media Player Web per visualizzare altre informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="1577c-119">Launches the Windows Media Player Web Help page to display further information about the error.</span></span> |



 

<span data-ttu-id="1577c-120">È possibile accedere all'oggetto **errore** tramite la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="1577c-120">The **Error** object is accessed through the following property.</span></span>



| <span data-ttu-id="1577c-121">Oggetto</span><span class="sxs-lookup"><span data-stu-id="1577c-121">Object</span></span>                      | <span data-ttu-id="1577c-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1577c-122">Property</span></span>                  |
|-----------------------------|---------------------------|
| [<span data-ttu-id="1577c-123">Player</span><span class="sxs-lookup"><span data-stu-id="1577c-123">Player</span></span>](player-object.md) | [<span data-ttu-id="1577c-124">error</span><span class="sxs-lookup"><span data-stu-id="1577c-124">error</span></span>](player-error.md) |



 

## <a name="see-also"></a><span data-ttu-id="1577c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1577c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1577c-126">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="1577c-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




