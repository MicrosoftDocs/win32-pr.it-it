---
description: Print Schema Framework definisce uno spazio dei nomi che include gli elementi e gli attributi XML definiti nelle parole chiave dello schema di stampa.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Oggetti e nomi definiti nelle parole chiave dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408554"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>Oggetti e nomi definiti nelle parole chiave dello schema di stampa

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Print Schema Framework definisce uno spazio dei nomi che include gli elementi e gli attributi XML definiti nelle parole chiave dello schema di stampa. Sono inclusi elementi come Feature, Option e ScoredProperty. nomi di attributo, ad esempio nome e propagazione; i valori e per gli attributi XML, ad esempio constrained. In altre parole, ogni uso di un nome definito nelle parole chiave dello schema di stampa deve essere qualificato in modo esplicito con questo spazio dei nomi o deve essere associato in modo implicito a questo spazio dei nomi tramite un attributo xmlns predefinito. Il documento Parole chiave dello schema di stampa definisce le istanze dell'elemento pubblico che possono essere visualizzate in qualsiasi contesto o percorso specificato. Le istanze degli elementi devono essere visualizzate solo all'interno del contesto o della posizione designata in Print Schema Framework. Ad esempio, l'istanza di <psf:Option name= "psk:Letter"> definita nelle parole chiave dello schema di stampa deve essere presente all'interno dell'istanza di <psf:Feature name = "psk:PageMediaSize"> (definita anche nelle parole chiave dello schema di stampa). Non è possibile usare un'istanza Option specificata al di fuori del contesto specificato.

Le istanze di elemento definite privatamente possono essere visualizzate ovunque, purché il tipo di elemento venga visualizzato in un contesto consentito dal framework dello schema di stampa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



