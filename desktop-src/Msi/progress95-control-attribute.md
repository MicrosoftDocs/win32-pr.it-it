---
description: Se questo bit è impostato su un controllo ProgressBar, la barra viene disegnata come una serie di rettangoli di piccole dimensioni. Se questo bit non è impostato, l'indicatore di stato viene disegnato come un singolo rettangolo continuo.
ms.assetid: b2c43763-799c-4f09-b9f8-47a4a5f4faf3
title: Attributo del controllo Progress95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e6fa8f2c0cd0e1622db4bb406d3ada1b63229e92b60a35e915bf0dacc72fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627350"
---
# <a name="progress95-control-attribute"></a>Attributo del controllo Progress95

Se questo bit è impostato su un [controllo ProgressBar](progressbar-control.md), la barra viene disegnata come una serie di rettangoli di piccole dimensioni. Se questo bit non è impostato, l'indicatore di stato viene disegnato come un singolo rettangolo continuo.

## <a name="valid-controls"></a>Controlli validi

[ProgressBar](progressbar-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                             |
|---------|-------------|--------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo in un controllo , includere il bit Progress95 nella colonna Attributes del record del controllo nella [tabella Control](control-table.md).

Vedere [Attributi di](control-attributes.md) controllo e il controllo che è necessario creare in [Controlli](controls.md).

 

 



