---
title: Ripping mediante l'interfaccia IWMPCdromRip
description: Ripping mediante l'interfaccia IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping del CD, interfaccia IWMPCdromRip
- ripping di CDs, interfaccia IWMPCdromRip
- Interfaccia IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858022"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a><span data-ttu-id="49573-113">Ripping mediante l'interfaccia IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="49573-113">Ripping by Using the IWMPCdromRip Interface</span></span>

<span data-ttu-id="49573-114">Questa sezione descrive come usare l'interfaccia [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) per rippare musica da un CD.</span><span class="sxs-lookup"><span data-stu-id="49573-114">This section describes how to use the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface to rip music from a CD.</span></span>

<span data-ttu-id="49573-115">La copia di un CD usando l'interfaccia **IWMPCdromRip** ha lo stesso effetto del ritaglio di musica usando l'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="49573-115">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="49573-116">Il contenuto Ripped viene aggiunto automaticamente alla libreria in base alle preferenze dell'utente.</span><span class="sxs-lookup"><span data-stu-id="49573-116">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="49573-117">Per ulteriori informazioni su come rippare i CD, vedere l'argomento relativo all'estrazione di musica da CDs nella Guida di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="49573-117">For more information about CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

<span data-ttu-id="49573-118">Gli esempi di codice in questa sezione usano le classi Active Template Library (ATL), ad esempio **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="49573-118">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="49573-119">Intestazioni incluse</span><span class="sxs-lookup"><span data-stu-id="49573-119">Included Headers</span></span>

<span data-ttu-id="49573-120">Per usare il codice in questa sezione, includere le intestazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="49573-120">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a><span data-ttu-id="49573-121">Puntatori a interfaccia</span><span class="sxs-lookup"><span data-stu-id="49573-121">Interface Pointers</span></span>

<span data-ttu-id="49573-122">Le interfacce per Windows Media Player sono archiviate nelle variabili membro seguenti.</span><span class="sxs-lookup"><span data-stu-id="49573-122">The interfaces for Windows Media Player are stored in the following member variables.</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="49573-123">Le sezioni seguenti descrivono come usare l'interfaccia IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="49573-123">The Following Sections Describe How to Use the IWMPCdromRip Interface</span></span>

-   [<span data-ttu-id="49573-124">Recupero dell'interfaccia di copia da CD</span><span class="sxs-lookup"><span data-stu-id="49573-124">Retrieving the Ripping Interface</span></span>](retrieving-the-ripping-interface.md)
-   [<span data-ttu-id="49573-125">Avvio del processo RIP</span><span class="sxs-lookup"><span data-stu-id="49573-125">Starting the Rip Process</span></span>](starting-the-rip-process.md)
-   [<span data-ttu-id="49573-126">Recupero dello stato di RIP</span><span class="sxs-lookup"><span data-stu-id="49573-126">Retrieving the Rip Status</span></span>](retrieving-the-rip-status.md)
-   [<span data-ttu-id="49573-127">Selezione di elementi per l'estrazione</span><span class="sxs-lookup"><span data-stu-id="49573-127">Selecting Items for Ripping</span></span>](selecting-items-for-ripping.md)

 

 




