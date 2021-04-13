---
title: Esecuzione di query sulle variabili di stato
description: L'interfaccia IUPnPService fornisce il metodo QueryStateVariable, che restituisce il valore di una variabile di stato specificata.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a716bbe93c2306eca43b977a42f33a85187f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329591"
---
# <a name="querying-state-variables"></a>Esecuzione di query sulle variabili di stato

L'interfaccia [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) fornisce il metodo [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , che restituisce il valore di una variabile di stato specificata.

Il forum di UPnP sconsiglia l'uso di [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable). È stato suggerito ai writer di dispositivi di scrivere le azioni appropriate per fornire queste informazioni. I writer di dispositivi non sono obbligati a implementare **QueryStateVariable**.

Vedere la sezione [richiamo di azioni](invoking-actions.md).

 

 




