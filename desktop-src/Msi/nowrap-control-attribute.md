---
description: Se questo bit è impostato, il testo nel controllo viene visualizzato su una sola riga. Se il testo si estende oltre i margini del controllo, viene troncato e i puntini di sospensione (&\# 0034;... &\# 0034;) viene inserito alla fine per indicare il troncamento. Se questo bit non è impostato, il testo viene incapsulato.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Attributo di controllo nowrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313339"
---
# <a name="nowrap-control-attribute"></a>Attributo di controllo nowrap

Se questo bit è impostato, il testo nel controllo viene visualizzato su una sola riga. Se il testo si estende oltre i margini del controllo, viene troncato e al termine vengono inseriti i puntini di sospensione ("...") per indicare il troncamento. Se questo bit non è impostato, il testo viene incapsulato.

## <a name="valid-controls"></a>Controlli validi

[Text](text-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesNoWrap** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit nowrap nella colonna attributi del record del controllo nella [tabella dei controlli](control-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 



