---
description: Se questo bit è impostato su un controllo ProgressBar, la barra viene disegnata come una serie di rettangoli di piccole dimensioni. Se questo bit non è impostato, la barra indicatore di stato viene disegnata come un singolo rettangolo continuo.
ms.assetid: b2c43763-799c-4f09-b9f8-47a4a5f4faf3
title: Attributo di controllo Progress95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2242dde671484274be946802ba4fd4c1cfd687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883682"
---
# <a name="progress95-control-attribute"></a>Attributo di controllo Progress95

Se questo bit è impostato su un [controllo ProgressBar](progressbar-control.md), la barra viene disegnata come una serie di rettangoli di piccole dimensioni. Se questo bit non è impostato, la barra indicatore di stato viene disegnata come un singolo rettangolo continuo.

## <a name="valid-controls"></a>Controlli validi

[ProgressBar](progressbar-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                             |
|---------|-------------|--------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit Progress95 nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



