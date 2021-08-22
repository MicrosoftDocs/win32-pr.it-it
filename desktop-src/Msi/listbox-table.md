---
description: Le righe di una casella di riepilogo non vengono considerate come singoli controlli, ma fanno parte di una casella di riepilogo che funziona come un controllo . La tabella ListBox definisce i valori per tutte le caselle di riepilogo.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: Tabella ListBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8877db002185cd675914eca6d5be38454796c7b50af6a48f88e0e63c10c195
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043191"
---
# <a name="listbox-table"></a>Tabella ListBox

Le righe di una casella di riepilogo non vengono considerate come singoli controlli, ma fanno parte di una casella di riepilogo che funziona come un controllo . La tabella ListBox definisce i valori per tutte le caselle di riepilogo.

La tabella ListBox include le colonne seguenti.



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

Proprietà denominata da aggiungere a questo elemento. Tutti gli elementi associati alla stessa proprietà diventano parte della stessa casella di riepilogo.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine
</dt> <dd>

Intero positivo utilizzato per determinare l'ordinamento degli elementi visualizzati in una singola casella di riepilogo. Se la casella di riepilogo è definita come ordinata, tutti gli elementi devono avere un valore Order. Non è necessario che i numeri interi siano consecutivi. Se la casella di riepilogo è definita come non ordinata, questa colonna viene ignorata.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Stringa di valore associata a questo elemento. Se si seleziona la riga, la proprietà associata viene impostata su questo valore.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Testo visibile localizzabile da assegnare all'elemento. Se questa voce o l'intera colonna non è presente, per impostazione predefinita il testo corrisponde alla voce corrispondente in Valore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il contenuto dei campi Value e Text viene formattato dalla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) al momento della creazione del controllo, pertanto può contenere qualsiasi espressione che la **funzione MsiFormatRecord** può interpretare. La formattazione si verifica solo quando il controllo viene creato e non viene aggiornato se una proprietà coinvolta nell'espressione viene modificata durante la durata del controllo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE46](ice46.md)  
</dl>

 

 



