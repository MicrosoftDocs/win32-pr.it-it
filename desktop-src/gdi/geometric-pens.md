---
description: Le dimensioni di una penna geometrica sono specificate in unità logiche.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Penne geometriche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993997"
---
# <a name="geometric-pens"></a>Penne geometriche

Le dimensioni di una penna geometrica sono specificate in unità logiche. Pertanto, le linee disegnate con una penna geometrica possono essere ridimensionate, ovvero possono apparire più larghe o più strette, a seconda della trasformazione mondiale corrente. Per ulteriori informazioni sulla trasformazione globale, vedere [spazi di coordinate e trasformazioni](coordinate-spaces-and-transformations.md).

Oltre ai tre attributi condivisi con le penne cosmetiche (larghezza, stile e colore), le penne geometriche posseggono i quattro attributi seguenti: pattern, Hatch facoltativo, stile finale e stile join. Per ulteriori informazioni su questi attributi, vedere [attributi di penna](pen-attributes.md).

Per creare una penna geometrica, un'applicazione usa la funzione [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Come per le penne cosmetiche, la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) seleziona una penna geometrica nel controller di dominio dell'applicazione.

 

 



