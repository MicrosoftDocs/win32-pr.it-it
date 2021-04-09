---
description: Le righe di una casella di riepilogo non vengono considerate come singoli controlli, ma fanno parte di una casella di riepilogo che funge da controllo. La tabella ListBox definisce i valori per tutte le caselle di riepilogo.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: Tabella ListBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967788"
---
# <a name="listbox-table"></a>Tabella ListBox

Le righe di una casella di riepilogo non vengono considerate come singoli controlli, ma fanno parte di una casella di riepilogo che funge da controllo. La tabella ListBox definisce i valori per tutte le caselle di riepilogo.

La tabella ListBox contiene le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Proprietà | [Identificatore](identifier.md) | S   | N        |
| JSON    | [Integer](integer.md)       | S   | N        |
| Valore    | [Formattato](formatted.md)   | N   | N        |
| Testo     | [Formattato](formatted.md)   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Proprietà denominata da associare a questo elemento. Tutti gli elementi collegati alla stessa proprietà diventano parte della stessa casella di riepilogo.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine
</dt> <dd>

Intero positivo utilizzato per determinare l'ordinamento degli elementi visualizzati in una singola casella di riepilogo. Se la casella di riepilogo è definita come ordinata, tutti gli elementi devono avere un valore di ordine. I numeri interi non devono essere consecutivi. Se la casella di riepilogo è definita come non ordinata, la colonna viene ignorata.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Stringa del valore associata a questo elemento. Selezionando la riga, la proprietà associata verrà impostata su questo valore.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Testo visibile e localizzabile da assegnare all'elemento. Se questa voce o l'intera colonna risulta mancante, per impostazione predefinita il testo viene impostato sulla voce corrispondente in value.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il contenuto del valore e i campi di testo vengono formattati dalla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando viene creato il controllo, pertanto possono contenere qualsiasi espressione che la funzione **MsiFormatRecord** possa interpretare. La formattazione si verifica solo quando viene creato il controllo e non viene aggiornata se una proprietà richiesta nell'espressione viene modificata durante il ciclo di vita del controllo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE46](ice46.md)  
</dl>

 

 



