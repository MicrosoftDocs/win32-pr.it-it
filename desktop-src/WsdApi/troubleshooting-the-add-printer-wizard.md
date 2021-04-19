---
description: Elenca le procedure di diagnostica da utilizzare per la risoluzione dei problemi relativi all'aggiunta guidata stampante.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Risoluzione dei problemi relativi all'aggiunta guidata stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310269"
---
# <a name="troubleshooting-the-add-printer-wizard"></a><span data-ttu-id="aeea0-103">Risoluzione dei problemi relativi all'aggiunta guidata stampante</span><span class="sxs-lookup"><span data-stu-id="aeea0-103">Troubleshooting the Add Printer Wizard</span></span>

<span data-ttu-id="aeea0-104">Aggiunta guidata stampante:</span><span class="sxs-lookup"><span data-stu-id="aeea0-104">The Add Printer Wizard:</span></span>

-   <span data-ttu-id="aeea0-105">Usa sempre WS-Discovery UDP per l'individuazione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="aeea0-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="aeea0-106">Avvia sempre una connessione HTTP o HTTPS per lo scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="aeea0-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="aeea0-107">A volte usa l'individuazione diretta</span><span class="sxs-lookup"><span data-stu-id="aeea0-107">Sometimes uses directed discovery</span></span>
-   <span data-ttu-id="aeea0-108">USA a volte un canale sicuro (HTTPS) per lo scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="aeea0-108">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="aeea0-109">Le seguenti procedure di diagnostica devono essere utilizzate (in ordine) per facilitare l'identificazione dei problemi con l'aggiunta guidata stampante.</span><span class="sxs-lookup"><span data-stu-id="aeea0-109">The following diagnostic procedures should be used (in order) to help identify problems with the Add Printer Wizard.</span></span>

<span data-ttu-id="aeea0-110">**Per risolvere i problemi relativi all'aggiunta guidata stampante**</span><span class="sxs-lookup"><span data-stu-id="aeea0-110">**To troubleshoot the Add Printer Wizard**</span></span>

1.  <span data-ttu-id="aeea0-111">Se si usa l'individuazione diretta, [risolvere i problemi di individuazione diretta](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="aeea0-111">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="aeea0-112">[Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="aeea0-112">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="aeea0-113">[Utilizzare un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="aeea0-113">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="aeea0-114">[Usare il client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="aeea0-114">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="aeea0-115">[Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="aeea0-115">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="aeea0-116">[Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="aeea0-116">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="aeea0-117">[Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="aeea0-117">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="aeea0-118">[Esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="aeea0-118">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="aeea0-119">Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in [Abilitazione della traccia di WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aeea0-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aeea0-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aeea0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aeea0-121">Introduzione con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="aeea0-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="aeea0-122">Risoluzione dei problemi relativi alle applicazioni mediante l'individuazione diretta</span><span class="sxs-lookup"><span data-stu-id="aeea0-122">Troubleshooting Applications Using Directed Discovery</span></span>](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



