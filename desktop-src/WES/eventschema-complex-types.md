---
title: Tipi complessi dello schema di eventi
description: Di seguito sono riportati i tipi complessi definiti dallo schema dell'evento.
ms.assetid: bc995483-7e54-4224-a372-4e63b0dd764c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2844fef209aedf6819aeaa5a5b6b8a2d698b39a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298825"
---
# <a name="event-schema-complex-types"></a><span data-ttu-id="d932d-103">Tipi complessi dello schema di eventi</span><span class="sxs-lookup"><span data-stu-id="d932d-103">Event Schema Complex Types</span></span>

<span data-ttu-id="d932d-104">Di seguito sono riportati i tipi complessi definiti dallo schema dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d932d-104">The following are the complex types that the Event schema defines.</span></span>



| <span data-ttu-id="d932d-105">Tipo complesso</span><span class="sxs-lookup"><span data-stu-id="d932d-105">Complex type</span></span>                                                                       | <span data-ttu-id="d932d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d932d-106">Description</span></span>                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d932d-107">**ComplexDataType**</span><span class="sxs-lookup"><span data-stu-id="d932d-107">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md)                 | <span data-ttu-id="d932d-108">Definisce una struttura che contiene uno o più elementi di dati.</span><span class="sxs-lookup"><span data-stu-id="d932d-108">Defines a structure that contains one or more data items.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="d932d-109">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d932d-109">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)                          | <span data-ttu-id="d932d-110">Definisce un elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="d932d-110">Defines a data item.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="d932d-111">**DebugDataType**</span><span class="sxs-lookup"><span data-stu-id="d932d-111">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="d932d-112">Definisce i dati che possono essere registrati per gli eventi del preprocessore di traccia software Windows (WPP).</span><span class="sxs-lookup"><span data-stu-id="d932d-112">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="d932d-113">**EventDataType**</span><span class="sxs-lookup"><span data-stu-id="d932d-113">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="d932d-114">Definisce gli elementi e le strutture dei dati dell'evento che contiene i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d932d-114">Defines the event data items and structures that contains the event data.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="d932d-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="d932d-115">**EventType**</span></span>](eventschema-eventtype-complextype.md)                             | <span data-ttu-id="d932d-116">Definisce il nodo radice dello schema dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d932d-116">Defines the root node of the Event schema.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="d932d-117">**ProcessingErrorDataType**</span><span class="sxs-lookup"><span data-stu-id="d932d-117">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="d932d-118">Definisce un errore che si è verificato durante il rendering dei dati dell'evento per l'evento.</span><span class="sxs-lookup"><span data-stu-id="d932d-118">Defines an error that occurred while rendering the event data for the event.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="d932d-119">**RenderingInfoType**</span><span class="sxs-lookup"><span data-stu-id="d932d-119">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="d932d-120">Definisce i messaggi di cui è stato eseguito il rendering per l'evento.</span><span class="sxs-lookup"><span data-stu-id="d932d-120">Defines the rendered messages for the event.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="d932d-121">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="d932d-121">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="d932d-122">Definisce le informazioni che identificano il provider e il modo in cui è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID processo e thread.</span><span class="sxs-lookup"><span data-stu-id="d932d-122">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/> |
| [<span data-ttu-id="d932d-123">**UserDataType**</span><span class="sxs-lookup"><span data-stu-id="d932d-123">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="d932d-124">Definisce un frammento XML che specifica il layout dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d932d-124">Defines an XML fragment that specifies the layout of the event data.</span></span><br/>                                                                                                                           |



 

 

 





