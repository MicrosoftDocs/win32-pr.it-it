---
description: Se questo bit è impostato su un controllo di modifica, il programma di installazione crea un controllo di modifica a più righe con una barra di scorrimento verticale.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Attributo di controllo su più righe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226971"
---
# <a name="multiline-control-attribute"></a>Attributo di controllo su più righe

Se questo bit è impostato su un [controllo di modifica](edit-control.md), il programma di installazione crea un controllo di modifica a più righe con una barra di scorrimento verticale.

Se questo bit non è impostato, viene specificato di visualizzare un normale controllo di modifica.

## <a name="valid-controls"></a>Controlli validi

[Controllo di modifica](edit-control.md).



| Decimal | Valore esadecimale | Costante                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit su più righe nella colonna attributi del record del controllo nella [tabella del controllo](control-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 



