---
description: Questo attributo è la stringa di testo visualizzata nel controllo.
ms.assetid: 0c4b7183-a43a-4c91-b01e-9f377500ba38
title: Attributo controllo testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3f4eb83f6f796180d3125025afedbc08d956d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227189"
---
# <a name="text-control-attribute"></a>Attributo controllo testo

Questo attributo è la stringa di testo visualizzata nel controllo. In caso di impostazione, se il campo 0 del record non è null, il record viene formattato con FormatText. Se il campo 0 è null, il primo campo del record definisce il testo. Quando si recupera il valore viene sempre restituito nel primo campo. Per alcuni controlli questo testo potrebbe non essere visibile. In Windows il tasto di scelta rapida per un controllo viene definito inserendo un "&" prima del carattere desiderato in questa stringa.

## <a name="valid-controls"></a>Controlli validi

Tutti i controlli ad eccezione del [controllo line](line-control.md).

## <a name="associated-bit-flags"></a>Flag di bit associati

No.

## <a name="remarks"></a>Osservazioni

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



