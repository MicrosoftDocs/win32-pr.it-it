---
title: Acquisto di contenuti multimediali
description: Acquisto di contenuti multimediali
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Windows Media Player Online Stores, acquisto di contenuti multimediali
- negozi online, acquisto di contenuti multimediali
- digitare 1 negozi online, acquistare contenuti multimediali
- Windows Media Player Online Store, acquisti di contenuti multimediali
- negozi online, acquisti di contenuti multimediali
- digitare 1 negozi online, acquisti di contenuti multimediali
- contenuti multimediali, acquisti
- acquisto di contenuti multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e420f1dce607e1c596c48490d10bbe8a2a5a5f61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956171"
---
# <a name="purchasing-media-content"></a><span data-ttu-id="ae332-111">Acquisto di contenuti multimediali</span><span class="sxs-lookup"><span data-stu-id="ae332-111">Purchasing Media Content</span></span>

<span data-ttu-id="ae332-112">Quando Windows Media Player Visualizza contenuto musicale nella visualizzazione albero della libreria, l'interfaccia utente include gli elementi su cui l'utente può fare clic per acquistare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="ae332-112">When Windows Media Player displays music content in the library tree view, the user interface includes elements that the user can click to buy the content.</span></span> <span data-ttu-id="ae332-113">Ad esempio, l'utente può fare clic su un pulsante per acquistare un singolo brano o acquistare un intero album.</span><span class="sxs-lookup"><span data-stu-id="ae332-113">For example, the user might click a button to buy an individual song or to buy an entire album.</span></span>

<span data-ttu-id="ae332-114">Se lo Store online attivo è di tipo 1, Windows Media Player ha accesso ai prezzi Track, album ed List nel catalogo del negozio online.</span><span class="sxs-lookup"><span data-stu-id="ae332-114">If the active online store is a Type 1 store, Windows Media Player has access to track, album, and list prices in the online store's catalog.</span></span> <span data-ttu-id="ae332-115">I prezzi nel catalogo sono stringhe con un formato riconosciuto solo dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="ae332-115">Those prices in the catalog are strings that have a format understood only by the online store.</span></span> <span data-ttu-id="ae332-116">Windows Media Player non interpreta le stringhe dei prezzi; vengono semplicemente visualizzate negli elementi dell'interfaccia utente come i pulsanti Acquista.</span><span class="sxs-lookup"><span data-stu-id="ae332-116">Windows Media Player does not interpret price strings; it merely displays them in user interface elements like Buy buttons.</span></span>

<span data-ttu-id="ae332-117">Quando Windows Media Player imposta un acquisto per un set di elementi multimediali, passa gli ID e i prezzi degli elementi multimediali al plug-in del partner di contenuti chiamando [IWMPContentPartner:: CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent).</span><span class="sxs-lookup"><span data-stu-id="ae332-117">When Windows Media Player sets up a purchase for a set of media items, it passes the IDs and prices of the media items to the content partner plug-in by calling [IWMPContentPartner::CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent).</span></span> <span data-ttu-id="ae332-118">A questo punto, il plug-in può ispezionare i prezzi forniti dal lettore.</span><span class="sxs-lookup"><span data-stu-id="ae332-118">At that point, the plug-in can inspect the prices provided by the Player.</span></span> <span data-ttu-id="ae332-119">Si tratta dei prezzi che l'utente prevede di pagare; ovvero i prezzi visualizzati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ae332-119">These are the prices that the user expects to pay; that is, the prices that the Player displayed to the user.</span></span> <span data-ttu-id="ae332-120">In base agli ID dei supporti e ai prezzi forniti dal lettore, il plug-in calcola il prezzo totale restituito al lettore nel parametro *bstrTotalPrice* .</span><span class="sxs-lookup"><span data-stu-id="ae332-120">Based on the media IDs and prices provided by the Player, the plug-in calculates a total price, which it returns to the Player in the *bstrTotalPrice* parameter.</span></span> <span data-ttu-id="ae332-121">I prezzi che il giocatore passa a **CanBuySilent** forniscono il plug-in con le informazioni, ma non obbligano il plug-in a restituire un determinato prezzo totale.</span><span class="sxs-lookup"><span data-stu-id="ae332-121">The prices that the Player passes to **CanBuySilent** provide the plug-in with information, but they do not obligate the plug-in to return a certain total price.</span></span> <span data-ttu-id="ae332-122">Il plug-in è in grado di calcolare il prezzo totale che ritiene appropriato.</span><span class="sxs-lookup"><span data-stu-id="ae332-122">The plug-in can calculate the total price as it sees fit.</span></span>

