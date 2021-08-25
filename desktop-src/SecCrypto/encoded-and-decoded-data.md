---
description: Per inviare dati tramite un supporto di comunicazione, ad esempio una linea telefonica, i dati devono essere serializzati&8212, che viene convertito in una stringa di uno e zeri trasmessi in serie sulla \# linea.
ms.assetid: ef8982dc-bbbc-466a-9afe-dd0425c23f1d
title: Dati codificati e decodificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063f18a4f58f2989e2bd0b890fd11a7ab6022a3de255385b1cf529afb5493485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874947"
---
# <a name="encoded-and-decoded-data"></a>Dati codificati e decodificati

Per inviare dati tramite un supporto di comunicazione, [](../secgloss/s-gly.md)ad esempio una linea telefonica, i dati devono essere serializzati, ovvero convertiti in una stringa di uno e zero trasmessi in modo seriale sulla linea. La serializzazione deve essere eseguita in modo che il computer che riceve i dati possa riconvertire i dati nel formato originale. Il modo in cui viene eseguita la serializzazione è detto protocollo [*di*](../secgloss/c-gly.md)comunicazione ed è controllato sia dal software che dall'hardware di trasmissione dei dati. I dati vengono convertiti in diversi livelli. La figura seguente mostra una visualizzazione notevolmente semplificata dei livelli del protocollo di comunicazione.

![livelli del protocollo di comunicazione](images/layer.png)

La figura precedente mostra il livello dell'applicazione nel Computer 1 che invia i dati da trasmettere (che in genere è costituito da una combinazione di caratteri testuali e numeri) al livello di \# codifica/decodifica. Il livello di codifica/decodifica codifica i dati in un flusso di byte del computer. Al livello più basso, il livello hardware, l'hardware converte i byte di dati in un flusso seriale di uno e zeri trasmessi sulla riga al Computer \# 2. Il livello hardware del Computer 2 converte di nuovo i valori uno e zero in byte del computer e li passa al livello di \# codifica/decodifica per la decodifica. Il livello di codifica/decodifica decodifica i byte nel formato originale e passa i dati al livello dell'applicazione.

Un principio di progettazione software accettato è l'uso dell'astrazione, cio' il processo di descrizione di un problema o di un oggetto in termini di parametri generali, anziché descrivere tutti i dettagli necessari per risolvere il problema o descrivere tutti i dettagli di un oggetto. Usando l'astrazione, un progettista può specificare un oggetto software con qualità specifiche senza doversi preoccupare della modalità di implementazione dell'oggetto nel codice software. Tale procedura lascia aperta l'implementazione. Semplifica inoltre la specifica e consente di specificare assiomi sull'oggetto che possono essere dimostrati quando l'oggetto viene implementato. Questi assiomi possono quindi essere presupposti quando l'oggetto viene utilizzato in un altro oggetto di livello superiore. L'astrazione è il segno distintivo della maggior parte delle specifiche software contemporanee.

La [*maggior parte dei protocolli*](../secgloss/c-gly.md) di comunicazione implica una buona quantità di astrazione. Gli oggetti ai livelli superiori sono definiti in modo astratto e devono essere implementati usando oggetti a livelli inferiori. Ad esempio, un servizio a un livello potrebbe richiedere il trasferimento di determinati oggetti astratti tra computer. Un livello inferiore può usare regole di codifica per trasformare gli oggetti astratti in stringhe di uno e zero.

Un metodo comune per specificare oggetti astratti destinati alla trasmissione seriale è denominato [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN.1). ASN.1 è definito nella raccomandazione CCITT [*X.208.*](../secgloss/x-gly.md) Un set di regole ASN.1 per rappresentare tali oggetti come stringhe di uno e zero è denominato [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) ed è definito nella raccomandazione CCITT [*X.509*](../secgloss/x-gly.md), sezione 8.7. Questi sono i metodi di codifica attualmente usati da CryptoAPI.

Per altre informazioni sulle funzioni di codifica/decodifica, vedere [Funzioni di codifica e decodifica di oggetti.](cryptography-functions.md)

 

 
