---
description: Per inviare dati su un supporto di comunicazione quale una linea telefonica, è necessario serializzare i dati&\# 8212, ovvero convertirli in una stringa di quelli e zeri trasmessi in modo seriale sulla riga.
ms.assetid: ef8982dc-bbbc-466a-9afe-dd0425c23f1d
title: Dati codificati e decodificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b130232ac67503c6a20835c4c9b4e728b36f8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966588"
---
# <a name="encoded-and-decoded-data"></a>Dati codificati e decodificati

Per inviare dati su un supporto di comunicazione, ad esempio una linea telefonica, i dati devono essere [*serializzati*](../secgloss/s-gly.md), ovvero convertiti in una stringa di quelli e zeri trasmessi in modo seriale sulla riga. La serializzazione deve essere eseguita in modo che il computer che riceve i dati possa convertire nuovamente i dati nel formato originale. Il modo in cui la serializzazione viene eseguita viene definito [*protocollo di comunicazione*](../secgloss/c-gly.md)ed è controllato sia dal software che dall'hardware per la trasmissione dei dati. Sono disponibili diversi livelli per la conversione dei dati. Nella figura seguente viene illustrata una vista molto semplificata dei livelli del protocollo di comunicazione.

![livelli del protocollo di comunicazione](images/layer.png)

La figura precedente Mostra il livello dell'applicazione sul computer \# 1 che invia i dati da trasmettere (che in genere è costituito da una combinazione di caratteri e numeri testuali) al livello di codifica/decodifica. Il livello Encode/Decode codifica i dati in un flusso di byte del computer. Al livello più basso, il livello hardware, l'hardware converte i byte di dati in un flusso seriale di quelli e zeri trasmessi sulla riga al computer \# 2. Il livello hardware del computer \# 2 converte i valori e gli zeri in byte del computer e li passa al livello Encode/Decode per la decodifica. Il livello Encode/Decode decodifica i byte nel formato originale e passa i dati al livello dell'applicazione.

Un principio di progettazione software accettato prevede l'uso dell' *astrazione*, ovvero il processo di descrizione di un problema o di un oggetto in termini di parametri generali anziché descrivere tutti i dettagli necessari per risolvere il problema o descrivere tutti i dettagli di un oggetto. Utilizzando l'astrazione, una finestra di progettazione può specificare un oggetto software con caratteristiche specifiche senza preoccuparsi della modalità di implementazione dell'oggetto nel codice software. Questa pratica lascia aperta l'implementazione. Semplifica anche la specifica e rende possibile lo stato degli assiomi sull'oggetto che può essere dimostrato quando l'oggetto viene implementato. Questi assiomi possono quindi essere presupposti quando l'oggetto viene utilizzato in un altro oggetto di livello superiore. Astrazione è l'emblema delle specifiche software più moderne.

La maggior parte dei [*protocolli di comunicazione*](../secgloss/c-gly.md) comporta una buona quantità di astrazione. Gli oggetti a livelli superiori sono definiti in modo astratto e sono progettati per essere implementati usando oggetti a livelli inferiori. Ad esempio, un servizio a un livello potrebbe richiedere il trasferimento di determinati oggetti astratti tra computer. Un livello di livello inferiore può utilizzare le regole di codifica per trasformare gli oggetti astratti in stringhe di uno e zero.

Un metodo comune per specificare oggetti astratti destinati alla trasmissione seriale è denominato [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1). ASN. 1 è definito nella raccomandazione CCITT [*X. 208*](../secgloss/x-gly.md). Un set di regole ASN. 1 per la rappresentazione di tali oggetti come stringhe di uno e zero è denominato [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) ed è definito nella raccomandazione CCITT [*X. 509*](../secgloss/x-gly.md), sezione 8,7. Questi sono i metodi di codifica attualmente usati da CryptoAPI.

Per altre informazioni sulle funzioni Encode/Decode, vedere [funzioni di codifica e decodifica di oggetti](cryptography-functions.md).

 

 
