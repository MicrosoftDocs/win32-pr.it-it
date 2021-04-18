---
description: I tipi di formato chiave dei dati configurabili possono essere utilizzati nei campi di testo per fornire una chiave in una tabella di database.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Tipi di formato chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307257"
---
# <a name="key-format-types"></a>Tipi di formato chiave

I tipi di formato chiave dei dati configurabili possono essere utilizzati nei campi di testo per fornire una chiave in una tabella di database. L'attributo msmConfigItemNonNullable è implicito in questo formato dati e non è necessario impostarlo. Null non è mai un valore valido per questo tipo. Le risposte a tutti gli elementi di formato chiave devono essere nel [formato speciale CMSM](cmsm-special-format.md).

Esistono i tipi di formato chiave seguenti:

[Tipo di directory](directory-type.md)

[Tipo di file](file-type.md)

[Tipo di proprietà](property-type.md)

[Tipo di finestra di dialogo](dialog-type.md)

[Tipo binario](binary-type.md)

[Tipo di icona](icon-type.md)

Gli elementi configurabili del tipo di formato chiave vengono utilizzati nelle colonne di testo per fornire una chiave del database e, in generale, possono essere sostituiti da qualsiasi stringa di testo. I singoli tipi possono avere restrizioni sintattiche aggiuntive, ma queste restrizioni non vengono applicate da Mergemod.dll. Particolari elementi configurabili possono anche avere restrizioni semantiche caratteristiche. Ad esempio, potrebbe essere necessario un particolare elemento configurabile come chiave nella [tabella binaria](binary-table.md) in una riga contenente un'immagine bitmap. Tali restrizioni non vengono applicate da Mergemod.dll e pertanto gli autori dei moduli devono essere preparati a gestire qualsiasi stringa che soddisfi il tipo di formato della chiave specificato. Se non diversamente specificato dal significato semantico o dagli attributi, null è una risposta valida.

 

 



