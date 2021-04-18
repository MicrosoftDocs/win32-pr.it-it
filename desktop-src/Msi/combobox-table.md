---
description: Le righe di una casella combinata non vengono considerate come singoli controlli; fanno parte di una singola casella combinata che funge da controllo. Questa tabella elenca i valori per ogni casella combinata.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: Tabella ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e209ac8a7c27c36fd5c1bbd3c97822617c48f5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315482"
---
# <a name="combobox-table"></a>Tabella ComboBox

Le righe di una casella combinata non vengono considerate come singoli controlli; fanno parte di una singola casella combinata che funge da controllo. Questa tabella elenca i valori per ogni casella combinata.

La tabella ComboBox contiene le colonne seguenti.



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

Proprietà denominata da associare a questo elemento. Tutti gli elementi collegati alla stessa proprietà diventano parte della stessa casella combinata.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine
</dt> <dd>

Intero positivo utilizzato per determinare l'ordinamento degli elementi visualizzati in un unico elenco di caselle combinate. I numeri interi non devono essere consecutivi. Se una casella combinata è definita come ordinata, tutti gli elementi devono avere un valore di ordine. Se la casella combinata è definita come non ordinata, la colonna viene ignorata.

Solo numeri positivi.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Stringa del valore associata a questo elemento. Se si seleziona questa riga della casella combinata, il valore della proprietà associata (specificata nella proprietà) verrà impostato su questo valore.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Testo visibile e localizzabile da assegnare all'elemento. Se questa voce o l'intera colonna risulta mancante, per impostazione predefinita il testo viene impostato sulla voce in value.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il contenuto del valore e i campi di testo vengono formattati dalla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando viene creato il controllo, pertanto possono contenere qualsiasi espressione che la funzione **MsiFormatRecord** possa interpretare. La formattazione si verifica solo quando il controllo viene creato e non viene aggiornato se una proprietà richiesta nell'espressione viene modificata durante il ciclo di vita del controllo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE46](ice46.md)  
</dl>

 

 



