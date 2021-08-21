---
description: Quando le applicazioni di disegno complesse eseguono operazioni grafiche lunghe, utilizzano risorse di sistema preziose.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Annullamento delle operazioni di disegno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2ddf90842ed7da612e046f8cc44bc8972b236232f3757bd31a295377eafab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470033"
---
# <a name="cancellation-of-drawing-operations"></a>Annullamento delle operazioni di disegno

Quando le applicazioni di disegno complesse eseguono operazioni grafiche lunghe, utilizzano risorse di sistema preziose. Sfruttando le funzionalità multitasking del sistema, un'applicazione può usare i thread e la funzione [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) per gestire queste operazioni. Ad esempio, se l'operazione grafica eseguita dal thread A utilizza le risorse necessarie, il thread B può chiamare la funzione CancelDC per arrestare l'operazione.

 

 



