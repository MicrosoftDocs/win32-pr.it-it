---
title: Codici in FACILITY_ITF
description: Codici in funzionalità \_ ITF
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955305"
---
# <a name="codes-in-facility_itf"></a>Codici in funzionalità \_ ITF

**HRESULT** s con funzionalità come la funzione \_ null e \_ la RPC della funzione hanno un significato universale perché sono definiti in una singola origine: Microsoft. Tuttavia, i valori di **HRESULT** nella funzionalità \_ ITF sono determinati dalla funzione o dal metodo di interfaccia da cui vengono restituiti. Ciò significa che lo stesso valore a 32 bit nella funzionalità \_ ITF restituita da due diversi metodi di interfaccia potrebbe avere significati diversi.

Il motivo per cui **HRESULT** s nella funzionalità \_ ITF può avere significati diversi in interfacce diverse è che **HRESULT** s viene mantenuto in una dimensione del tipo di dati efficiente di 32 bit. Sfortunatamente, 32 bit non è sufficiente per lo sviluppo di un sistema di allocazione di codice di errore che evita codici in conflitto allocati da programmatori diversi in momenti diversi in posizioni diverse (a differenza della gestione degli identificatori di interfaccia e dei CLSID). Di conseguenza, l' **HRESULT** a 32 bit è strutturato in modo tale che Microsoft possa definire diversi codici di errore universali, consentendo ad altri programmatori di definire nuovi codici di errore senza temere conflitti. La convenzione relativa al codice di stato è la seguente:

-   I codici di stato in strutture diverse \_ dalla funzionalità ITF possono essere definiti solo da Microsoft.
-   I codici di stato in funzionalità \_ ITF sono definiti esclusivamente dallo sviluppatore dell'interfaccia o funzione che restituisce il codice di stato. Per evitare conflitti tra i codici di errore, chi definisce l'interfaccia è responsabile del coordinamento e della pubblicazione dei \_ codici di stato ITF della struttura associati a tale interfaccia.

Tutti i codici ITF della funzionalità definita da COM \_ hanno un valore di codice compreso nell'intervallo di 0x0000-0x01ff. Sebbene sia possibile usare qualsiasi codice nella funzionalità \_ ITF, è consigliabile usare solo i valori del codice nell'intervallo di 0x0200-0xFFFF. Questa raccomandazione viene effettuata come mezzo per ridurre la confusione con eventuali errori definiti da COM.

È inoltre consigliabile che gli sviluppatori definiscano nuove funzioni e interfacce per restituire i codici di errore definiti da COM e in strutture diverse dalla funzionalità \_ ITF. In particolare, le interfacce che hanno la possibilità di essere riutilizzate in remoto con RPC in futuro dovrebbero definire i \_ codici RPC della struttura come validi. E \_ imprevisto è un codice di errore specifico che la maggior parte degli sviluppatori desidera rendere legale universalmente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> </dl>

 

 




