---
description: Il supporto di una sessione di comunicazione è il formato in cui vengono trasmessi i dati. I controlli multimediali consentono a un'applicazione di riconoscere diversi tipi di supporti e di regolare gli aspetti del flusso multimediale, ad esempio il volume della trasmissione vocale.
ms.assetid: b32503fe-d494-44ea-b144-e38b8ab9b3d4
title: Controllo multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dad56e3feef8493a70cf93152b225be2777848
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320659"
---
# <a name="media-control"></a>Controllo multimediale

Il supporto di una sessione di comunicazione è il formato in cui vengono trasmessi i dati. I controlli multimediali consentono a un'applicazione di riconoscere diversi tipi di supporti e di regolare gli aspetti del flusso multimediale, ad esempio il volume della trasmissione vocale.

La disponibilità di controllo e informazioni del supporto varia notevolmente in base al tipo di applicazione TAPI, al supporto del provider di servizi e all'ambiente di comunicazione locale. Il materiale seguente fornisce una descrizione generale del controllo multimediale. TAPI fornisce un framework flessibile per l'implementazione dei controlli, pertanto le funzionalità più interessanti saranno spesso specifiche di un determinato provider di servizi.

Con la telefonia classica, un'applicazione ha un controllo molto ridotto sul flusso multimediale dopo che è stato configurato un percorso di comunicazione. Le applicazioni TAPI 2 hanno accesso ad alcune funzioni che consentono loro di riconoscere e reagire a cifre o toni durante una chiamata e possono essere in grado di usare l'API Wave per esercitare un controllo aggiuntivo sui supporti durante una sessione di comunicazione, ma in caso contrario non hanno accesso al flusso multimediale. Per una revisione di queste funzioni, vedere Panoramica di [accesso multimediale](./media-access.md) di TAPI 2,2 o Panoramica di TSPI [Media Access](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) .

TAPI 3 introduce i [provider di servizi multimediali](about-the-media-service-provider-msp-.md), che aumentano in modo eccessivo sia le informazioni che il controllo sui supporti o una sessione di comunicazione. Un'applicazione TAPI 3 può accedere direttamente al [flusso](stream-objects.md) multimediale di una sessione. Viene creato un flusso separato per ogni tipo di supporto della sessione, ad esempio voce o video. Alcuni MSPs possono implementare i controlli substream, che possono dividere ulteriormente i flussi, ad esempio dal partecipante nel caso di IPConf MSP.



| Funzioni di TAPI 2. x                                          | Descrizione                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**lineGatherDigits**](/windows/win32/api/tapi/nf-tapi-linegatherdigits)       | Avvia la raccolta memorizzata nel buffer di cifre nella chiamata specificata.                                                          |
| [**lineGenerateDigits**](/windows/win32/api/tapi/nf-tapi-linegeneratedigits)   | Avvia la generazione delle cifre specificate nella chiamata specificata come toni inband usando la modalità di segnalazione specificata. |
| [**lineGenerateTone**](/windows/win32/api/tapi/nf-tapi-linegeneratetone)       | Genera il tono di inbando specificato sulla chiamata specificata.                                                               |
| [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)     | Abilita e Disabilita il rilevamento non memorizzato nel buffer delle cifre ricevute nella chiamata.                                              |
| [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia)       | Abilita e Disabilita il rilevamento dei tipi di supporto sulla chiamata specificata.                                                   |
| [**lineMonitorTones**](/windows/win32/api/tapi/nf-tapi-linemonitortones)       | Abilita e Disabilita il rilevamento dei toni inband sulla chiamata.                                                            |
| [**lineSetMediaControl**](/windows/win32/api/tapi/nf-tapi-linesetmediacontrol) | Abilita e Disabilita le azioni di controllo sul flusso multimediale associato alla riga, all'indirizzo o alla chiamata specificata.             |



 



| Interfacce o metodi di TAPI 3. x                               | Descrizione                                                                                                                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) | Supporta le applicazioni legacy che devono comunicare direttamente con un dispositivo.                                                                                                                             |
| [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport)           | Consente a un'applicazione di individuare se un terminale creato da un TSP legacy (pre-TAPI 3) può essere controllato usando l'API Wave.                                                                        |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                 | Consente a un'applicazione di recuperare informazioni su un flusso. per avviare, sospendere o arrestare il flusso; per selezionare o deselezionare i terminali in un flusso; e per ottenere un elenco dei terminali selezionati nel flusso. |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)                   | Consente a un'applicazione di enumerare, creare o rimuovere flussi multimediali.                                                                                                                                   |



 

 

 
