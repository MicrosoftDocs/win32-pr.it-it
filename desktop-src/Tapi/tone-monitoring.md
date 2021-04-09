---
description: Il monitoraggio dei toni monitora il flusso multimediale di una chiamata per i toni specificati.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Monitoraggio del tono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050128"
---
# <a name="tone-monitoring"></a><span data-ttu-id="9164c-103">Monitoraggio del tono</span><span class="sxs-lookup"><span data-stu-id="9164c-103">Tone Monitoring</span></span>

<span data-ttu-id="9164c-104">Il monitoraggio dei toni monitora il flusso multimediale di una chiamata per i toni specificati.</span><span class="sxs-lookup"><span data-stu-id="9164c-104">Tone monitoring monitors the media stream of a call for specified tones.</span></span> <span data-ttu-id="9164c-105">Un tono è descritto dalle frequenze e dalla cadenza dei componenti.</span><span class="sxs-lookup"><span data-stu-id="9164c-105">A tone is described by its component frequencies and cadence.</span></span> <span data-ttu-id="9164c-106">Un'implementazione dell'API può consentire il monitoraggio simultaneo di diversi colori.</span><span class="sxs-lookup"><span data-stu-id="9164c-106">An implementation of the API may allow several different tones to be monitored simultaneously.</span></span> <span data-ttu-id="9164c-107">Un'applicazione può contrassegnare ogni tono per poter distinguere i diversi toni per i quali richiede il rilevamento.</span><span class="sxs-lookup"><span data-stu-id="9164c-107">An application can tag each tone to be able to distinguish the different tones for which it requests detection.</span></span>

<span data-ttu-id="9164c-108">Un'applicazione può abilitare o disabilitare il monitoraggio dei toni per una chiamata specificata con [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span><span class="sxs-lookup"><span data-stu-id="9164c-108">An application can enable or disable tone monitoring on a specified call with [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span></span> <span data-ttu-id="9164c-109">Con questa funzione, l'applicazione indica quali toni rilevare in una chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="9164c-109">With this function, the application indicates which tones to detect on a specified call.</span></span> <span data-ttu-id="9164c-110">Quando il monitoraggio dei toni è abilitato, le cifre rilevate fanno sì che l'applicazione riceva una notifica con il messaggio di [**riga \_ MONITORTONE**](line-monitortone.md) .</span><span class="sxs-lookup"><span data-stu-id="9164c-110">When tone monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORTONE**](line-monitortone.md) message.</span></span> <span data-ttu-id="9164c-111">Questo messaggio fornisce l'handle di chiamata su cui è stato rilevato il tono e il tag dell'applicazione per il tono.</span><span class="sxs-lookup"><span data-stu-id="9164c-111">This message provides the call handle on which the tone was detected as well as the application's tag for the tone.</span></span>

<span data-ttu-id="9164c-112">L'ambito del monitoraggio del tono è associato alla durata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="9164c-112">The scope of tone monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="9164c-113">Il monitoraggio dei toni in una chiamata termina non appena la chiamata si *disconnette* o diventa *inattiva*.</span><span class="sxs-lookup"><span data-stu-id="9164c-113">Tone monitoring on a call ends as soon the call *disconnects* or goes *idle*.</span></span>

> [!Note]  
> <span data-ttu-id="9164c-114">Il monitoraggio di toni, cifre o tipi di supporti spesso richiede l'uso di risorse di cui il provider di servizi può avere solo un importo finito.</span><span class="sxs-lookup"><span data-stu-id="9164c-114">The monitoring of tones, digits, or media types often requires the use of resources of which the service provider can only have a finite amount.</span></span> <span data-ttu-id="9164c-115">Una richiesta di monitoraggio può essere rifiutata se le risorse non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="9164c-115">A request for monitoring can be rejected if resources are not available.</span></span> <span data-ttu-id="9164c-116">Per lo stesso motivo, un'applicazione deve disabilitare eventuali monitoraggi superflui.</span><span class="sxs-lookup"><span data-stu-id="9164c-116">For the same reason, an application should disable any unnecessary monitoring.</span></span>

 

 

 



