---
description: Le righe di una casella combinata non vengono considerate come singoli controlli. fanno parte di una singola casella combinata che funziona come un controllo . In questa tabella sono elencati i valori per ogni casella combinata.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: Tabella ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea20677ab6ede02f76a1061d5f715eb0b8d6d87a1744d1eb89b7e0918a018e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380296"
---
# <a name="combobox-table"></a>Tabella ComboBox

Le righe di una casella combinata non vengono considerate come singoli controlli. fanno parte di una singola casella combinata che funziona come un controllo . In questa tabella sono elencati i valori per ogni casella combinata.

La tabella ComboBox include le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Proprietà | [Identificatore](identifier.md) | S   | N        |
| JSON    | [Integer](integer.md)       | S   | N        |
| Valore    | [Formattato](formatted.md)   | N   | N        |
| Testo     | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Proprietà denominata da aggiungere a questo elemento. Tutti gli elementi associati alla stessa proprietà diventano parte della stessa casella combinata.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine
</dt> <dd>

Intero positivo utilizzato per determinare l'ordinamento degli elementi visualizzati in un singolo elenco di caselle combinate. I numeri interi non devono essere consecutivi. Se una casella combinata è definita come ordinata, tutti gli elementi devono avere un valore Order. Se la casella combinata è definita come non ordinata, questa colonna viene ignorata.

Solo numeri positivi.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Stringa di valore associata a questo elemento. Se si seleziona questa riga della casella combinata, la proprietà associata (specificata in Proprietà) viene impostata su questo valore.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Testo visibile e localizzabile da assegnare all'elemento. Se questa voce o l'intera colonna non è presente, il testo viene impostato per impostazione predefinita sulla voce in Valore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il contenuto dei campi Value e Text viene formattato dalla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) al momento della creazione del controllo, pertanto può contenere qualsiasi espressione che la **funzione MsiFormatRecord** può interpretare. La formattazione si verifica solo quando il controllo viene creato e non viene aggiornato se una proprietà coinvolta nell'espressione viene modificata durante la durata del controllo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE46](ice46.md)  
</dl>

 

 



