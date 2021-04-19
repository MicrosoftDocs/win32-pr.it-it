---
description: Le righe di un controllo ListView non vengono considerate come singoli controlli, ma fanno parte di un ListView che funge da controllo. La tabella ListView definisce i valori per tutti i ListView.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: Tabella ListView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310796"
---
# <a name="listview-table"></a>Tabella ListView

Le righe di un controllo ListView non vengono considerate come singoli controlli, ma fanno parte di un ListView che funge da controllo. La tabella ListView definisce i valori per tutti i ListView.

La tabella ListView contiene le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Proprietà | [Identificatore](identifier.md) | S   | N        |
| JSON    | [Integer](integer.md)       | S   | N        |
| Valore    | [Formattato](formatted.md)   | N   | N        |
| Testo     | [Formattato](formatted.md)   | N   | S        |
| Binary\_ | [Identificatore](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Proprietà denominata da associare a questo elemento. Tutti gli elementi collegati alla stessa proprietà diventano parte dello stesso ListView.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine
</dt> <dd>

Intero positivo utilizzato per determinare l'ordinamento degli elementi visualizzati in un singolo elenco ListView. I numeri interi non devono essere consecutivi. Se un ListView viene definito come ordinato, tutti gli elementi devono avere un valore di ordinamento. Se ListView è definito come non ordinato, la colonna viene ignorata.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Stringa del valore associata a questo elemento. Selezionando la riga, la proprietà associata verrà impostata su questo valore.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Testo visibile e localizzabile da assegnare all'elemento. Se questa voce o l'intera colonna risulta mancante, per impostazione predefinita il testo viene impostato sulla voce corrispondente in value.

</dd> <dt>

<span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binario\_
</dt> <dd>

Dati dell'immagine per l'icona. Si tratta di una chiave esterna per la [tabella binaria](binary-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Il contenuto del valore e i campi di testo vengono formattati dalla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando viene creato il controllo, pertanto possono contenere qualsiasi espressione che la funzione MsiFormatRecord possa interpretare. La formattazione si verifica solo quando viene creato il controllo e non viene aggiornata se una proprietà richiesta nell'espressione viene modificata durante il ciclo di vita del controllo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
</dl>

 

 



