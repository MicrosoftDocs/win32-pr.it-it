---
description: Una classe dispositivo è un gruppo di dispositivi fisici o driver di dispositivo correlati attraverso i quali le applicazioni inviano e ricevono le informazioni o i dati che costituiscono una chiamata.
ms.assetid: 859979a8-0d16-4b7b-b183-d6e30f3e034d
title: Classi di dispositivi TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d68e07359468e7a3ba3a1e73c3e0888076e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319855"
---
# <a name="tapi-device-classes"></a>Classi di dispositivi TAPI

Una classe dispositivo è un gruppo di dispositivi fisici o driver di dispositivo correlati attraverso i quali le applicazioni inviano e ricevono le informazioni o i dati che costituiscono una chiamata. Ogni classe Device ha un *nome di classe del dispositivo* che identifica in modo univoco la classe e fornisce informazioni sull'interfaccia di programmazione e i comandi che possono essere usati per aprire e comunicare con i dispositivi nella classe.

L'interfaccia TAPI (Telephony Application Programming Interface) associa i dispositivi di una o più classi di dispositivi a ogni riga o dispositivo telefonico. Per accedere a uno di questi dispositivi, è possibile recuperare l'identificatore del dispositivo usando la funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) o [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) . Specificare il nome della classe del dispositivo e la funzione restituisce il nome della porta, il nome del dispositivo, l'handle del dispositivo o l'identificatore del dispositivo specifici che è necessario aprire e accedere al dispositivo. Il formato delle informazioni restituite dipende dalla classe del dispositivo ed è descritto negli argomenti successivi di questa sezione.

Si usano anche i nomi delle classi del dispositivo con le funzioni [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) e [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) per consentire all'utente di impostare le opzioni di configurazione per il dispositivo specificato, con le funzioni [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon) e [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon) per recuperare un'icona per rappresentare il dispositivo specificato e con le funzioni [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) per recuperare e impostare direttamente le opzioni di configurazione per il dispositivo specificato.

L'elenco seguente illustra i nomi delle classi di dispositivi.



| Nome classe dispositivo                                      | Descrizione                                       |
|--------------------------------------------------------|---------------------------------------------------|
| [comunicazione](comm.md)                                       | Porta di comunicazione.                              |
| [comunicazione/datamode](comm-datamodem.md)                   | Modem tramite una porta di comunicazione.              |
| [comm/DataModel/PortName](comm-datamodem-portname.md) | Nome del dispositivo a cui è connesso un modem. |
| [Wave/in](wave-in.md)                                 | Dispositivo audio Wave (solo input).                   |
| [Wave/out](wave-out.md)                               | Dispositivo audio Wave (solo output).                  |
| [Wave/in/out](wave-in-out.md)                         | Dispositivo audio Wave, full duplex.                   |
| [MIDI/in](midi-in.md)                                 | MIDI sequencer (solo input).                      |
| [MIDI/out](midi-out.md)                               | MIDI sequencer (solo output).                     |
| [TAPI/linea](tapi-line.md)                             | Dispositivo linea.                                      |
| [TAPI/Phone](tapi-phone.md)                           | Dispositivo telefonico.                                     |
| [NDIS](ndis.md)                                       | Dispositivo di rete.                                   |
| [TAPI/terminale](tapi-terminal.md)                     | Dispositivo terminal.                                  |



 

> [!Note]  
> Questi nomi non fanno distinzione tra maiuscole e minuscole. è possibile utilizzare qualsiasi combinazione di lettere maiuscole e minuscole.

 

È possibile che in un sistema specifico siano disponibili classi di dispositivi e nomi di classi di dispositivi aggiuntivi. In generale, se un dispositivo non appartiene a una delle classi di dispositivo predefinite, il produttore definisce in genere una nuova classe di dispositivi e assegna un nome di classe del dispositivo univoco. Controllare la documentazione del dispositivo per determinare le altre classi di dispositivi disponibili. Si noti, tuttavia, che anche se la classe del dispositivo e il tipo di supporto sono correlati, non sono uguali. Un tipo di supporto descrive il formato delle informazioni sulle chiamate e una classe di dispositivi definisce l'interfaccia di programmazione utilizzata per gestire tali informazioni. Pertanto, anche se un produttore definisce un nuovo tipo di supporto, non è necessariamente vero che il produttore debba anche definire una nuova classe di dispositivi per supportare la modalità.

Il formato dei dati di configurazione usati con le funzioni [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) e [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) dipende anche dalla classe Device. In generale, si usa **lineGetDevConfig** per salvare una copia dei dati di configurazione del dispositivo corrente e successivamente usare **lineSetDevConfig** con i dati di configurazione salvati per ripristinare lo stato precedente della configurazione del dispositivo. Si tratta di un modo pratico per modificare temporaneamente la configurazione senza richiedere all'utente di ripristinare manualmente lo stato precedente. Poiché il formato esatto dei dati di configurazione del dispositivo può essere diverso con ogni provider di servizi, è consigliabile non usare **lineSetDevConfig** e **lineGetDevConfig** per modificare direttamente i dati di configurazione del dispositivo. Alcuni formati sono disponibili solo per le informazioni.

 

 



