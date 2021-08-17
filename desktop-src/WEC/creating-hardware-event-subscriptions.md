---
title: Creazione di sottoscrizioni di eventi hardware
description: Nei computer in cui è installato baseboard Management Controller (BMC), gli eventi hardware vengono generati e registrati nel registro eventi di sistema (SEL), ovvero l'archivio eventi BMC archiviato nella memoria non volatile.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ee32d590143ed8a1ffacec6f59ad3b3094c2d2a22d0df66b0cb0d3521f83e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751113"
---
# <a name="creating-hardware-event-subscriptions"></a>Creazione di sottoscrizioni di eventi hardware

Nei computer in cui è installato baseboard Management Controller (BMC), gli eventi hardware vengono generati e registrati nel registro eventi di sistema (SEL), ovvero l'archivio eventi BMC archiviato nella memoria non volatile. Per leggere questi eventi hardware in Windows Server 2008 usando il Visualizzatore eventi, è necessario creare una sottoscrizione agli eventi. Le sottoscrizioni di eventi hardware funzionano solo Windows Server 2008.

La procedura seguente definisce come creare la sottoscrizione di eventi SEL per recuperare gli eventi hardware:

1.  Salvare il codice XML seguente in un file .xml (in questo esempio il file è denominato Wsmanselrg.xml). Questo codice XML definisce la sottoscrizione.

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

    

2.  Creare una sottoscrizione di eventi eseguendo il comando seguente in una finestra del prompt dei comandi (il programma Wecutil.exe si trova nella directory %SYSTEMROOT% \\ System32):

    **Wecutil cs** *<path> \\wsmanselrg.xml*

3.  Assicurarsi che la sottoscrizione sia attiva eseguendo il comando seguente in una finestra del prompt dei comandi:

    **Wecutil gr** *wsmanselrg*

BMC è un microcontroller collegato in locale a un server. I BBM hanno sensori che monitorano lo stato fisico del server e una connessione di rete separata in grado di comunicare in rete, anche se il server è offline. È possibile accedere ai dati BMC tramite il provider WMI IPMI (Intelligent Platform Management Interface). Per altre informazioni sul provider IPMI, vedere [Provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

Per il funzionamento della sottoscrizione di eventi, nel computer devono essere installati il BMC e il provider IPMI. Per i computer che eseguono Windows Server 2008, il provider IPMI viene installato per impostazione predefinita. Se il BMC non è disponibile, non è possibile installare il driver IPMI e lo stato del runtime della sottoscrizione visualizza sempre un errore (0x8004001 - Errore generico WMI).

 

 