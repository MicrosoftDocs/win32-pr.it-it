---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Oggetti e nomi definiti nelle parole chiave dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2347c73dd647f90a88821658cdcf9e2ed846e83
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234557"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>Oggetti e nomi definiti nelle parole chiave dello schema di stampa

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il Framework dello schema di stampa definisce uno spazio dei nomi che include gli elementi e gli attributi XML definiti nelle parole chiave Print Schema. Sono inclusi elementi quali feature, Option e ScoredProperty; nomi di attributi, ad esempio nome e propagazione; valori e per gli attributi XML, ad esempio vincolato. In altre parole, ogni utilizzo di un nome definito nelle parole chiave dello schema di stampa deve essere qualificato in modo esplicito con questo spazio dei nomi oppure deve essere associato in modo implicito a questo spazio dei nomi tramite l'utilizzo di un attributo xmlns predefinito. Il documento parole chiave dello schema di stampa definisce le istanze di elementi pubblici che possono essere visualizzate in un contesto o in un percorso specifico. Le istanze degli elementi devono essere visualizzate solo nel contesto o nel percorso designato nel Framework dello schema di stampa. Ad esempio, l'<PSF: Option Name = "PSK: Letter" > istanza definita nelle parole chiave Print Schema deve essere visualizzata all'interno dell'istanza di <PSF: feature name = "PSK: PageMediaSize" > (definita anche nelle parole chiave Print Schema). Non si ha la libertà di usare un'istanza di opzione specificata al di fuori del contesto specificato.

Le istanze degli elementi definite privatamente possono essere visualizzate in qualsiasi punto, purché il tipo di elemento venga visualizzato in un contesto consentito dal Framework dello schema di stampa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



