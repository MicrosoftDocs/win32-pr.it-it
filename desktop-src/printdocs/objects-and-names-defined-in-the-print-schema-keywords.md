---
description: Print Schema Framework definisce uno spazio dei nomi che include gli elementi e gli attributi XML definiti nelle parole chiave dello schema di stampa.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Oggetti e nomi definiti nelle parole chiave dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be119d7931210bbc0aea82a4a59534b135ef8655e3aad1ef2c2afaf275d31833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718981"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>Oggetti e nomi definiti nelle parole chiave dello schema di stampa

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Print Schema Framework definisce uno spazio dei nomi che include gli elementi e gli attributi XML definiti nelle parole chiave dello schema di stampa. Sono inclusi elementi come Feature, Option e ScoredProperty. nomi di attributi, ad esempio nome e propagazione; e per gli attributi XML, ad esempio vincolati. In altre parole, ogni uso di un nome definito nelle parole chiave dello schema di stampa deve essere qualificato in modo esplicito con questo spazio dei nomi o deve essere associato in modo implicito a questo spazio dei nomi tramite un attributo xmlns predefinito. Il documento Parole chiave dello schema di stampa definisce le istanze di elementi pubblici che possono essere visualizzate in un contesto o in una posizione specifica. Le istanze dell'elemento devono essere visualizzate solo all'interno del contesto o della posizione designata in Print Schema Framework. Ad esempio, l'istanza <psf:Option name= "psk:Letter"> definita nelle parole chiave dello schema di stampa deve essere visualizzata all'interno dell'istanza di <psf:Feature name = "psk:PageMediaSize"> (definita anche nelle parole chiave dello schema di stampa). Non è possibile usare una determinata istanza option al di fuori del contesto specificato.

Le istanze di elemento definite privatamente possono essere visualizzate ovunque, purché il tipo di elemento venga visualizzato in un contesto consentito da Print Schema Framework.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



