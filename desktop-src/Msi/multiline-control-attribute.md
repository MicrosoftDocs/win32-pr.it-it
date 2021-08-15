---
description: Se questo bit è impostato su un controllo Edit, il programma di installazione crea un controllo di modifica su più righe con una barra di scorrimento verticale.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Attributo del controllo MultiLine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474bf8a9b765f402924a554c9da064a8c60a01f6af910a3fd24c81d377978a93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943432"
---
# <a name="multiline-control-attribute"></a>Attributo del controllo MultiLine

Se questo bit è impostato su un controllo [Edit](edit-control.md), il programma di installazione crea un controllo di modifica su più righe con una barra di scorrimento verticale.

Se questo bit non è impostato, specifica la visualizzazione di un normale controllo di modifica.

## <a name="valid-controls"></a>Controlli validi

[Modificare il controllo](edit-control.md).



| Decimal | Valore esadecimale | Costante                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo in un controllo, includere il bit MultiLine nella colonna Attributi del record del controllo nella [tabella Control](control-table.md).

Vedere [Attributi e controlli](control-attributes.md) del [controllo](controls.md).

 

 



