---
description: La tabella UIText contiene le versioni localizzate di alcune stringhe utilizzate nell'interfaccia utente. Queste stringhe non fanno parte di nessun'altra tabella. La tabella UIText è per le stringhe che non dispongono di una posizione logica in nessun'altra tabella.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: Tabella UIText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128099"
---
# <a name="uitext-table"></a>Tabella UIText

La tabella UIText contiene le versioni localizzate di alcune stringhe utilizzate nell'interfaccia utente. Queste stringhe non fanno parte di nessun'altra tabella. La tabella UIText è per le stringhe che non dispongono di una posizione logica in nessun'altra tabella.

La tabella UIText include le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| Chiave    | [Identificatore](identifier.md) | S   | N        |
| Testo   | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Chiave univoca che identifica la stringa particolare.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

Versione localizzata della stringa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Alcuni controlli utilizzano la tabella UIText come origine delle stringhe. Per informazioni sulle stringhe richieste in questa tabella per ogni particolare controllo, vedere i singoli controlli nella Guida di [riferimento all'interfaccia utente](user-interface-reference.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



