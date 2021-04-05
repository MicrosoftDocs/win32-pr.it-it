---
description: Questo evento viene pubblicato dal controllo ScrollableText per consentire all'utente di stampare il contenuto del controllo.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: ControlEvent MsiPrint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885289"
---
# <a name="msiprint-controlevent"></a><span data-ttu-id="481cc-103">ControlEvent MsiPrint</span><span class="sxs-lookup"><span data-stu-id="481cc-103">MsiPrint ControlEvent</span></span>

<span data-ttu-id="481cc-104">Questo evento viene pubblicato dal [controllo ScrollableText](scrollabletext-control.md) per consentire all'utente di stampare il contenuto del controllo.</span><span class="sxs-lookup"><span data-stu-id="481cc-104">This event is published by the [ScrollableText Control](scrollabletext-control.md) to enable the user to print the contents of that control.</span></span>

<span data-ttu-id="481cc-105">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="481cc-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="481cc-106">Questo ControlEvent è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="481cc-106">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="481cc-107">Questo evento deve essere sottoscritto da un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo del [controllo ScrollableText](scrollabletext-control.md).</span><span class="sxs-lookup"><span data-stu-id="481cc-107">This event should be subscribed to by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the [ScrollableText Control](scrollabletext-control.md).</span></span> <span data-ttu-id="481cc-108">TheMsiPrint ControlEvent deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="481cc-108">TheMsiPrint ControlEvent should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="481cc-109">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="481cc-109">Published By</span></span>

[<span data-ttu-id="481cc-110">ScrollableText</span><span class="sxs-lookup"><span data-stu-id="481cc-110">ScrollableText</span></span>](scrollabletext-control.md)

## <a name="argument"></a><span data-ttu-id="481cc-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="481cc-111">Argument</span></span>

<span data-ttu-id="481cc-112">Questo ControlEvent non usa un argomento.</span><span class="sxs-lookup"><span data-stu-id="481cc-112">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="481cc-113">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="481cc-113">Action on Subscribers</span></span>

<span data-ttu-id="481cc-114">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="481cc-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="481cc-115">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="481cc-115">Typical Use</span></span>

<span data-ttu-id="481cc-116">È possibile utilizzare un controllo [pulsante](pushbutton-control.md) nella stessa finestra di dialogo del [controllo ScrollableText](scrollabletext-control.md) per visualizzare una finestra di dialogo modale che consente all'utente di stampare il contenuto del controllo ScrollableText.</span><span class="sxs-lookup"><span data-stu-id="481cc-116">A [PushButton](pushbutton-control.md) control on the same dialog box as the [ScrollableText Control](scrollabletext-control.md) can be used to display a modal dialog box enabling the user to print the contents of the ScrollableText Control.</span></span>

 

 



