---
title: Funzioni del provider di trasporto WDS
description: I provider di contenuti definiti dall'utente possono esporre le funzioni di callback seguenti al server multicast.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713855"
---
# <a name="wds-transport-provider-functions"></a><span data-ttu-id="728c0-103">Funzioni del provider di trasporto WDS</span><span class="sxs-lookup"><span data-stu-id="728c0-103">WDS Transport Provider Functions</span></span>

<span data-ttu-id="728c0-104">I provider di contenuti definiti dall'utente possono esporre le funzioni di callback seguenti al server multicast.</span><span class="sxs-lookup"><span data-stu-id="728c0-104">User-defined content providers can expose the following callback functions to the multicast server.</span></span>



| <span data-ttu-id="728c0-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="728c0-105">Function</span></span>                                                                               | <span data-ttu-id="728c0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="728c0-106">Description</span></span>                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="728c0-107">*WdsTransportProviderCloseContent*</span><span class="sxs-lookup"><span data-stu-id="728c0-107">*WdsTransportProviderCloseContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | <span data-ttu-id="728c0-108">Chiude un flusso di contenuto specificato da un handle.</span><span class="sxs-lookup"><span data-stu-id="728c0-108">Closes a content stream specified by a handle.</span></span>                                                                          |
| [<span data-ttu-id="728c0-109">*WdsTransportProviderCloseInstance*</span><span class="sxs-lookup"><span data-stu-id="728c0-109">*WdsTransportProviderCloseInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | <span data-ttu-id="728c0-110">Chiude un'istanza di un provider di contenuti specificato da un handle.</span><span class="sxs-lookup"><span data-stu-id="728c0-110">Closes an instance of a content provider specified by a handle.</span></span>                                                         |
| [<span data-ttu-id="728c0-111">*WdsTransportProviderCompareContent*</span><span class="sxs-lookup"><span data-stu-id="728c0-111">*WdsTransportProviderCompareContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | <span data-ttu-id="728c0-112">Confronta un nome di contenuto e un'istanza specificati con un flusso di contenuto aperto per determinare se sono uguali.</span><span class="sxs-lookup"><span data-stu-id="728c0-112">Compares a specified content name and instance to an open content stream to determine if they are the same.</span></span>             |
| [<span data-ttu-id="728c0-113">*WdsTransportProviderCreateInstance*</span><span class="sxs-lookup"><span data-stu-id="728c0-113">*WdsTransportProviderCreateInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | <span data-ttu-id="728c0-114">Apre una nuova istanza di un provider di contenuti.</span><span class="sxs-lookup"><span data-stu-id="728c0-114">Opens a new instance of a content provider.</span></span>                                                                             |
| [<span data-ttu-id="728c0-115">*WdsTransportProviderDumpState*</span><span class="sxs-lookup"><span data-stu-id="728c0-115">*WdsTransportProviderDumpState*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | <span data-ttu-id="728c0-116">Indica al provider di trasporto di stampare un riepilogo dello stato e di tutte le altre informazioni rilevanti nel log di traccia.</span><span class="sxs-lookup"><span data-stu-id="728c0-116">Instructs the transport provider to print a summary of its state and any other relevant information to the tracing log.</span></span> |
| [<span data-ttu-id="728c0-117">*WdsTransportProviderGetContentMetadata*</span><span class="sxs-lookup"><span data-stu-id="728c0-117">*WdsTransportProviderGetContentMetadata*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | <span data-ttu-id="728c0-118">Recupera i metadati per un flusso di contenuto aperto.</span><span class="sxs-lookup"><span data-stu-id="728c0-118">Retrieves metadata for an open content stream.</span></span>                                                                          |
| [<span data-ttu-id="728c0-119">*WdsTransportProviderGetContentSize*</span><span class="sxs-lookup"><span data-stu-id="728c0-119">*WdsTransportProviderGetContentSize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | <span data-ttu-id="728c0-120">Recupera le dimensioni di un flusso di contenuto aperto.</span><span class="sxs-lookup"><span data-stu-id="728c0-120">Retrieves the size of an open content stream.</span></span>                                                                           |
| [<span data-ttu-id="728c0-121">*WdsTransportProviderInitialize*</span><span class="sxs-lookup"><span data-stu-id="728c0-121">*WdsTransportProviderInitialize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | <span data-ttu-id="728c0-122">Inizializza un provider di contenuti.</span><span class="sxs-lookup"><span data-stu-id="728c0-122">Initializes a content provider.</span></span>                                                                                         |
| [<span data-ttu-id="728c0-123">*WdsTransportProviderOpenContent*</span><span class="sxs-lookup"><span data-stu-id="728c0-123">*WdsTransportProviderOpenContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | <span data-ttu-id="728c0-124">Apre una nuova visualizzazione statica di un flusso di contenuto.</span><span class="sxs-lookup"><span data-stu-id="728c0-124">Opens a new static view of a content stream.</span></span>                                                                            |
| [<span data-ttu-id="728c0-125">*WdsTransportProviderReadContent*</span><span class="sxs-lookup"><span data-stu-id="728c0-125">*WdsTransportProviderReadContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | <span data-ttu-id="728c0-126">Legge il contenuto da un flusso di contenuto aperto.</span><span class="sxs-lookup"><span data-stu-id="728c0-126">Reads content from an open content stream.</span></span>                                                                              |
| [<span data-ttu-id="728c0-127">*WdsTransportProviderRefreshSettings*</span><span class="sxs-lookup"><span data-stu-id="728c0-127">*WdsTransportProviderRefreshSettings*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | <span data-ttu-id="728c0-128">Indica al provider di trasporto di rileggere le impostazioni rilevanti.</span><span class="sxs-lookup"><span data-stu-id="728c0-128">Instructs the transport provider to reread any relevant settings.</span></span>                                                       |
| [<span data-ttu-id="728c0-129">*WdsTransportProviderShutdown*</span><span class="sxs-lookup"><span data-stu-id="728c0-129">*WdsTransportProviderShutdown*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | <span data-ttu-id="728c0-130">Shutsdown il provider di contenuti.</span><span class="sxs-lookup"><span data-stu-id="728c0-130">Shutsdown the content provider.</span></span>                                                                                         |
| [<span data-ttu-id="728c0-131">*WdsTransportProviderUserAccessCheck*</span><span class="sxs-lookup"><span data-stu-id="728c0-131">*WdsTransportProviderUserAccessCheck*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | <span data-ttu-id="728c0-132">Specifica l'accesso a un flusso di contenuto in base al token di un utente.</span><span class="sxs-lookup"><span data-stu-id="728c0-132">Specifies access to a content stream based on a user's token.</span></span>                                                           |



 

 

 




