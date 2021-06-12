---
description: Informazioni sulle classi di dispositivo TSPI. Una classe di dispositivo è un gruppo di dispositivi o driver di dispositivo tramite cui le applicazioni inviano e ricevono dati o informazioni sulle chiamate.
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: Classi di dispositivo TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6775e73df3914339edbdf791659de821855864dd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011344"
---
# <a name="tspi-device-classes"></a>Classi di dispositivo TSPI

Una *classe di dispositivo* è un gruppo di dispositivi fisici correlati o driver di dispositivo tramite i quali le applicazioni inviano e ricevono le informazioni o i dati che costituisce una chiamata. Ogni classe di  dispositivo ha un nome di classe di dispositivo che identifica in modo univoco la classe e fornisce informazioni sull'interfaccia di programmazione e sui comandi che possono essere usati per aprire e comunicare con i dispositivi nella classe .

TapI (Telephony Application Programming Interface) associa i dispositivi di una o più classi di dispositivi a ogni linea o dispositivo telefonico. È possibile accedere a uno di questi dispositivi recuperando l'identificatore del dispositivo usando la [**funzione lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid) [**o phoneGetID.**](/windows/win32/api/tapi/nf-tapi-phonegetid) Si specifica il nome della classe del dispositivo e la funzione restituisce il nome della porta, il nome del dispositivo, l'handle del dispositivo o l'identificatore di dispositivo specifico che è necessario aprire e accedere al dispositivo. Il formato delle informazioni restituite dipende dalla classe del dispositivo ed è descritto in questa sezione.

È anche possibile usare i nomi delle classi di dispositivo [**con le funzioni lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) e [**phoneConfigDialog**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) per consentire all'utente di impostare le opzioni di configurazione per il dispositivo specificato. con le [**funzioni lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon) e [**phoneGetIcon**](/windows/win32/api/tapi/nf-tapi-phonegeticon) per recuperare un'icona per rappresentare il dispositivo specificato; e con le [**funzioni lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) per recuperare e impostare direttamente le opzioni di configurazione per il dispositivo specificato.

Di seguito sono riportati i nomi predefiniti delle classi di dispositivo.



| Nome della classe del dispositivo                                       | Descrizione                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [Comm](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | Porta di comunicazione                              |
| [comm/datamodem](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | Modem tramite una porta di comunicazione              |
| [comm/datamodem/portname](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | Nome del dispositivo a cui è connesso un modem |
| [wave/in](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Dispositivo audio Wave (solo input)                   |
| [wave/out](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Dispositivo audio Wave (solo output)                  |
| [wave/in/out](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Dispositivo audio Wave, full duplex                   |
| [midi/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | Sequencer MIDI (solo input)                      |
| [midi/out](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | Sequencer MIDI (solo output)                     |
| [tapi/line](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | Dispositivo line                                      |
| [tapi/phone](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | Dispositivo telefonico                                     |
| [Ndis](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | Dispositivo di rete                                   |
| [tapi/terminale](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | Dispositivo terminale                                  |



 

Questi nomi non usano la distinzione tra maiuscole e minuscole, quindi è possibile usare qualsiasi combinazione di lettere maiuscole e minuscole.

In un determinato sistema possono essere disponibili classi di dispositivi e nomi di classi di dispositivi aggiuntivi. In generale, se un dispositivo non appartiene a una delle classi di dispositivi predefinite, il produttore in genere definisce una nuova classe di dispositivo e assegna un nome di classe di dispositivo univoco. È necessario consultare la documentazione del dispositivo per determinare quali classi di dispositivi aggiuntive sono disponibili per il dispositivo. Si noti, tuttavia, che anche se la classe del dispositivo e il tipo di supporto sono correlati, non sono uguali. Un *tipo di* supporto descrive un formato di informazioni in una chiamata e una classe *di* dispositivo definisce l'interfaccia di programmazione usata per gestire le informazioni. Pertanto, anche se un produttore definisce un nuovo tipo di supporto, potrebbe non essere vero che il produttore deve anche definire una nuova classe di dispositivo per supportare la modalità.

Anche il formato dei dati di configurazione usati con [**le funzioni lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) e [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) dipende dalla classe del dispositivo. In generale, si usa **lineGetDevConfig** per salvare una copia dei dati di configurazione del dispositivo corrente e quindi in seguito si usa **lineSetDevConfig** con i dati di configurazione salvati per ripristinare lo stato precedente della configurazione del dispositivo. Si tratta di un modo pratico per modificare temporaneamente la configurazione senza richiedere all'utente di ripristinarla manualmente allo stato precedente. Poiché il formato esatto dei dati di configurazione del dispositivo può essere diverso con ogni provider di servizi, non usare **lineSetDevConfig** e **lineGetDevConfig** per modificare direttamente i dati di configurazione del dispositivo. Alcuni formati vengono forniti solo per le informazioni.

 

 
