---
description: Questo attributo misura la distanza di riempimento della barra indicatore di stato.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Attributo di controllo progress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318651"
---
# <a name="progress-control-attribute"></a>Attributo di controllo progress

Questo attributo misura la distanza di riempimento della barra indicatore di stato. Il record contiene due Integer e una stringa. Il primo numero è lo stato di avanzamento, il secondo numero è l'intervallo (il numero massimo possibile per lo stato di avanzamento). In impostazione, i numeri interi possono essere immessi come campi interi o stringhe contenenti i numeri interi. Se il secondo numero è mancante, si presuppone che sia il valore predefinito (1024). Se lo stato di avanzamento è maggiore di quello dell'intervallo, questo viene modificato in modo da essere compreso nell'intervallo. Il terzo campo è una stringa, il nome dell'azione di cui viene visualizzato lo stato di avanzamento.

Per informazioni correlate, vedere [creazione di un controllo ProgressBar](authoring-a-progressbar-control.md)e [aggiunta di azioni personalizzate a ProgressBar](adding-custom-actions-to-the-progressbar.md).

## <a name="valid-controls"></a>Controlli validi

[ProgressBar](progressbar-control.md)

## <a name="associated-bit-flags"></a>Flag di bit associati

Questo attributo non utilizza flag di bit.

## <a name="remarks"></a>Commenti

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



