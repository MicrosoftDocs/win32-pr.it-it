---
description: Elenca le procedure di diagnostica da utilizzare per la risoluzione dei problemi relativi alla procedura guidata del proiettore.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Risoluzione dei problemi relativi alla procedura guidata del proiettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306865"
---
# <a name="troubleshooting-the-projector-wizard"></a><span data-ttu-id="afdfb-103">Risoluzione dei problemi relativi alla procedura guidata del proiettore</span><span class="sxs-lookup"><span data-stu-id="afdfb-103">Troubleshooting the Projector Wizard</span></span>

<span data-ttu-id="afdfb-104">Creazione guidata proiettore:</span><span class="sxs-lookup"><span data-stu-id="afdfb-104">The Projector Wizard:</span></span>

-   <span data-ttu-id="afdfb-105">Usa sempre WS-Discovery UDP per l'individuazione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="afdfb-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="afdfb-106">Usa sempre HTTP per lo scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="afdfb-106">Always uses HTTP for metadata exchange</span></span>
-   <span data-ttu-id="afdfb-107">A volte usa l'individuazione diretta</span><span class="sxs-lookup"><span data-stu-id="afdfb-107">Sometimes uses directed discovery</span></span>

<span data-ttu-id="afdfb-108">Per identificare i problemi relativi alla procedura guidata del proiettore, è necessario utilizzare le seguenti procedure di diagnostica (in ordine).</span><span class="sxs-lookup"><span data-stu-id="afdfb-108">The following diagnostic procedures should be used (in order) to help identify problems with the Projector Wizard.</span></span>

<span data-ttu-id="afdfb-109">**Per risolvere i problemi relativi alla procedura guidata del proiettore**</span><span class="sxs-lookup"><span data-stu-id="afdfb-109">**To troubleshoot the Projector Wizard**</span></span>

1.  <span data-ttu-id="afdfb-110">Se si usa l'individuazione diretta, [risolvere i problemi di individuazione diretta](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="afdfb-110">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="afdfb-111">[Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="afdfb-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="afdfb-112">[Utilizzare un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="afdfb-112">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="afdfb-113">[Usare il client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="afdfb-113">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="afdfb-114">[Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="afdfb-114">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="afdfb-115">[Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="afdfb-115">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="afdfb-116">[Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="afdfb-116">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="afdfb-117">[Esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="afdfb-117">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="afdfb-118">Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in [Abilitazione della traccia di WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="afdfb-118">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afdfb-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afdfb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afdfb-120">Introduzione con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="afdfb-120">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



