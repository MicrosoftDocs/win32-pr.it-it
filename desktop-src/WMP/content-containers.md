---
title: Contenitori di contenuto
description: Contenitori di contenuto
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player Online Stores, contenitori di contenuti
- archivi online, contenitori di contenuti
- digitare 1 negozi online, contenitori di contenuto
- Windows Media Player Online Stores, interfaccia IWMPContentContainer
- negozi online, interfaccia IWMPContentContainer
- tipo 1 Store online, interfaccia IWMPContentContainer
- Windows Media Player, contenitori di contenuto
- Windows Media Player, interfaccia IWMPContentContainer
- contenitori di contenuto
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299511"
---
# <a name="content-containers"></a><span data-ttu-id="4775f-113">Contenitori di contenuto</span><span class="sxs-lookup"><span data-stu-id="4775f-113">Content Containers</span></span>

<span data-ttu-id="4775f-114">Windows Media Player usa i contenitori di contenuto per rappresentare il contenuto multimediale digitale in un download o una transazione di acquisto della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4775f-114">Windows Media Player uses content containers to represent digital media content in a subscription download or purchase transaction.</span></span> <span data-ttu-id="4775f-115">Un contenitore di contenuti è rappresentato dall'interfaccia **IWMPContentContainer** .</span><span class="sxs-lookup"><span data-stu-id="4775f-115">A content container is represented by the **IWMPContentContainer** interface.</span></span> <span data-ttu-id="4775f-116">Un contenitore di contenuto potrebbe contenere un elenco di contenuti correlati, ad esempio un album, o un set di elementi di contenuto non correlati o *tracce*.</span><span class="sxs-lookup"><span data-stu-id="4775f-116">A content container might contain a list of related content, such as an album, or a set of unrelated content items, or *tracks*.</span></span> <span data-ttu-id="4775f-117">È possibile usare l'interfaccia **IWMPContentContainer** per enumerare le tracce del contenitore di contenuto e recuperare il prezzo di ogni traccia. È anche possibile recuperare informazioni sul contenitore di contenuto stesso, ad esempio l'ID del contenitore, il tipo di contenuto nel contenitore e il prezzo totale per le tracce nel contenitore (che potrebbero differire dalla somma dei prezzi delle singole tracce, come nel caso di un acquisto di album).</span><span class="sxs-lookup"><span data-stu-id="4775f-117">You can use the **IWMPContentContainer** interface to enumerate the tracks of the content container and retrieve the price of each track. You can also retrieve information about the content container itself, such as the container ID, the type of content in the container, and the total price for the tracks in the container (which might differ from the sum of the prices of the individual tracks, as in the case of an album purchase).</span></span>

<span data-ttu-id="4775f-118">Per fornire un meccanismo per la creazione di pacchetti di più contenitori di contenuto in un singolo oggetto, Windows Media Player supporta l'interfaccia **IWMPContentContainerList** .</span><span class="sxs-lookup"><span data-stu-id="4775f-118">To provide a mechanism for packaging multiple content containers into a single object, Windows Media Player supports the **IWMPContentContainerList** interface.</span></span> <span data-ttu-id="4775f-119">**IWMPContentContainerList** fornisce metodi per enumerare e recuperare i contenitori di contenuto nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="4775f-119">**IWMPContentContainerList** provides methods to enumerate and retrieve the content containers in the list.</span></span> <span data-ttu-id="4775f-120">Per individuare se l'elenco di contenitori di contenuto rappresenta un download di acquisto o di sottoscrizione, chiamare [IWMPContentContainerList:: GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) per recuperare un valore [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) .</span><span class="sxs-lookup"><span data-stu-id="4775f-120">To discover whether the content container list represents a purchase or a subscription download, call [IWMPContentContainerList::GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) to retrieve a [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4775f-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4775f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4775f-122">**Informazioni sugli archivi online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="4775f-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4775f-123">**Interfaccia IWMPContentContainer**</span><span class="sxs-lookup"><span data-stu-id="4775f-123">**IWMPContentContainer Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[<span data-ttu-id="4775f-124">**Interfaccia IWMPContentContainerList**</span><span class="sxs-lookup"><span data-stu-id="4775f-124">**IWMPContentContainerList Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




