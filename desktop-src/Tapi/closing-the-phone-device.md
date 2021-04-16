---
description: La funzione phoneClose chiude il dispositivo telefonico specificato.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Chiusura del dispositivo telefonico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527234"
---
# <a name="closing-the-phone-device"></a><span data-ttu-id="6e744-103">Chiusura del dispositivo telefonico</span><span class="sxs-lookup"><span data-stu-id="6e744-103">Closing the Phone Device</span></span>

<span data-ttu-id="6e744-104">La funzione [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) chiude il dispositivo telefonico specificato.</span><span class="sxs-lookup"><span data-stu-id="6e744-104">The [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) function closes the specified phone device.</span></span> <span data-ttu-id="6e744-105">Il dispositivo telefonico può anche essere chiuso forzatamente dopo che l'utente ha modificato la configurazione del telefono o del driver.</span><span class="sxs-lookup"><span data-stu-id="6e744-105">The phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="6e744-106">Se l'utente desidera che le modifiche di configurazione vengano applicate immediatamente (a differenza di dopo il successivo riavvio del sistema) e influiscono sulla visualizzazione corrente dell'applicazione del dispositivo (ad esempio una modifica delle funzionalità del dispositivo), un provider di servizi può chiudere forzatamente il dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="6e744-106">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

<span data-ttu-id="6e744-107">Questi messaggi possono anche essere inviati non richiesti a causa del mancato rimborso del dispositivo telefonico in un altro modo.</span><span class="sxs-lookup"><span data-stu-id="6e744-107">These messages can also be sent unsolicited as a result of the phone device being reclaimed in some other manner.</span></span> <span data-ttu-id="6e744-108">Un'applicazione deve pertanto essere preparata a gestire messaggi di [**\_ chiusura telefono**](phone-close.md) non richiesti.</span><span class="sxs-lookup"><span data-stu-id="6e744-108">An application should therefore be prepared to handle unsolicited [**PHONE\_CLOSE**](phone-close.md) messages.</span></span> <span data-ttu-id="6e744-109">Al momento della chiusura del dispositivo telefonico, tutte le risposte asincrone in sospeso relative a tale dispositivo vengono cancellate.</span><span class="sxs-lookup"><span data-stu-id="6e744-109">At the time the phone device is closed, any outstanding asynchronous replies pertaining to that device are suppressed.</span></span>

 

 



