---
title: Checksum e conteggi degli oggetti
description: Checksum e conteggi di oggetti sono strategie di rilevamento che consentono a un'applicazione di rilevare uno stato di aggiornamento parziale.
ms.assetid: 14829a74-c186-4250-beac-036c5ecc5913
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc643ec7cd896a7c73df0be5738887a330392140
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470755"
---
# <a name="checksums-and-object-counts"></a>Checksum e conteggi degli oggetti

Checksum e conteggi di oggetti sono strategie di rilevamento che consentono a un'applicazione di rilevare uno stato di aggiornamento parziale. I checksum possono anche essere usati per rilevare le incoerenze introdotte dalla risoluzione dei conflitti. Sia i valori di checksum che i conteggi degli oggetti richiedono una posizione in cui archiviare il valore usato per verificare un checksum o un conteggio oggetti. Può trovarsi in un oggetto "Master" scelto tra quelli interessati dalla relazione specifica dell'applicazione o in un oggetto padre in cui sono archiviati gli oggetti correlati.

Per i checksum, le applicazioni che leggono gli oggetti correlati verificano il checksum calcolando un risultato locale e confrontandolo con il valore archiviato. Se i valori non corrispondono, la replica si trova in uno stato di aggiornamento parziale e gli oggetti non possono essere utilizzati.

Per i conteggi di oggetti, le applicazioni contano gli oggetti correlati, in genere figli di un singolo elemento padre, e confrontano il numero con il valore archiviato. Se i conteggi non corrispondono, la replica si trova in uno stato di aggiornamento parziale e gli oggetti non possono essere utilizzati.

Alcune considerazioni importanti:

-   Per il corretto funzionamento dell'approccio con checksum, è necessario aggiornare uno o più attributi usati nel calcolo del checksum. L'algoritmo utilizzato per calcolare il checksum deve riflettere in modo affidabile le differenze nell'input. Se molti input diversi hanno prodotto lo stesso checksum, l'algoritmo non rileva in modo affidabile gli aggiornamenti parziali. È utile anche il "salting" dell'input con valori come **objectGUID** del computer di origine e la data e l'ora dell'aggiornamento.
-   Il conteggio degli oggetti funziona meglio se usato con nuovi set di oggetti o in combinazione con GUID di coerenza (vedere la sezione successiva per altre informazioni). È necessario che l'applicazione che esegue l'aggiornamento conosca, in anticipo, il numero di oggetti che si troveranno nel contenitore quando l'aggiornamento viene completato o che usi un altro mezzo per contrassegnare il contenitore come non valido durante l'aggiornamento, ad esempio impostando il conteggio su zero. Al termine dell'aggiornamento, l'applicazione di origine contrassegna il contenitore con il numero di oggetti contenuti.

 

 




