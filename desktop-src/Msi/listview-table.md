---
description: Le righe di una visualizzazione elenco non vengono considerate come singoli controlli, ma fanno parte di una visualizzazione elenco che funziona come un controllo . La tabella ListView definisce i valori per tutte le visualizzazioni elenco.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: Tabella ListView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a84ebab6c90486283c3dd8d4731cc0b7f3aff11a5459a0e93496bab83d7c277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013079"
---
# <a name="listview-table"></a>Tabella ListView

Le righe di una visualizzazione elenco non vengono considerate come singoli controlli, ma fanno parte di una visualizzazione elenco che funziona come un controllo . La tabella ListView definisce i valori per tutte le visualizzazioni elenco.

La tabella ListView include le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Proprietà | [Identificatore](identifier.md) | S   | N        |
| JSON    | [Integer](integer.md)       | S   | N        |
| Valore    | [Formattato](formatted.md)   | N   | N        |
| Testo     | [Formattato](formatted.md)   | N   | S        |
| Binario\_ | [Identificatore](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Proprietà denominata da aggiungere a questo elemento. Tutti gli elementi associati alla stessa proprietà diventano parte della stessa visualizzazione elenco.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine
</dt> <dd>

Numero intero positivo usato per determinare l'ordinamento degli elementi visualizzati in un singolo elenco listview. Non è necessario che i numeri interi siano consecutivi. Se una visualizzazione elenco è definita come ordinata, tutti gli elementi devono avere un valore Ordinamento. Se la visualizzazione elenco è definita come non ordinata, questa colonna viene ignorata.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Stringa del valore associata a questo elemento. Se si seleziona la riga, la proprietà associata viene impostata su questo valore.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Testo visibile localizzabile da assegnare all'elemento. Se questa voce o l'intera colonna non è presente, per impostazione predefinita il testo corrisponde alla voce corrispondente in Valore.

</dd> <dt>

<span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binario\_
</dt> <dd>

Dati dell'immagine per l'icona. Si tratta di una chiave esterna per la [tabella binaria](binary-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Il contenuto dei campi Value e Text viene formattato dalla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando viene creato il controllo, pertanto può contenere qualsiasi espressione che la funzione MsiFormatRecord può interpretare. La formattazione si verifica solo quando viene creato il controllo e non viene aggiornata se una proprietà coinvolta nell'espressione viene modificata durante il ciclo di vita del controllo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
</dl>

 

 



