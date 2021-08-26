---
description: Le dimensioni di una penna sono specificate in unità dispositivo.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Penne erre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65f875ce5873b5f53cba19b5440751b8ac7683df99765ea7e8e6eec813ef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966071"
---
# <a name="cosmetic-pens"></a>Penne erre

Le dimensioni di una penna sono specificate in unità dispositivo. Pertanto, le linee disegnate con una penna sono sempre a larghezza fissa. Le linee disegnate con una penna geometrica vengono in genere disegnate da 3 a 10 volte più veloci delle linee disegnate con una penna geometrica. Le penne di colore hanno tre attributi: larghezza, stile e colore. Per altre informazioni su questi attributi, vedere [Attributi penna.](pen-attributes.md)

Per creare una penna per il linguaggio, usare [**la funzione CreatePen,**](/windows/desktop/api/Wingdi/nf-wingdi-createpen) [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) Per recuperare una delle tre penne di stock gestito dal sistema, usare la [**funzione GetStockObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)

Dopo aver creato una penna (o aver ottenuto un handle per una delle penne predefinite), selezionare la penna nel contesto di dispositivo (DC) dell'applicazione usando la [**funzione SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Da questo punto in avanti, l'applicazione usa questa penna per qualsiasi operazione di disegno di linee nell'area client.

 

 



