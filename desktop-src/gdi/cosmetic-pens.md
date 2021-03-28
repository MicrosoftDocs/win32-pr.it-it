---
description: Le dimensioni di una penna cosmetica sono specificate in unità dispositivo.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Penne cosmetiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754466"
---
# <a name="cosmetic-pens"></a>Penne cosmetiche

Le dimensioni di una penna cosmetica sono specificate in unità dispositivo. Pertanto, le linee disegnate con una penna cosmetica hanno sempre una larghezza fissa. Le linee disegnate con una penna cosmetica vengono in genere disegnate da 3 a 10 volte più velocemente rispetto alle linee disegnate con una penna geometrica. Le penne cosmetiche hanno tre attributi: larghezza, stile e colore. Per ulteriori informazioni su questi attributi, vedere [attributi di penna](pen-attributes.md).

Per creare una penna cosmetica, usare la funzione [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Per recuperare una delle tre penne cosmetiche predefinite gestite dal sistema, usare la funzione [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) .

Dopo la creazione di una penna (o l'ottenimento di un handle per una delle penne predefinite), selezionare la penna nel contesto di dispositivo (DC) dell'applicazione usando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Da questo punto in poi, l'applicazione usa questa penna per tutte le operazioni di disegno di riga nell'area client.

 

 



