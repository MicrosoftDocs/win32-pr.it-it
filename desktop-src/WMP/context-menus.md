---
title: Menu di scelta rapida
description: Menu di scelta rapida
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player Online Store, menu di scelta rapida
- archivi online, menu di scelta rapida
- digitare 1 archivi online, menu di scelta rapida
- Windows Media Player Online Stores, menu di scelta rapida personalizzati
- negozi online, menu di scelta rapida personalizzati
- digitare 1 archivi online, menu di scelta rapida personalizzati
- menu di scelta rapida
- menu di scelta rapida personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398542"
---
# <a name="context-menus"></a><span data-ttu-id="76636-111">Menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="76636-111">Context Menus</span></span>

<span data-ttu-id="76636-112">Gli archivi online possono fornire menu di scelta rapida personalizzati.</span><span class="sxs-lookup"><span data-stu-id="76636-112">Online stores can provide custom context menus.</span></span> <span data-ttu-id="76636-113">A tale scopo, il plug-in di archivio online implementa il metodo [IWMPContentPartner:: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) .</span><span class="sxs-lookup"><span data-stu-id="76636-113">To do this, the online store plug-in implements the [IWMPContentPartner::GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) method.</span></span> <span data-ttu-id="76636-114">Windows Media Player chiama questo metodo per fornire informazioni sul percorso nell'interfaccia utente in cui viene visualizzato il menu di scelta rapida (in cui l'utente ha fatto clic con il pulsante destro del mouse).</span><span class="sxs-lookup"><span data-stu-id="76636-114">Windows Media Player calls this method to provide information about the location in the user interface where the context menu is displayed (where the user right-clicked).</span></span> <span data-ttu-id="76636-115">Il plug-in restituisce una matrice di strutture [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) che descrivono ogni voce di menu di scelta rapida, incluso un ID di comando per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="76636-115">The plug-in returns an array of [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) structures that describe each context menu item, including a command ID for each.</span></span>

<span data-ttu-id="76636-116">Dopo che Windows Media Player ha recuperato la matrice, il giocatore usa la matrice per compilare il menu di scelta rapida visualizzato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="76636-116">After Windows Media Player has retrieved the array, the Player uses the array to build the context menu the user sees.</span></span> <span data-ttu-id="76636-117">Quando l'utente fa clic su un elemento nel menu di scelta rapida, il lettore chiama [IWMPContentPartner:: InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passando l'ID di comando associato alla voce di menu tramite il parametro *dwCommandID* .</span><span class="sxs-lookup"><span data-stu-id="76636-117">When the user clicks an item in the context menu, the Player calls [IWMPContentPartner::InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passing the command ID associated with the menu item through the *dwCommandID* parameter.</span></span> <span data-ttu-id="76636-118">Il lettore passa anche un valore del percorso della libreria e una matrice di ID che rappresenta gli elementi su cui è stato richiamato il menu, ad esempio una matrice di ID di traccia.</span><span class="sxs-lookup"><span data-stu-id="76636-118">The Player also passes a library location value and an array of IDs that represents the items the menu was invoked upon, such as an array of track IDs.</span></span> <span data-ttu-id="76636-119">Utilizzando queste informazioni, il plug-in può avviare qualsiasi processo appropriato in risposta al clic del mouse dell'utente.</span><span class="sxs-lookup"><span data-stu-id="76636-119">By using this information, the plug-in can start any appropriate process in response to the user's mouse click.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76636-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76636-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76636-121">**Informazioni sugli archivi online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="76636-121">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




