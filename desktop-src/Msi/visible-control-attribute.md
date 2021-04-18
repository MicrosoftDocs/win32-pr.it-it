---
description: Se viene impostato il bit del controllo visibile, il controllo è visibile nella finestra di dialogo. Se questo bit non è impostato, il controllo è nascosto nella finestra di dialogo. Lo stato visibile o nascosto dell'attributo del controllo visibile può essere modificato in seguito da un evento del controllo.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Attributo controllo visibile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306565"
---
# <a name="visible-control-attribute"></a>Attributo controllo visibile

Se viene impostato il bit del controllo visibile, il controllo è visibile nella finestra di dialogo. Se questo bit non è impostato, il controllo è nascosto nella finestra di dialogo. Lo stato visibile o nascosto dell'attributo del controllo visibile può essere modificato in seguito da un [evento del controllo](control-events.md).

## <a name="valid-controls"></a>Controlli validi

Tutti i controlli.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                          |
|---------|-------------|-----------------------------------|
| 1       | 0x00000001  | **msidbControlAttributesVisible** |



 

## <a name="remarks"></a>Commenti

È possibile utilizzare la [tabella ControlCondition](controlcondition-table.md) per visualizzare o nascondere un controllo in base al valore di una proprietà o di un'istruzione condizionale. È anche possibile visualizzare o nascondere un controllo sottoscrivendo il controllo a un [ControlEvent](control-events.md). Immettere l'identificatore dell'attributo nella colonna Attribute e l'identificatore dell'evento nella colonna Event della [tabella EventMapping](eventmapping-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 



