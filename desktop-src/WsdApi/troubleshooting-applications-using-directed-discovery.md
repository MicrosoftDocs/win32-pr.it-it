---
description: Le applicazioni che usano l'individuazione diretta inviano messaggi Probe su HTTP o HTTPS per individuare i dispositivi.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Risoluzione dei problemi relativi alle applicazioni WSDAPI con individuazione diretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528573"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a><span data-ttu-id="aa1e4-103">Risoluzione dei problemi relativi alle applicazioni WSDAPI con individuazione diretta</span><span class="sxs-lookup"><span data-stu-id="aa1e4-103">Troubleshooting WSDAPI Applications Using Directed Discovery</span></span>

<span data-ttu-id="aa1e4-104">Le applicazioni che usano l'individuazione diretta inviano messaggi [Probe](probe-message.md) su http o HTTPS per individuare i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="aa1e4-104">Applications that use directed discovery send [Probe](probe-message.md) messages over HTTP or HTTPS to discover devices.</span></span> <span data-ttu-id="aa1e4-105">I messaggi [ProbeMatches](probematches-message.md) corrispondenti inviati in risposta vengono inviati anche tramite http o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="aa1e4-105">The corresponding [ProbeMatches](probematches-message.md) messages sent in response are also sent over HTTP or HTTPS.</span></span> <span data-ttu-id="aa1e4-106">L'individuazione diretta può essere avviata dall'aggiunta guidata stampante, da un client di individuazione funzioni o da un'applicazione WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="aa1e4-106">Directed discovery can be initiated by the Add Printer Wizard, a Function Discovery client, or a WSDAPI application.</span></span> <span data-ttu-id="aa1e4-107">I messaggi Probe e ProbeMatches sono strutturalmente identici a quelli inviati tramite UDP.</span><span class="sxs-lookup"><span data-stu-id="aa1e4-107">The Probe and ProbeMatches messages are structurally identical to those sent over UDP.</span></span> <span data-ttu-id="aa1e4-108">I messaggi sono preceduti dalle intestazioni HTTP o HTTPS appropriate.</span><span class="sxs-lookup"><span data-stu-id="aa1e4-108">The messages are prefixed with the appropriate HTTP or HTTPS headers.</span></span>

<span data-ttu-id="aa1e4-109">Le seguenti procedure di diagnostica devono essere utilizzate (in ordine) per identificare i problemi di un'applicazione mediante l'individuazione diretta.</span><span class="sxs-lookup"><span data-stu-id="aa1e4-109">The following diagnostic procedures should be used (in order) to help identify problems with an application using directed discovery.</span></span>

<span data-ttu-id="aa1e4-110">**Per risolvere i problemi di un'applicazione WSDAPI utilizzando l'individuazione diretta**</span><span class="sxs-lookup"><span data-stu-id="aa1e4-110">**To troubleshoot a WSDAPI application using directed discovery**</span></span>

1.  <span data-ttu-id="aa1e4-111">[Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="aa1e4-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="aa1e4-112">[Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="aa1e4-112">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
3.  <span data-ttu-id="aa1e4-113">[Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="aa1e4-113">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
4.  <span data-ttu-id="aa1e4-114">[Esaminare le tracce di rete per un'applicazione usando l'individuazione diretta](inspecting-network-traces-for-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="aa1e4-114">[Inspect network traces for an application using directed discovery](inspecting-network-traces-for-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="aa1e4-115">Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in [Abilitazione della traccia di WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aa1e4-115">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa1e4-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa1e4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa1e4-117">Introduzione con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="aa1e4-117">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="aa1e4-118">Risoluzione dei problemi relativi all'aggiunta guidata stampante</span><span class="sxs-lookup"><span data-stu-id="aa1e4-118">Troubleshooting the Add Printer Wizard</span></span>](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[<span data-ttu-id="aa1e4-119">Risoluzione dei problemi relativi alle applicazioni WSDAPI</span><span class="sxs-lookup"><span data-stu-id="aa1e4-119">Troubleshooting WSDAPI Applications</span></span>](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



