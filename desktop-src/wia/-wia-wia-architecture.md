---
description: WIA viene implementato come un server out-of-process Component Object Model (COM) per assicurare il funzionamento affidabile delle applicazioni client.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Architettura WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652258ee249fb3c68e65472e863ccd35154ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568347"
---
# <a name="wia-architecture"></a><span data-ttu-id="9a1c2-103">Architettura WIA</span><span class="sxs-lookup"><span data-stu-id="9a1c2-103">WIA Architecture</span></span>

<span data-ttu-id="9a1c2-104">WIA viene implementato come un server out-of-process Component Object Model (COM) per assicurare il funzionamento affidabile delle applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="9a1c2-104">WIA is implemented as a Component Object Model (COM) out-of-process server to ensure the robust operation of client applications.</span></span> <span data-ttu-id="9a1c2-105">A differenza della maggior parte delle applicazioni del server di elaborazione, l'acquisizione di immagini Windows (WIA) evita le penalizzazioni delle prestazioni durante il trasferimento dei dati delle immagini fornendo un proprio meccanismo di trasferimento dei dati, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="9a1c2-105">Unlike most out of process server applications, Windows Image Acquisition (WIA) avoids performance penalties during image data transfer by providing its own data transfer mechanism, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span> <span data-ttu-id="9a1c2-106">Questa interfaccia a prestazioni elevate usa una finestra di memoria condivisa per trasferire i dati al client.</span><span class="sxs-lookup"><span data-stu-id="9a1c2-106">This high performance interface uses a shared memory window to transfer data to the client.</span></span>

<span data-ttu-id="9a1c2-107">WIA include tre componenti principali: un Gestione dispositivi, una libreria di servizi minidriver e un dispositivo minidriver.</span><span class="sxs-lookup"><span data-stu-id="9a1c2-107">WIA has three main components: a Device Manager, a Minidriver Service Library, and a Device Minidriver.</span></span>

-   <span data-ttu-id="9a1c2-108">Il Gestione dispositivi enumera i dispositivi di imaging, recupera le proprietà del dispositivo, imposta gli eventi per i dispositivi e crea oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a1c2-108">The Device Manager enumerates imaging devices, retrieves device properties, sets up events for devices, and creates device objects.</span></span>
-   <span data-ttu-id="9a1c2-109">La libreria del servizio minidriver implementa tutti i servizi indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a1c2-109">The Minidriver Service Library implements all services that are device independent.</span></span>
-   <span data-ttu-id="9a1c2-110">Il dispositivo minidriver esegue il mapping delle proprietà e dei comandi WIA al dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="9a1c2-110">The Device Minidriver maps WIA properties and commands to the specific device.</span></span>

<span data-ttu-id="9a1c2-111">Il diagramma seguente illustra l'architettura WIA:</span><span class="sxs-lookup"><span data-stu-id="9a1c2-111">The following diagram illustrates the WIA architecture:</span></span>

![architettura WIA](images/wiarch.gif)

 

 



