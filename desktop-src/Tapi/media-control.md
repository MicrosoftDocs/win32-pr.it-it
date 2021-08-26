---
description: Il supporto di una sessione di comunicazione è il formato in cui vengono trasmessi i dati. I controlli multimediali consentono a un'applicazione di riconoscere diversi tipi di supporti e regolare gli aspetti del flusso multimediale, ad esempio il volume della trasmissione vocale.
ms.assetid: b32503fe-d494-44ea-b144-e38b8ab9b3d4
title: Controllo dei supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17e3ad30107a98cc5d1a312880fa29422c42dce2b2bc59cadfbf894cb032d74a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034531"
---
# <a name="media-control"></a>Controllo dei supporti

Il supporto di una sessione di comunicazione è il formato in cui vengono trasmessi i dati. I controlli multimediali consentono a un'applicazione di riconoscere diversi tipi di supporti e regolare gli aspetti del flusso multimediale, ad esempio il volume della trasmissione vocale.

La disponibilità di informazioni e controllo dei supporti varia notevolmente in base al tipo di applicazione TAPI, al supporto del provider di servizi e all'ambiente di comunicazione locale. Il materiale seguente fornisce una descrizione generale del controllo dei supporti. TAPI fornisce un framework flessibile per l'implementazione dei controlli, quindi le funzionalità più interessanti saranno spesso specifiche di un determinato provider di servizi.

Nella telefonia classica, un'applicazione aveva un controllo molto poco sul flusso multimediale dopo la configurazione di un percorso di comunicazione. Le applicazioni TAPI 2 hanno accesso ad alcune funzioni che consentono loro di riconoscere e reagire a cifre o toni durante una chiamata e possono usare l'API Wave per esercitare un controllo aggiuntivo sui supporti durante una sessione di comunicazione, ma in caso contrario non hanno accesso al flusso multimediale. Per una revisione di queste funzioni, vedere la panoramica di TAPI 2.2 [Media](./media-access.md) [Access](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) o la panoramica di Accesso ai supporti TSPI.

TAPI 3 introduce i provider di [servizi](about-the-media-service-provider-msp-.md)multimediali, che aumentano notevolmente le informazioni e il controllo sui supporti o su una sessione di comunicazione. Un'applicazione TAPI 3 può accedere direttamente al [flusso multimediale](stream-objects.md) di una sessione. Viene creato un flusso separato per ogni tipo di supporto coinvolto nella sessione, ad esempio voce o video. Alcuni PROVIDER possono implementare controlli substream, che possono suddividere ulteriormente i flussi, ad esempio per partecipante nel caso di IPConf MSP.



| Funzioni TAPI 2.x                                          | Descrizione                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**lineGatherDigits**](/windows/win32/api/tapi/nf-tapi-linegatherdigits)       | Avvia la raccolta di cifre memorizzate nel buffer nella chiamata specificata.                                                          |
| [**lineGenerateDigits**](/windows/win32/api/tapi/nf-tapi-linegeneratedigits)   | Avvia la generazione delle cifre specificate nella chiamata specificata come toni inband usando la modalità di segnalazione specificata. |
| [**lineGenerateTone**](/windows/win32/api/tapi/nf-tapi-linegeneratetone)       | Genera il tono inband specificato sulla chiamata specificata.                                                               |
| [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)     | Abilita e disabilita il rilevamento senza buffer delle cifre ricevute nella chiamata.                                              |
| [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia)       | Abilita e disabilita il rilevamento dei tipi di supporti nella chiamata specificata.                                                   |
| [**lineMonitorTones**](/windows/win32/api/tapi/nf-tapi-linemonitortones)       | Abilita e disabilita il rilevamento dei toni di banda nella chiamata.                                                            |
| [**lineSetMediaControl**](/windows/win32/api/tapi/nf-tapi-linesetmediacontrol) | Abilita e disabilita le azioni di controllo sul flusso multimediale associato alla riga, all'indirizzo o alla chiamata specificata.             |



 



| Interfacce o metodi TAPI 3.x                               | Descrizione                                                                                                                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) | Supporta applicazioni legacy che devono comunicare direttamente con un dispositivo.                                                                                                                             |
| [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport)           | Consente a un'applicazione di individuare se un terminale creato da un TSP legacy (pre-TAPI 3) può essere controllato usando l'API Wave.                                                                        |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                 | Consente a un'applicazione di recuperare informazioni su un flusso. per avviare, sospendere o arrestare il flusso; per selezionare o deselezionare i terminali in un flusso; e per ottenere un elenco di terminali selezionati nel flusso. |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)                   | Consente a un'applicazione di enumerare, creare o rimuovere flussi multimediali.                                                                                                                                   |



 

 

 
