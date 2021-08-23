---
description: Nella tabella CheckBox sono elencati i valori per le caselle di controllo.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Tabella CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848769f9430681a8c37de0afd8d9d1fa8abfee2f833798ecbdc5271535f79da4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649871"
---
# <a name="checkbox-table"></a>Tabella CheckBox

Nella tabella CheckBox sono elencati i valori per le caselle di controllo.

La tabella CheckBox include le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Proprietà | [Identificatore](identifier.md) | S   | N        |
| Valore    | [Formattato](formatted.md)   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Proprietà denominata da aggiungere a questo elemento.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Stringa di valore associata a questo elemento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la casella di controllo è selezionata, la proprietà corrispondente viene impostata sul valore specificato. Se non è specificato alcun valore o questa tabella non esiste, la proprietà viene impostata sul valore originale quando la casella di controllo è selezionata. Se il valore originale è Null, la proprietà viene impostata su "1".

Il contenuto della colonna Value viene formattato dalla [**funzione MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando viene creato il controllo. Può pertanto contenere qualsiasi espressione che può essere **interpretata dalla funzione MsiFormatRecord.** La colonna Valore viene formattata solo quando il controllo viene creato e non viene aggiornato se una proprietà coinvolta in un'espressione viene modificata durante la durata del controllo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



