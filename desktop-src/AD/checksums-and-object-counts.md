---
title: Checksum e conteggi degli oggetti
description: I checksum e i conteggi degli oggetti sono strategie di rilevamento che consentono a un'applicazione di rilevare uno stato di aggiornamento parziale.
ms.assetid: 14829a74-c186-4250-beac-036c5ecc5913
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1690b30f4027f5fe2e35b85129bbcdfb6cac3356a1d053e77dcb518ff75f8fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022798"
---
# <a name="checksums-and-object-counts"></a>Checksum e conteggi degli oggetti

I checksum e i conteggi degli oggetti sono strategie di rilevamento che consentono a un'applicazione di rilevare uno stato di aggiornamento parziale. I checksum possono essere usati anche per rilevare le incoerenze introdotte dalla risoluzione delle collisioni. Sia i checksum che i conteggi degli oggetti richiedono una posizione in cui archiviare il valore usato per verificare un checksum o un conteggio di oggetti. Può trattarsi di un oggetto "master" scelto tra quelli coinvolti nella relazione specifica dell'applicazione o in un oggetto padre in cui sono archiviati gli oggetti correlati.

Per i checksum, le applicazioni che leggono gli oggetti correlati verificano il checksum calcolando un risultato locale e confrontandolo con il valore archiviato. Se i valori non corrispondono, la replica è in uno stato di aggiornamento parziale e gli oggetti non possono essere utilizzati.

Per i conteggi degli oggetti, le applicazioni contano gli oggetti correlati (in genere gli elementi figlio di un singolo elemento padre) e confrontano il conteggio con il valore archiviato. Se i conteggi non corrispondono, la replica è in uno stato di aggiornamento parziale e gli oggetti non possono essere utilizzati.

Alcune considerazioni importanti:

-   Per il corretto funzionamento dell'approccio al checksum, è necessario aggiornare uno o più attributi usati nel calcolo del checksum. L'algoritmo usato per calcolare il checksum deve riflettere in modo affidabile le differenze nell'input. Se molti input diversi hanno lo stesso checksum, l'algoritmo non rileverà in modo affidabile gli aggiornamenti parziali. È anche utile "salting" dell'input con valori come **objectGUID** del computer di origine e data e ora dell'aggiornamento.
-   I conteggi degli oggetti funzionano meglio se usati con nuovi set di oggetti o in combinazione con GUID di coerenza (per altre informazioni, vedere la sezione successiva). L'applicazione che esegue l'aggiornamento deve conoscere in anticipo il numero di oggetti che saranno presenti nel contenitore al termine dell'aggiornamento o usare altri mezzi per contrassegnare il contenitore come non valido mentre l'aggiornamento continua (ad esempio, impostando il conteggio su zero). Dopo aver completato l'aggiornamento, l'applicazione di origine contrassegna il contenitore con il numero di oggetti contenuti.

 

 




