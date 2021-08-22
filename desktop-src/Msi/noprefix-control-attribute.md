---
description: Se questo bit è impostato su un controllo di testo, l'occorrenza del carattere &\# 0034;&&0034; in una stringa di testo viene visualizzata come \# se stessa. Se questo bit non è impostato, il carattere che segue &\# 0034;&&0034; nella stringa di testo viene visualizzato come carattere di \# sottolineatura.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: Attributo del controllo NoPrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15345bb56ad85ec654cffe7a0bf2173973e032ac33aca633105d3a220647cf93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065881"
---
# <a name="noprefix-control-attribute"></a>Attributo del controllo NoPrefix

Se questo bit è impostato su un controllo di testo, l'occorrenza del carattere "&" in una stringa di testo viene visualizzata come se stessa. Se questo bit non è impostato, il carattere che segue "&" nella stringa di testo viene visualizzato come carattere di sottolineatura.

## <a name="valid-controls"></a>Controlli validi

[Text](text-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x20000     | **msidbControlAttributesNoPrefix** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo in un controllo, includere il bit NoPrefix nella colonna Attributes del record del controllo nella [tabella Control](control-table.md).

Vedere [Attributi e controlli](control-attributes.md) del [controllo.](controls.md)

 

 



