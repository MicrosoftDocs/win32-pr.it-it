---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Parole chiave Public PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320859"
---
# <a name="printcapabilities-public-keywords"></a>Parole chiave Public PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Nella sezione seguente vengono specificati gli elementi configurabili dall'utente e le definizioni dei parametri che potrebbero essere applicabili a un documento PrintCapabilities.

## <a name="user-configurable-elements-usage"></a>Utilizzo degli elementi configurabili dall'utente

Gli elementi configurabili dall'utente rappresentano parole chiave pubbliche dello schema di stampa che possono essere visualizzate in un documento PrintCapabilities o in un oggetto PrintTicket. Sono progettate per rappresentare gli attributi di dispositivo configurabili supportati da un dispositivo specifico o comunicano l'intento dell'impostazione di stampa da un'applicazione o un utente.

Gli elementi configurabili dall'utente possono fare riferimento a elementi di riferimento al parametro. Per altre informazioni, vedere la sezione [elementi di riferimento del parametro](parameter-reference-elements.md) .

## <a name="parameter-definitions-usage"></a>Utilizzo delle definizioni dei parametri

Le definizioni dei parametri hanno il formato di tipi di elemento ParameterDef in un documento sulle funzionalità di stampa. I tipi di elemento ParameterDef vengono inizializzati in un oggetto PrintTicket usando il tipo di elemento ParameterInit. Il valore del parametro verrà specificato utilizzando l'elemento ParameterInit. Una parola chiave configurabile dall'utente può fare riferimento a una definizione di parametro usando il tipo di elemento ParameterRef. Per altre informazioni, vedere la sezione [costrutti di parametri](parameter-constructs.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



