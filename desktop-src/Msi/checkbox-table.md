---
description: La tabella CheckBox elenca i valori per le caselle di controllo.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Tabella CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310987"
---
# <a name="checkbox-table"></a>Tabella CheckBox

La tabella CheckBox elenca i valori per le caselle di controllo.

La tabella CheckBox contiene le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Proprietà | [Identificatore](identifier.md) | S   | N        |
| Valore    | [Formattato](formatted.md)   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Proprietà denominata da associare a questo elemento.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Stringa del valore associata a questo elemento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la casella di controllo è selezionata, la proprietà corrispondente viene impostata sul valore specificato. Se non è stato specificato alcun valore o la tabella non esiste, la proprietà viene impostata sul valore originale quando la casella di controllo è selezionata. Se il valore originale è null, la proprietà viene impostata su "1".

Il contenuto della colonna valore viene formattato in base alla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando viene creato il controllo. Può quindi contenere qualsiasi espressione che la funzione **MsiFormatRecord** può interpretare. La colonna valore viene formattata solo quando il controllo viene creato e non viene aggiornata se una proprietà in un'espressione viene modificata durante il ciclo di vita del controllo.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



