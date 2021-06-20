---
description: Informazioni sugli elementi configurabili dall'utente e sulle definizioni dei parametri che possono essere applicabili a un documento PrintCapabilities.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Parole chiave pubbliche di PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d836ca13297f031897598bb2ecbfc6588c49753
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407094"
---
# <a name="printcapabilities-public-keywords"></a>Parole chiave pubbliche di PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La sezione seguente specifica sia gli elementi configurabili dall'utente che le definizioni dei parametri che possono essere applicabili a un documento PrintCapabilities.

## <a name="user-configurable-elements-usage"></a>Utilizzo degli elementi configurabili dall'utente

Gli elementi configurabili dall'utente rappresentano parole chiave pubbliche dello schema di stampa che possono essere visualizzate in un documento PrintCapabilities o printTicket. Sono destinati a rappresentare gli attributi del dispositivo configurabili supportati da un dispositivo specifico o a comunicare la finalità dell'impostazione di stampa da parte di un'applicazione o di un utente.

Gli elementi configurabili dall'utente possono fare riferimento a elementi di riferimento dei parametri. Per altre informazioni, vedere la sezione [Elementi di riferimento dei](parameter-reference-elements.md) parametri.

## <a name="parameter-definitions-usage"></a>Utilizzo delle definizioni dei parametri

Le definizioni dei parametri hanno la forma di tipi di elemento ParameterDef in un documento Di funzionalità di stampa. I tipi di elemento ParameterDef vengono inizializzati in un printticket usando il tipo di elemento ParameterInit. Il valore del parametro verrà specificato usando l'elemento ParameterInit. Una parola chiave configurabile dall'utente può fare riferimento a una definizione di parametro usando il tipo di elemento ParameterRef. Per altre informazioni, vedere la [sezione Costrutti di](parameter-constructs.md) parametri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



