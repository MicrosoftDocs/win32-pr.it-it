---
description: Informazioni sulle classi di dispositivi TAPI. Una classe di dispositivo è un gruppo di dispositivi o driver di dispositivo tramite cui le applicazioni inviano e ricevono dati o informazioni sulle chiamate.
ms.assetid: 859979a8-0d16-4b7b-b183-d6e30f3e034d
title: Classi di dispositivi TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f277e74012241139cf619c5229c4525711d93304f7321809461aff13416e62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975481"
---
# <a name="tapi-device-classes"></a>Classi di dispositivi TAPI

Una classe di dispositivo è un gruppo di dispositivi fisici correlati o driver di dispositivo tramite i quali le applicazioni inviano e ricevono le informazioni o i dati che costituisce una chiamata. Ogni classe di  dispositivo ha un nome di classe di dispositivo che identifica in modo univoco la classe e fornisce informazioni sull'interfaccia di programmazione e sui comandi che possono essere usati per aprire e comunicare con i dispositivi nella classe .

TapI (Telephony Application Programming Interface) associa i dispositivi di una o più classi di dispositivi a ogni dispositivo linea o telefono. È possibile accedere a uno di questi dispositivi recuperando l'identificatore del dispositivo usando la [**funzione lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) [**o phoneGetID.**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) Si specifica il nome della classe del dispositivo e la funzione restituisce il nome della porta, il nome del dispositivo, l'handle del dispositivo o l'identificatore di dispositivo specifico che è necessario aprire e accedere al dispositivo. Il formato delle informazioni restituite dipende dalla classe del dispositivo ed è descritto negli argomenti successivi di questa sezione.

Si usano anche i nomi delle classi di dispositivo con le funzioni [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) e [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) per consentire all'utente di impostare le opzioni di configurazione per il dispositivo specificato, con le funzioni [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon) e [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon) per recuperare un'icona per rappresentare il dispositivo specificato e con le funzioni [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) per recuperare e impostare direttamente le opzioni di configurazione per il dispositivo specificato.

L'elenco seguente mostra i nomi delle classi di dispositivo.



| Nome della classe del dispositivo                                      | Descrizione                                       |
|--------------------------------------------------------|---------------------------------------------------|
| [Comm](comm.md)                                       | Porta di comunicazione.                              |
| [comm/datamodem](comm-datamodem.md)                   | Modem tramite una porta di comunicazione.              |
| [comm/datamodem/portname](comm-datamodem-portname.md) | Nome del dispositivo a cui è connesso un modem. |
| [wave/in](wave-in.md)                                 | Dispositivo audio Wave (solo input).                   |
| [wave/out](wave-out.md)                               | Dispositivo audio Wave (solo output).                  |
| [wave/in/out](wave-in-out.md)                         | Dispositivo audio Wave, full duplex.                   |
| [midi/in](midi-in.md)                                 | Sequencer MIDI (solo input).                      |
| [midi/out](midi-out.md)                               | Sequencer MIDI (solo output).                     |
| [tapi/line](tapi-line.md)                             | Dispositivo line.                                      |
| [tapi/phone](tapi-phone.md)                           | Telefono dispositivo.                                     |
| [Ndis](ndis.md)                                       | Dispositivo di rete.                                   |
| [tapi/terminale](tapi-terminal.md)                     | Dispositivo terminale.                                  |



 

> [!Note]  
> Questi nomi non sono distinzione tra maiuscole e minuscole. è possibile usare qualsiasi combinazione di lettere maiuscole e minuscole.

 

In un determinato sistema possono essere disponibili classi di dispositivi e nomi di classi di dispositivi aggiuntivi. In generale, se un dispositivo non appartiene a una delle classi di dispositivi predefinite, il produttore in genere definisce una nuova classe di dispositivo e assegna un nome di classe di dispositivo univoco. Consultare la documentazione del dispositivo per determinare quali classi di dispositivi aggiuntive sono disponibili per il dispositivo. Si noti, tuttavia, che anche se la classe del dispositivo e il tipo di supporto sono correlati, non sono uguali. Un tipo di supporto descrive il formato delle informazioni sulle chiamate e una classe di dispositivo definisce l'interfaccia di programmazione usata per gestire le informazioni. Pertanto, anche se un produttore definisce un nuovo tipo di supporto, non è necessariamente vero che il produttore deve anche definire una nuova classe di dispositivo per supportare la modalità.

Anche il formato dei dati di configurazione usati con [**le funzioni lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) e [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) dipende dalla classe del dispositivo. In generale, si usa **lineGetDevConfig** per salvare una copia dei dati di configurazione del dispositivo corrente e quindi in seguito si usa **lineSetDevConfig** con i dati di configurazione salvati per ripristinare lo stato precedente della configurazione del dispositivo. Si tratta di un modo pratico per modificare temporaneamente la configurazione senza richiedere all'utente di ripristinarla manualmente allo stato precedente. Poiché il formato esatto dei dati di configurazione del dispositivo può essere diverso con ogni provider di servizi, non è consigliabile usare **lineSetDevConfig** e **lineGetDevConfig** per modificare direttamente i dati di configurazione del dispositivo. Alcuni formati vengono forniti solo per informazioni.

 

 



