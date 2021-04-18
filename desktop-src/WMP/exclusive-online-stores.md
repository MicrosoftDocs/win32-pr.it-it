---
title: Negozi online esclusivi
description: Negozi online esclusivi
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player Online Stores, esclusivo
- negozi online, esclusivi
- digitare 1 Store online, esclusivo
- digitare 2 archivi online, esclusivi
- negozi online esclusivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299383"
---
# <a name="exclusive-online-stores"></a><span data-ttu-id="0cac2-108">Negozi online esclusivi</span><span class="sxs-lookup"><span data-stu-id="0cac2-108">Exclusive Online Stores</span></span>

<span data-ttu-id="0cac2-109">Con Windows Media Player 11, un'applicazione che incorpora il controllo Player in modalità remota può specificare un negozio online esclusivo.</span><span class="sxs-lookup"><span data-stu-id="0cac2-109">With Windows Media Player 11, an application that embeds the Player control remotely can specify an exclusive online store.</span></span> <span data-ttu-id="0cac2-110">In tal caso, il selettore di servizio in Windows Media Player è disabilitato e solo l'archivio online specificato è disponibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="0cac2-110">In that case, the service selector in Windows Media Player is disabled, and only the specified online store is available to the user.</span></span> <span data-ttu-id="0cac2-111">Inoltre, Windows Media Player adotta il colore specificato dall'elemento **color** del documento ServiceInfo del negozio online esclusivo.</span><span class="sxs-lookup"><span data-stu-id="0cac2-111">Also, Windows Media Player adopts the color specified by the **Color** element of the exclusive online store's ServiceInfo document.</span></span>

<span data-ttu-id="0cac2-112">Per specificare un archivio online esclusivo, un'applicazione deve aggiungere ExclusiveService:*nome* -chiavi alla fine della stringa restituita da [IWMPRemoteMediaServices:: GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span><span class="sxs-lookup"><span data-stu-id="0cac2-112">To specify an exclusive online store, an application must append ExclusiveService:*keyname* to the end of the string that it returns from [IWMPRemoteMediaServices::GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span></span> <span data-ttu-id="0cac2-113">Si supponga, ad esempio, che Proseware sia il nome della chiave assegnato a un particolare negozio online.</span><span class="sxs-lookup"><span data-stu-id="0cac2-113">For example, suppose Proseware is the key name given to a particular online store.</span></span> <span data-ttu-id="0cac2-114">Se **GetServiceType** restituisce la stringa "Remote ExclusiveService: proseware", Proseware sarà l'unico negozio online disponibile nel controllo lettore incorporato in remoto.</span><span class="sxs-lookup"><span data-stu-id="0cac2-114">If **GetServiceType** returns the string "Remote ExclusiveService:Proseware", then Proseware will be the only online store available in the remotely embedded Player control.</span></span>

<span data-ttu-id="0cac2-115">Un'applicazione può limitare il Media Player Windows a uno Store online esclusivo solo se Windows Media Player non è già in esecuzione quando viene avviata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0cac2-115">An application can limit Windows Media Player to an exclusive online store only if Windows Media Player is not already running when the application is launched.</span></span> <span data-ttu-id="0cac2-116">È responsabilità dell'applicazione informare l'utente che deve chiudere Windows Media Player prima di eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0cac2-116">It is the application's responsibility to inform the user that he or she must close Windows Media Player before running the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cac2-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cac2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cac2-118">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="0cac2-118">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="0cac2-119">**Gestione remota del controllo di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="0cac2-119">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




