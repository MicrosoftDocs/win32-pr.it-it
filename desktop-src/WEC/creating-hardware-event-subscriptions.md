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
# <a name="creating-hardware-event-subscriptions"></a>Creazione di sottoscrizioni di eventi hardware

Nei computer in cui è installato un controller di gestione di battiscopa (BMC), gli eventi hardware vengono generati e registrati nel registro eventi di sistema (SEL), ovvero l'archivio eventi BMC archiviato nella memoria non volatile. Per leggere questi eventi hardware in Windows Server 2008 usando il Visualizzatore eventi, è necessario creare una sottoscrizione agli eventi. Le sottoscrizioni di eventi hardware funzioneranno solo in Windows Server 2008.

Nella procedura seguente viene illustrato come creare la sottoscrizione di eventi SEL per recuperare gli eventi hardware:

1.  Salvare il codice XML seguente in un file con estensione XML (in questo esempio il file è denominato Wsmanselrg.xml). Questo XML definisce la sottoscrizione.

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

    

2.  Creare una sottoscrizione di eventi eseguendo il comando seguente in una finestra del prompt dei comandi (il programma Wecutil.exe si trova nella directory% SYSTEMROOT% \\ System32):

    *<path> \\wsmanselrg.xml* **CS wecutil**

3.  Verificare che la sottoscrizione sia attiva eseguendo il comando seguente in una finestra del prompt dei comandi:

    **Wecutil gr** *wsmanselrg*

Il BMC è un microcontroller collegato localmente a un server. BMC hanno sensori che monitorano lo stato fisico del server e una connessione di rete separata in grado di comunicare in rete, anche se il server è offline. È possibile accedere ai dati BMC tramite il provider WMI IPMI (Intelligent Platform Management Interface). Per ulteriori informazioni sul provider IPMI, vedere [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

Per il corretto funzionamento della sottoscrizione di eventi, nel computer deve essere installato il BMC e il provider IPMI. Per i computer che eseguono Windows Server 2008, il provider IPMI viene installato per impostazione predefinita. Se il BMC non è disponibile, non è possibile installare il driver IPMI e lo stato di runtime della sottoscrizione visualizzerà sempre un errore (0x8004001-errore generico WMI).

 

 