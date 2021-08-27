---
description: Questo attributo misura la distanza di riempimento dell'indicatore di stato.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Attributo del controllo Progress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a867772ff1452087ab22da76d3c1f93aea32e5ad50bd23ffe8ace62889086781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074631"
---
# <a name="progress-control-attribute"></a>Attributo del controllo Progress

Questo attributo misura la distanza di riempimento dell'indicatore di stato. Il record contiene due numeri interi e una stringa. Il primo numero è lo stato di avanzamento, il secondo è l'intervallo (il numero massimo possibile per lo stato). In base all'impostazione, i numeri interi possono essere immessi come campi integer o stringhe contenenti i numeri interi. Se manca il secondo numero, si presuppone che sia il valore predefinito (1024). Se lo stato di avanzamento è maggiore dell'intervallo, viene modificato in modo che sia l'intervallo. Il terzo campo è una stringa, il nome dell'azione di cui viene visualizzato lo stato di avanzamento.

Per informazioni correlate, vedere [Creazione di un controllo ProgressBar](authoring-a-progressbar-control.md)e Aggiunta di azioni personalizzate a [ProgressBar](adding-custom-actions-to-the-progressbar.md).

## <a name="valid-controls"></a>Controlli validi

[ProgressBar](progressbar-control.md)

## <a name="associated-bit-flags"></a>Flag di bit associati

Questo attributo non usa flag di bit.

## <a name="remarks"></a>Commenti

Vedere [Attributi di controllo](control-attributes.md) e il controllo che è necessario creare in [Controlli](controls.md).

 

 



