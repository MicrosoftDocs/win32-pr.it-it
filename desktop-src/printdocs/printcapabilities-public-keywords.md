---
description: Informazioni sugli elementi configurabili dall'utente e sulle definizioni dei parametri che possono essere applicabili a un documento PrintCapabilities.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Parole chiave pubbliche PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cccfa2cb22d8e784e8d4b82e548b9f4ae9772d1bd216573f5229d00f2f6d633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600621"
---
# <a name="printcapabilities-public-keywords"></a>Parole chiave pubbliche PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La sezione seguente specifica sia gli elementi configurabili dall'utente che le definizioni di parametro che possono essere applicabili a un documento PrintCapabilities.

## <a name="user-configurable-elements-usage"></a>Utilizzo degli elementi configurabili dall'utente

Gli elementi configurabili dall'utente rappresentano parole chiave pubbliche dello schema di stampa che possono essere visualizzate in un documento PrintCapabilities o in un PrintTicket. Sono destinati a rappresentare gli attributi del dispositivo configurabili supportati da un dispositivo specifico o a comunicare la finalità dell'impostazione di stampa da un'applicazione o un utente.

Gli elementi configurabili dall'utente possono fare riferimento a elementi di riferimento ai parametri. Per altre informazioni, vedere la sezione [Elementi di riferimento ai](parameter-reference-elements.md) parametri.

## <a name="parameter-definitions-usage"></a>Utilizzo delle definizioni dei parametri

Le definizioni dei parametri hanno la forma di tipi di elemento ParameterDef in un documento di funzionalità di stampa. I tipi di elemento ParameterDef vengono inizializzati in printTicket usando il tipo di elemento ParameterInit. Il valore del parametro verrà specificato usando l'elemento ParameterInit. Una parola chiave configurabile dall'utente può fare riferimento a una definizione di parametro usando il tipo di elemento ParameterRef. Per altre informazioni, vedere la [sezione Costrutti di](parameter-constructs.md) parametro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



