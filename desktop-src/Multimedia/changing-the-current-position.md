---
title: Modifica della posizione corrente
description: Modifica della posizione corrente
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK messaggio di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235dc2639d7d9fc01f94aff700ae9e0ebf1dcbe2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399035"
---
# <a name="changing-the-current-position"></a><span data-ttu-id="33220-104">Modifica della posizione corrente</span><span class="sxs-lookup"><span data-stu-id="33220-104">Changing the Current Position</span></span>

<span data-ttu-id="33220-105">Per modificare la posizione corrente in un elemento del dispositivo, usare il messaggio del comando di [**\_ ricerca MCI**](mci-seek.md) insieme al \_ flag MCI to e la struttura [**\_ \_ parametri Seek di MCI**](mci-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="33220-105">To change the current position in a device element, use the [**MCI\_SEEK**](mci-seek.md) command message along with the MCI\_TO flag and the [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="33220-106">Se si usa il membro **dwTo** per specificare una posizione di ricerca con MCI \_ Seek, è necessario eseguire una query sul formato dell'ora e impostarlo, se necessario.</span><span class="sxs-lookup"><span data-stu-id="33220-106">If you use the **dwTo** member to specify a seek position with MCI\_SEEK, you should query the time format and set it, if necessary.</span></span>

<span data-ttu-id="33220-107">Oltre a specificare una posizione con il membro **dwTo** , è possibile specificare i flag di \_ ricerca MCI \_ da \_ avviare o MCI \_ Seek \_ to \_ end per il parametro *dwParam1* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per trovare le posizioni iniziale e finale dell'elemento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33220-107">In addition to specifying a position with the **dwTo** member, you can specify the MCI\_SEEK\_TO\_START or MCI\_SEEK\_TO\_END flags for the *dwParam1* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to find the starting and ending positions of the device element.</span></span> <span data-ttu-id="33220-108">Se si usa uno di questi flag, non specificare l'oggetto MCI \_ da contrassegnare.</span><span class="sxs-lookup"><span data-stu-id="33220-108">If you use one of these flags, don't specify the MCI\_TO flag.</span></span>

 

 