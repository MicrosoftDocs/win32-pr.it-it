---
title: Codici in FACILITY_ITF
description: Codici in FACILITY \_ ITF
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2a16d051c352c353376865265c0451014f6110fbcde326914c3cc244a36223
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793791"
---
# <a name="codes-in-facility_itf"></a>Codici in FACILITY \_ ITF

**I valori HRESULT** con funzionalità come FACILITY NULL e FACILITY RPC hanno un significato universale perché sono definiti in \_ \_ un'unica origine: Microsoft. Tuttavia, **i valori HRESULT** in FACILITY ITF sono determinati dalla funzione o dal metodo \_ di interfaccia da cui vengono restituiti. Ciò significa che lo stesso valore a 32 bit in FACILITY ITF restituito da due metodi di interfaccia diversi \_ potrebbe avere significati diversi.

Il motivo per cui I valori **HRESULT** in FACILITY ITF possono avere significati diversi in interfacce diverse è che gli HRESULT vengono mantenuti a una dimensione efficiente del tipo di dati di \_ 32 bit.  Sfortunatamente, i 32 bit non sono sufficientemente grandi per lo sviluppo di un sistema di allocazione di codici di errore che evita codici in conflitto allocati da programmatori diversi in momenti diversi in posizioni diverse (a differenza della gestione degli identificatori di interfaccia e dei CLSID). Di conseguenza, il valore **HRESULT** a 32 bit è strutturato in modo che Microsoft possa definire diversi codici di errore universali, consentendo allo stesso tempo ad altri programmatori di definire nuovi codici di errore senza temere conflitti. La convenzione del codice di stato è la seguente:

-   I codici di stato in strutture diverse da FACILITY \_ ITF possono essere definiti solo da Microsoft.
-   I codici di stato in FACILITY ITF sono definiti esclusivamente dallo sviluppatore dell'interfaccia o della funzione \_ che restituisce il codice di stato. Per evitare codici di errore in conflitto, chi definisce l'interfaccia è responsabile del coordinamento e della pubblicazione dei codici di stato \_ FACILITY ITF associati a tale interfaccia.

Tutti i codici ITF FACILITY definiti da COM hanno un valore di codice compreso nell'intervallo di \_ 0x0000-0x01FF. Sebbene sia consentito usare qualsiasi codice in FACILITY ITF, è consigliabile usare solo i valori del codice nell'intervallo \_ 0x0200-0xFFFF.) Questa raccomandazione viene effettuata per ridurre la confusione con eventuali errori definiti da COM.

È inoltre consigliabile che gli sviluppatori definiranno nuove funzioni e interfacce per restituire i codici di errore come definito da COM e in strutture diverse da FACILITY \_ ITF. In particolare, le interfacce che hanno la possibilità di essere remote tramite RPC in futuro devono definire i codici RPC FACILITY \_ come validi. E UNEXPECTED è un codice di errore specifico che la maggior parte degli sviluppatori vuole rendere \_ universalmente legale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> </dl>

 

 




