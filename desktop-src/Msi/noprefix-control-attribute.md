---
description: Se questo bit è impostato su un controllo di testo, l'occorrenza del carattere &\# 0034; &&\# 0034; in una stringa di testo viene visualizzata come se stessa. Se questo bit non è impostato, il carattere che segue &\# 0034; &&\# 0034; nella stringa di testo viene visualizzato come carattere di sottolineatura.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix (attributo di controllo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226612"
---
# <a name="noprefix-control-attribute"></a>NoPrefix (attributo di controllo)

Se questo bit è impostato su un controllo di testo, l'occorrenza del carattere "&" in una stringa di testo viene visualizzata come se stessa. Se questo bit non è impostato, il carattere che segue "&" nella stringa di testo viene visualizzato come carattere di sottolineatura.

## <a name="valid-controls"></a>Controlli validi

[Text](text-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x20000     | **msidbControlAttributesNoPrefix** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit NoPrefix nella colonna attributi del record del controllo nella [tabella dei controlli](control-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 



