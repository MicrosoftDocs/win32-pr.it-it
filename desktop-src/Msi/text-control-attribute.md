---
description: Questo attributo è la stringa di testo visualizzata nel controllo .
ms.assetid: 0c4b7183-a43a-4c91-b01e-9f377500ba38
title: Attributo del controllo Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 249951290e59d8e76f11cae66ab61956727068c99713ed2e5a18a40c9c9a7522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141860"
---
# <a name="text-control-attribute"></a>Attributo del controllo Text

Questo attributo è la stringa di testo visualizzata nel controllo . In caso di impostazione, se il campo 0 del record non è Null, il record viene formattato usando FormatText. Se il campo 0 è Null, il primo campo del record definisce il testo. Quando si riceve il valore, viene sempre restituito nel primo campo. Per alcuni controlli questo testo potrebbe non essere visibile. In Windows il tasto di scelta rapida per un controllo viene definito inserendo un "&" davanti al carattere desiderato in questa stringa.

## <a name="valid-controls"></a>Controlli validi

Tutti i controlli ad eccezione [del controllo Line.](line-control.md)

## <a name="associated-bit-flags"></a>Flag di bit associati

No.

## <a name="remarks"></a>Osservazioni

Vedere [Attributi di](control-attributes.md) controllo e il controllo che è necessario creare in [Controlli](controls.md).

 

 



