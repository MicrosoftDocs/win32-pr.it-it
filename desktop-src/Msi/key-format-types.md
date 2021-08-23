---
description: I tipi di formato chiave dei dati configurabili possono essere usati nei campi di testo per fornire una chiave in una tabella di database.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Tipi di formato chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a22c4149ec89bd9a1745c28fe17cdafcbcfeaee827dcb35bd8c6badbf2acfb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692491"
---
# <a name="key-format-types"></a>Tipi di formato chiave

I tipi di formato chiave dei dati configurabili possono essere usati nei campi di testo per fornire una chiave in una tabella di database. L'attributo msmConfigItemNonNullable è implicito in questo formato di dati e non deve essere impostato. Null non è mai un valore valido per questo tipo. Le risposte a tutti gli elementi di formato chiave devono essere in [formato speciale CMSM.](cmsm-special-format.md)

Esistono i tipi di formato chiave seguenti:

[Tipo di directory](directory-type.md)

[Tipo di file](file-type.md)

[Tipo di proprietà](property-type.md)

[Tipo di finestra di dialogo](dialog-type.md)

[Tipo binario](binary-type.md)

[Tipo di icona](icon-type.md)

Gli elementi configurabili del tipo di formato chiave vengono usati nelle colonne di testo per fornire una chiave di database e in generale possono essere sostituiti da qualsiasi stringa di testo. I singoli tipi possono avere restrizioni sintattiche aggiuntive, ma queste restrizioni non vengono applicate Mergemod.dll. Particolari elementi configurabili possono avere anche restrizioni semantiche delle caratteristiche. Ad esempio, può essere necessario che un particolare elemento configurabile sia una chiave nella tabella [Binary](binary-table.md) in una riga contenente un'immagine bitmap. Queste restrizioni non vengono applicate dai Mergemod.dll e pertanto gli autori di moduli devono essere preparati a gestire qualsiasi stringa che soddisfi il tipo di formato della chiave specificato. Se non diversamente specificato dal significato semantico o dagli attributi, null è una risposta valida.

 

 



