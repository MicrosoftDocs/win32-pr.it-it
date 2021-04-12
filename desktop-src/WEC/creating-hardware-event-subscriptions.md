---
title: Creazione di sottoscrizioni di eventi hardware
description: Nei computer in cui è installato un controller di gestione di battiscopa (BMC), gli eventi hardware vengono generati e registrati nel registro eventi di sistema (SEL), ovvero l'archivio eventi BMC archiviato nella memoria non volatile.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5f904e74d1f29b0666c9cb02b13689a0633bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338518"
---
# <a name="creating-hardware-event-subscriptions"></a><span data-ttu-id="791e1-103">Creazione di sottoscrizioni di eventi hardware</span><span class="sxs-lookup"><span data-stu-id="791e1-103">Creating Hardware Event Subscriptions</span></span>

<span data-ttu-id="791e1-104">Nei computer in cui è installato un controller di gestione di battiscopa (BMC), gli eventi hardware vengono generati e registrati nel registro eventi di sistema (SEL), ovvero l'archivio eventi BMC archiviato nella memoria non volatile.</span><span class="sxs-lookup"><span data-stu-id="791e1-104">On computers that have a Baseboard Management Controller (BMC) installed, hardware events are raised and logged in the System event log (SEL), which is the BMC event store that is stored in nonvolatile memory.</span></span> <span data-ttu-id="791e1-105">Per leggere questi eventi hardware in Windows Server 2008 usando il Visualizzatore eventi, è necessario creare una sottoscrizione agli eventi.</span><span class="sxs-lookup"><span data-stu-id="791e1-105">To read these hardware events on Windows Server 2008 using the Event Viewer, you must create a subscription to the events.</span></span> <span data-ttu-id="791e1-106">Le sottoscrizioni di eventi hardware funzioneranno solo in Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="791e1-106">The hardware event subscriptions will only work on Windows Server 2008.</span></span>

<span data-ttu-id="791e1-107">Nella procedura seguente viene illustrato come creare la sottoscrizione di eventi SEL per recuperare gli eventi hardware:</span><span class="sxs-lookup"><span data-stu-id="791e1-107">The following procedure defines how to create the SEL event subscription to retrieve the hardware events:</span></span>

1.  <span data-ttu-id="791e1-108">Salvare il codice XML seguente in un file con estensione XML (in questo esempio il file è denominato Wsmanselrg.xml).</span><span class="sxs-lookup"><span data-stu-id="791e1-108">Save the following XML in an .xml file (in this example the file is named Wsmanselrg.xml).</span></span> <span data-ttu-id="791e1-109">Questo XML definisce la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="791e1-109">This XML defines the subscription.</span></span>

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  <span data-ttu-id="791e1-110">Creare una sottoscrizione di eventi eseguendo il comando seguente in una finestra del prompt dei comandi (il programma Wecutil.exe si trova nella directory% SYSTEMROOT% \\ System32):</span><span class="sxs-lookup"><span data-stu-id="791e1-110">Create an event subscription by executing the following command in a command prompt window (the Wecutil.exe program is located in the %SYSTEMROOT%\\System32 directory.):</span></span>

    <span data-ttu-id="791e1-111">*<path> \\wsmanselrg.xml* **CS wecutil**</span><span class="sxs-lookup"><span data-stu-id="791e1-111">**Wecutil cs** *<path>\\wsmanselrg.xml*</span></span>

3.  <span data-ttu-id="791e1-112">Verificare che la sottoscrizione sia attiva eseguendo il comando seguente in una finestra del prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="791e1-112">Ensure that the subscription is active by executing the following command in a command prompt window:</span></span>

    <span data-ttu-id="791e1-113">**Wecutil gr** *wsmanselrg*</span><span class="sxs-lookup"><span data-stu-id="791e1-113">**Wecutil gr** *wsmanselrg*</span></span>

<span data-ttu-id="791e1-114">Il BMC è un microcontroller collegato localmente a un server.</span><span class="sxs-lookup"><span data-stu-id="791e1-114">The BMC is a microcontroller attached locally to a server.</span></span> <span data-ttu-id="791e1-115">BMC hanno sensori che monitorano lo stato fisico del server e una connessione di rete separata in grado di comunicare in rete, anche se il server è offline.</span><span class="sxs-lookup"><span data-stu-id="791e1-115">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="791e1-116">È possibile accedere ai dati BMC tramite il provider WMI IPMI (Intelligent Platform Management Interface).</span><span class="sxs-lookup"><span data-stu-id="791e1-116">You have access to BMC data through the Intelligent Platform Management Interface (IPMI) WMI Provider.</span></span> <span data-ttu-id="791e1-117">Per ulteriori informazioni sul provider IPMI, vedere [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="791e1-117">For more information about the IPMI provider, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

<span data-ttu-id="791e1-118">Per il corretto funzionamento della sottoscrizione di eventi, nel computer deve essere installato il BMC e il provider IPMI.</span><span class="sxs-lookup"><span data-stu-id="791e1-118">The computer must have the BMC and the IPMI provider installed for the event subscription to work.</span></span> <span data-ttu-id="791e1-119">Per i computer che eseguono Windows Server 2008, il provider IPMI viene installato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="791e1-119">For computers running on Windows Server 2008, the IPMI provider is installed by default.</span></span> <span data-ttu-id="791e1-120">Se il BMC non è disponibile, non è possibile installare il driver IPMI e lo stato di runtime della sottoscrizione visualizzerà sempre un errore (0x8004001-errore generico WMI).</span><span class="sxs-lookup"><span data-stu-id="791e1-120">If the BMC is not available, then IPMI driver cannot be installed and the subscription runtime status will always display an error (0x8004001 - WMI Generic Failure).</span></span>

 

 