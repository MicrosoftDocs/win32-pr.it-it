---
description: Progettazione per la distribuzione
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Progettazione per la distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483045"
---
# <a name="designing-for-deployment"></a>Progettazione per la distribuzione

La pianificazione dell'ambito delle applicazioni COM+ è un'attività di progettazione importante da considerare prima. I sistemi distribuiti che devono essere eseguiti utilizzando COM+ devono essere progettati per la distribuzione con la quantità minima di configurazione singola e per utilizzare in modo più efficiente ogni processo. Sono inoltre disponibili tecniche che consentono di ottenere prestazioni ottimali quando si distribuisce un'applicazione COM+. Per ulteriori informazioni, vedere [distribuzione per una comunicazione più rapida](deploying-for-faster-communication.md).

Quando viene visualizzato con lo strumento di amministrazione Servizi componenti, ogni applicazione COM+ viene visualizzata come una cartella all'interno della quale vengono raggruppati logicamente i set di componenti. Sebbene sia possibile spostare singoli componenti tra cartelle dei **componenti** dell'applicazione com+ (in altre parole, da un'applicazione a un'altra), diversi servizi impostati a livello di applicazione com+, ad esempio la sicurezza, possono variare. Queste impostazioni del servizio possono influire sulla portabilità.

## <a name="a-com-server-application-defines-a-process-boundary"></a>Un'applicazione server COM+ definisce un limite di processo

Quando si crea una nuova applicazione server COM+, si definisce realmente un nuovo limite di processo. Si noti l'eccezione per le applicazioni di libreria descritte di seguito. Questo processo diventa l'istanza dell'applicazione di controllo per i componenti contenuti nell'applicazione COM+. Tutti questi componenti vengono eseguiti in-process in una nuova istanza del programma eseguibile COM+ ogni volta che un programma chiama in un'applicazione COM+ per la prima volta. Ciò significa che tutti i componenti all'interno di una determinata cartella dei **componenti** dell'applicazione com+ vengono eseguiti in un singolo spazio di processo che funge da server DCOM. All'interno dell'applicazione COM+, COM+ gestisce la memoria, coordinando il Distributed Transaction Coordinator (DTC), l'attivazione dell'istanza del componente JIT, il rilevamento e il recupero di arresti anomali e la protezione basata sui ruoli.

## <a name="calling-across-com-application-boundaries"></a>Chiamata attraverso i limiti dell'applicazione COM+

Poiché ogni applicazione COM+ viene normalmente implementata come file eseguibile separato, l'effetto della suddivisione di un'applicazione distribuita in più applicazioni COM+ introduce chiamate COM out-of-process quando i componenti di un'applicazione COM+ chiamano i componenti in un'altra applicazione COM+. In questo modo si introduce un calo delle prestazioni a causa del carico aggiuntivo che il marshalling dei parametri COM nei processi impone.

> [!Note]  
> Non vi sono problemi intrinseci che incorrano a questa riduzione delle prestazioni. è sufficiente tenere presente che si verificherà. A seconda del tempo di risposta richiesto, del numero di utenti che richiederanno simultaneamente servizi aziendali e del carico di avvio aggiunto che ogni componente aggiunge a ogni applicazione COM+, è accettabile che l'impatto sulle prestazioni sia attribuibile alle chiamate tra applicazioni.

 

Una possibilità che elimina la riduzione delle prestazioni della chiamata attraverso i limiti dell'applicazione COM+ consiste nel contrassegnare un'applicazione COM+ specifica come applicazione di libreria. Un'applicazione libreria COM+ viene eseguita nel processo del client che la crea. Naturalmente, nessun miglioramento delle prestazioni ha un costo zero. In questo caso, il compromesso riguarda le limitazioni delle applicazioni di libreria COM+. Sebbene un'applicazione di libreria possa utilizzare la protezione basata sui ruoli, non è in grado di supportare i componenti in coda o l'accesso remoto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Distribuzione per una comunicazione più veloce](deploying-for-faster-communication.md)
</dt> <dt>

[Progettazione per la disponibilità](designing-for-availability.md)
</dt> <dt>

[Progettazione per la scalabilità](designing-for-scalability.md)
</dt> <dt>

[Progettazione per la sicurezza](designing-for-security.md)
</dt> </dl>

 

 



