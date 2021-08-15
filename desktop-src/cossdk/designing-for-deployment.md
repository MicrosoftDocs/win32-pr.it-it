---
description: Progettazione per la distribuzione
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Progettazione per la distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a755132f1be35ecb6913b7690bce11e342fceb957e63607ee4e9b579bcc758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307303"
---
# <a name="designing-for-deployment"></a>Progettazione per la distribuzione

La pianificazione dell'ambito delle applicazioni COM+ è un'attività di progettazione importante da prendere in considerazione nelle prime fasi. I sistemi distribuiti destinati all'esecuzione con COM+ devono essere progettati per la distribuzione con la minima quantità di configurazione singola e per usare in modo più efficiente ogni processo. Esistono anche tecniche che consentono di ottenere prestazioni ottimali durante la distribuzione di un'applicazione COM+. Per altre informazioni, vedere [Distribuzione per una comunicazione più veloce.](deploying-for-faster-communication.md)

Quando viene visualizzata con lo strumento di amministrazione Servizi componenti, ogni applicazione COM+ viene visualizzata come una cartella all'interno della quale i set di componenti vengono raggruppati logicamente. Anche se è possibile spostare  singoli componenti tra le cartelle Componenti dell'applicazione COM+, ovvero da un'applicazione a un'altra, diversi servizi impostati a livello di applicazione COM+, ad esempio la sicurezza, possono essere diversi. Queste impostazioni del servizio possono influire sulla portabilità.

## <a name="a-com-server-application-defines-a-process-boundary"></a>Un'applicazione server COM+ definisce un limite di processo

Quando si crea una nuova applicazione server COM+, si definisce effettivamente un nuovo limite di processo. Si noti l'eccezione per le applicazioni di libreria illustrate di seguito. Questo processo diventa l'istanza dell'applicazione di controllo per i componenti contenuti nell'applicazione COM+. Tutti questi componenti vengono eseguiti in-process in una nuova istanza del programma eseguibile COM+ ogni volta che un programma chiama un'applicazione COM+ per la prima volta. Ciò significa che tutti i componenti all'interno della cartella **Components** di una determinata applicazione COM+ vengono eseguiti in un unico spazio di elaborazione che funge da server DCOM. All'interno dell'applicazione COM+, COM+ gestisce la memoria, il coordinamento con Distributed Transaction Coordinator (DTC), l'attivazione just-in-time dell'istanza del componente, il rilevamento e il ripristino degli arresti anomali e la sicurezza basata sui ruoli.

## <a name="calling-across-com-application-boundaries"></a>Chiamata attraverso i limiti dell'applicazione COM+

Poiché in genere ogni applicazione COM+ viene implementata come eseguibile separato, l'effetto della suddivisione di un'applicazione distribuita tra più applicazioni COM+ introduce chiamate COM out-of-process quando i componenti in un'applicazione COM+ chiamano i componenti in un'altra applicazione COM+. Ciò introduce una riduzione delle prestazioni a causa del carico aggiuntivo imposto dal marshalling dei parametri COM tra processi.

> [!Note]  
> Non c'è nulla di intrinsecamente errato nell'incorrere in questa penalità delle prestazioni. È sufficiente tenere presente che si verificherà. A seconda del tempo di risposta richiesto, del numero di utenti che richiederanno contemporaneamente servizi aziendali e dell'ulteriore carico di avvio che ogni componente aggiunge a ogni applicazione COM+, è possibile che il livello di prestazioni attribuibile alle chiamate tra applicazioni sia accettabile.

 

Una possibilità che elimina la penalità delle prestazioni delle chiamate oltre i limiti dell'applicazione COM+ è contrassegnare una determinata applicazione COM+ come applicazione di libreria. Un'applicazione della libreria COM+ viene eseguita nel processo del client che la crea. Naturalmente, nessun miglioramento delle prestazioni ha un costo zero. In questo caso, il compromesso implica le limitazioni delle applicazioni della libreria COM+. Sebbene un'applicazione di libreria possa usare la sicurezza basata sui ruoli, non può supportare i componenti in coda o l'accesso remoto.

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

 

 



