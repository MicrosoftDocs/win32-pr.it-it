---
title: Catalogo musica
description: Catalogo musica
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player Online Stores, cataloghi musica
- archivi online, cataloghi musicali
- digitare 1 negozi online, cataloghi musica
- Windows Media Player Online Stores, compilatore catalog
- archivi online, compilatore di cataloghi
- digitare 1 negozi online, compilatore di cataloghi
- Cataloghi musica
- compilatore Catalogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046278"
---
# <a name="music-catalog"></a><span data-ttu-id="fc938-111">Catalogo musica</span><span class="sxs-lookup"><span data-stu-id="fc938-111">Music Catalog</span></span>

<span data-ttu-id="fc938-112">Un archivio online di tipo 1 crea il proprio catalogo musicale come un set di file con valori delimitati da tabulazioni (TSV).</span><span class="sxs-lookup"><span data-stu-id="fc938-112">A type 1 online store creates its music catalog as a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="fc938-113">Quindi, il negozio online usa il [compilatore del catalogo](catalog-compiler-for-type-1-online-stores.md) Microsoft per compilare i file TSV in un catalogo compresso che può essere scaricato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fc938-113">Then the online store uses Microsoft's [catalog compiler](catalog-compiler-for-type-1-online-stores.md) to compile the TSV files into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="fc938-114">Windows Media Player può scaricare i file di catalogo completi o i file di aggiornamento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="fc938-114">Windows Media Player can download full catalog files or catalog update files.</span></span> <span data-ttu-id="fc938-115">Gli aggiornamenti del catalogo contengono solo le informazioni sul catalogo modificate dopo l'ultimo aggiornamento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="fc938-115">Catalog updates contain only the catalog information that has changed since the last catalog update.</span></span> <span data-ttu-id="fc938-116">È il plug-in del partner di contenuti a determinare se scaricare un catalogo completo o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="fc938-116">It is up to the content partner plug-in to determine whether to download a full catalog or an update.</span></span> <span data-ttu-id="fc938-117">In entrambi i casi, Windows Media Player applica le modifiche al catalogo corrente al momento della notifica dal plug-in.</span><span class="sxs-lookup"><span data-stu-id="fc938-117">In either case, Windows Media Player applies the changes to the current catalog upon notification from the plug-in.</span></span>

<span data-ttu-id="fc938-118">Se per l'archivio online è stato preparato un nuovo catalogo, il plug-in può inviare una notifica al lettore chiamando [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) e passando wmpcnNewCatalogAvailable come valore per il parametro di *tipo* .</span><span class="sxs-lookup"><span data-stu-id="fc938-118">If the online store has a new catalog prepared, the plug-in can notify the Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) and passing wmpcnNewCatalogAvailable as the value for the *type* parameter.</span></span>

<span data-ttu-id="fc938-119">Quando Windows Media Player è pronto per il download di un catalogo o di un aggiornamento, il lettore chiama [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="fc938-119">When Windows Media Player is ready to download a catalog or update, the Player calls [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> <span data-ttu-id="fc938-120">Questo metodo fornisce il plug-in con informazioni sul catalogo corrente, ad esempio la versione del catalogo e l'identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="fc938-120">This method provides the plug-in with information about the current catalog, such as the catalog version and locale identifier.</span></span> <span data-ttu-id="fc938-121">Il plug-in risponde fornendo l'URL (Uniform Resource Locator) del catalogo o dell'aggiornamento completo corretto, nonché un numero di versione e una data di scadenza aggiornati.</span><span class="sxs-lookup"><span data-stu-id="fc938-121">The plug-in responds by supplying the uniform resource locator (URL) of the correct full catalog or update, as well as an updated version number and expiration date.</span></span> <span data-ttu-id="fc938-122">Windows Media Player richiede periodicamente aggiornamenti del catalogo in base alle informazioni fornite dal plug-in in **GetCatalogURL**.</span><span class="sxs-lookup"><span data-stu-id="fc938-122">Windows Media Player will periodically request catalog updates based upon the information provided by the plug-in in **GetCatalogURL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc938-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc938-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc938-124">**Informazioni sugli archivi online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="fc938-124">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="fc938-125">**Compilatore del catalogo per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="fc938-125">**Catalog Compiler for Type 1 Online Stores**</span></span>](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="fc938-126">**Interfaccia IWMPContentPartner**</span><span class="sxs-lookup"><span data-stu-id="fc938-126">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




