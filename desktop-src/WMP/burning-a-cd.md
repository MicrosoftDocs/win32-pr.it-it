---
title: Masterizzazione di un CD
description: Masterizzazione di un CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, informazioni
- masterizzazione di CDs, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117383"
---
# <a name="burning-a-cd"></a><span data-ttu-id="6fed4-112">Masterizzazione di un CD</span><span class="sxs-lookup"><span data-stu-id="6fed4-112">Burning a CD</span></span>

<span data-ttu-id="6fed4-113">Questa sezione descrive come usare l'interfaccia [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) per masterizzare musica in un CD.</span><span class="sxs-lookup"><span data-stu-id="6fed4-113">This section describes how to use the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface to burn music to a CD.</span></span> <span data-ttu-id="6fed4-114">L'interfaccia **IWMPCdromBurn** fornisce funzionalità per la masterizzazione di playlist in CDS come dati o tracce audio, nonché per cancellare CD-RW.</span><span class="sxs-lookup"><span data-stu-id="6fed4-114">The **IWMPCdromBurn** interface provides functionality for burning playlists to CDs as either data or audio tracks, as well as erasing CD-RWs.</span></span>

<span data-ttu-id="6fed4-115">Utilizzo del codice</span><span class="sxs-lookup"><span data-stu-id="6fed4-115">Code Usage</span></span>

<span data-ttu-id="6fed4-116">Gli esempi di codice in questa sezione usano le classi Active Template Library (ATL), ad esempio **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="6fed4-116">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

<span data-ttu-id="6fed4-117">Intestazioni incluse</span><span class="sxs-lookup"><span data-stu-id="6fed4-117">Included Headers</span></span>

<span data-ttu-id="6fed4-118">Per usare il codice in questa sezione, includere le intestazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6fed4-118">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



<span data-ttu-id="6fed4-119">Puntatori a interfaccia</span><span class="sxs-lookup"><span data-stu-id="6fed4-119">Interface Pointers</span></span>

<span data-ttu-id="6fed4-120">Le interfacce per Windows Media Player sono archiviate nelle variabili membro seguenti:</span><span class="sxs-lookup"><span data-stu-id="6fed4-120">The interfaces for Windows Media Player are stored in the following member variables:</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="6fed4-121">Gli argomenti seguenti descrivono come usare l'API di masterizzazione CD.</span><span class="sxs-lookup"><span data-stu-id="6fed4-121">The following topics describe how to use the CD burning API.</span></span>

-   [<span data-ttu-id="6fed4-122">Recupero dell'interfaccia di masterizzazione CD</span><span class="sxs-lookup"><span data-stu-id="6fed4-122">Retrieving the CD Burning Interface</span></span>](retrieving-the-cd-burning-interface.md)
-   [<span data-ttu-id="6fed4-123">Avvio del processo di masterizzazione</span><span class="sxs-lookup"><span data-stu-id="6fed4-123">Starting the Burn Process</span></span>](starting-the-burn-process.md)
-   [<span data-ttu-id="6fed4-124">Cancellazione di un CD riscrivibile</span><span class="sxs-lookup"><span data-stu-id="6fed4-124">Erasing a Rewritable CD</span></span>](erasing-a-rewritable-cd.md)
-   [<span data-ttu-id="6fed4-125">Recupero dello stato dell'unità e del disco</span><span class="sxs-lookup"><span data-stu-id="6fed4-125">Retrieving the Drive and Disc Status</span></span>](retrieving-the-drive-and-disc-status.md)
-   [<span data-ttu-id="6fed4-126">Recupero dello stato di masterizzazione</span><span class="sxs-lookup"><span data-stu-id="6fed4-126">Retrieving the Burn Status</span></span>](retrieving-the-burn-status.md)

## <a name="related-topics"></a><span data-ttu-id="6fed4-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6fed4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fed4-128">**Guida al controllo del lettore**</span><span class="sxs-lookup"><span data-stu-id="6fed4-128">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