<span data-ttu-id="ae332-123">Oltre a calcolare il prezzo totale di un acquisto, **CanBuySilent** determina se il purchace può procedere in modo invisibile all'utente; ovvero senza visualizzare una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ae332-123">In addition to calculating the total price of a purchase, **CanBuySilent** determines whether the purchace can proceed silently; that is, without displaying a dialog box.</span></span> <span data-ttu-id="ae332-124">Se **CanBuySilent** restituisce **True**, Windows Media Player semplicemente modifica il testo del pulsante Acquista per richiedere all'utente di confermare l'acquisto.</span><span class="sxs-lookup"><span data-stu-id="ae332-124">If **CanBuySilent** returns **True**, Windows Media Player simply changes the text on the Buy button to prompt the user to confirm the purchase.</span></span> <span data-ttu-id="ae332-125">Se **CanBuySilent** restituisce **False**, Windows Media Player visualizza una finestra di dialogo in cui viene richiesto all'utente di confermare l'acquisto.</span><span class="sxs-lookup"><span data-stu-id="ae332-125">If **CanBuySilent** returns **False**, Windows Media Player displays a dialog box that prompts the user to confirm the purchase.</span></span> <span data-ttu-id="ae332-126">La finestra di dialogo fornisce all'utente informazioni che riepilogano l'acquisto, ad esempio il numero di album, il numero di singole tracce e il prezzo totale (restituito dal plug-in).</span><span class="sxs-lookup"><span data-stu-id="ae332-126">The dialog box provides the user with information that summarizes the purchase like number of albums, number of individual tracks, and the total price (as returned by the plug-in).</span></span>

<span data-ttu-id="ae332-127">Dopo che l'utente ha confermato l'acquisto, il lettore chiama [IWMPContentPartner:: Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy).</span><span class="sxs-lookup"><span data-stu-id="ae332-127">After the user confirms the purchase, the Player calls [IWMPContentPartner::Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy).</span></span> <span data-ttu-id="ae332-128">Questa chiamata al metodo fornisce il plug-in con lo stesso elenco di contenitori di contenuto di **CanBuySilent**.</span><span class="sxs-lookup"><span data-stu-id="ae332-128">This method call provides the plug-in with the same content container list as **CanBuySilent**.</span></span> <span data-ttu-id="ae332-129">Quando si chiama **Acquista**, Windows Media Player fornisce anche un cookie (semplicemente un valore **DWORD** , univoco per la sessione) che il plug-in può usare per identificare la transazione.</span><span class="sxs-lookup"><span data-stu-id="ae332-129">When calling **Buy**, Windows Media Player also provides a cookie (simply a **DWORD** value, unique for the session) that the plug-in can use to identify the transaction.</span></span> <span data-ttu-id="ae332-130">Al termine della transazione, il plug-in deve chiamare [IWMPContentPartnerCallback:: BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), passando il valore del cookie originale per il parametro *dwBuyCookie* , per notificare al lettore che la transazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ae332-130">When the transaction is completed, the plug-in must call [IWMPContentPartnerCallback::BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), passing the original cookie value for the *dwBuyCookie* parameter, to notify the Player that the transaction is finished.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae332-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ae332-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae332-132">**Guida per programmatori per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="ae332-132">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




