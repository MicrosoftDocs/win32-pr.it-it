---
description: Una classe dispositivo è un gruppo di dispositivi fisici o driver di dispositivo correlati attraverso i quali le applicazioni inviano e ricevono le informazioni o i dati che costituiscono una chiamata.
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: Classi di dispositivi TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10392487657e8190052546605c54bed8cc0ccf4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349651"
---
# <a name="tspi-device-classes"></a>Classi di dispositivi TSPI

Una *classe dispositivo* è un gruppo di dispositivi fisici o driver di dispositivo correlati attraverso i quali le applicazioni inviano e ricevono le informazioni o i dati che costituiscono una chiamata. Ogni classe Device ha un *nome di classe del dispositivo* che identifica in modo univoco la classe e fornisce informazioni sull'interfaccia di programmazione e i comandi che possono essere usati per aprire e comunicare con i dispositivi nella classe.

L'interfaccia TAPI (Telephony Application Programming Interface) associa i dispositivi di una o più classi di dispositivi a ogni riga o dispositivo telefonico. Per accedere a uno di questi dispositivi, è possibile recuperare l'identificatore del dispositivo usando la funzione [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid) o [**phoneGetID**](/windows/win32/api/tapi/nf-tapi-phonegetid) . Specificare il nome della classe del dispositivo e la funzione restituisce il nome della porta, il nome del dispositivo, l'handle del dispositivo o l'identificatore del dispositivo specifici che è necessario aprire e accedere al dispositivo. Il formato delle informazioni restituite dipende dalla classe device ed è descritto in questa sezione.

Per consentire all'utente di impostare le opzioni di configurazione per il dispositivo specificato, è anche possibile usare nomi di classi di dispositivi con le funzioni [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) e [**phoneConfigDialog**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) . con le funzioni [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon) e [**phoneGetIcon**](/windows/win32/api/tapi/nf-tapi-phonegeticon) per recuperare un'icona per rappresentare il dispositivo specificato; e con le funzioni [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) per recuperare e impostare direttamente le opzioni di configurazione per il dispositivo specificato.

Di seguito sono riportati i nomi delle classi di dispositivo predefinite.



| Nome classe dispositivo                                       | Descrizione                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [comunicazione](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | Porta di comunicazione                              |
| [comunicazione/datamode](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | Modem tramite una porta di comunicazione              |
| [comm/DataModel/PortName](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | Nome del dispositivo a cui è connesso un modem |
| [Wave/in](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Dispositivo audio Wave (solo input)                   |
| [Wave/out](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Dispositivo audio Wave (solo output)                  |
| [Wave/in/out](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Dispositivo audio Wave, full duplex                   |
| [MIDI/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | MIDI sequencer (solo input)                      |
| [MIDI/out](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | MIDI sequencer (solo output)                     |
| [TAPI/linea](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | Dispositivo linea                                      |
| [TAPI/Phone](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | Dispositivo telefonico                                     |
| [NDIS](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | Dispositivo di rete                                   |
| [TAPI/terminale](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | Dispositivo Terminal                                  |



 

Questi nomi non fanno distinzione tra maiuscole e minuscole, pertanto è possibile utilizzare qualsiasi combinazione di lettere maiuscole e minuscole.

È possibile che in un sistema specifico siano disponibili classi di dispositivi e nomi di classi di dispositivi aggiuntivi. In generale, se un dispositivo non appartiene a una delle classi di dispositivo predefinite, il produttore definisce in genere una nuova classe di dispositivi e assegna un nome di classe del dispositivo univoco. È necessario controllare la documentazione del dispositivo per determinare le altre classi di dispositivi disponibili. Si noti, tuttavia, che anche se la classe del dispositivo e il tipo di supporto sono correlati, non sono uguali. Un *tipo di supporto* descrive un formato di informazioni su una chiamata e una *classe di dispositivi* definisce l'interfaccia di programmazione utilizzata per gestire tali informazioni. Quindi, anche se un produttore definisce un nuovo tipo di supporto, potrebbe non essere vero che il produttore debba anche definire una nuova classe di dispositivi per supportare la modalità.

Il formato dei dati di configurazione usati con le funzioni [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) e [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) dipende anche dalla classe Device. In generale, si usa **lineGetDevConfig** per salvare una copia dei dati di configurazione del dispositivo corrente e successivamente usare **lineSetDevConfig** con i dati di configurazione salvati per ripristinare lo stato precedente della configurazione del dispositivo. Si tratta di un modo pratico per modificare temporaneamente la configurazione senza richiedere all'utente di ripristinare manualmente lo stato precedente. Poiché il formato esatto dei dati di configurazione del dispositivo può essere diverso con ogni provider di servizi, non usare **lineSetDevConfig** e **lineGetDevConfig** per modificare direttamente i dati di configurazione del dispositivo. Per informazioni sono disponibili alcuni formati.

 

 
