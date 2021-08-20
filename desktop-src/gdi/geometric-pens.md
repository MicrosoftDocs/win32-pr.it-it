---
description: Le dimensioni di una penna geometrica sono specificate in unità logiche.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Penne geometriche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 748efb1748634b4fd5add35b62a7e6e8c576293f20eee62421674f59128821f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699243"
---
# <a name="geometric-pens"></a>Penne geometriche

Le dimensioni di una penna geometrica sono specificate in unità logiche. Di conseguenza, le linee disegnate con una penna geometrica possono essere ridimensionate, ad esempio possono apparire più larghe o più sottili, a seconda della trasformazione globale corrente. Per altre informazioni sulla trasformazione globale, vedere [Spazi delle coordinate e trasformazioni](coordinate-spaces-and-transformations.md).

Oltre ai tre attributi condivisi con le penne estetiche (larghezza, stile e colore), le penne geometriche possiedono i quattro attributi seguenti: modello, tratteggio facoltativo, stile finale e stile di join. Per altre informazioni su questi attributi, vedere [Attributi penna](pen-attributes.md).

Per creare una penna geometrica, un'applicazione usa la [**funzione ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) Come per le penne estetiche, la [**funzione SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) seleziona una penna geometrica nel controller di dominio dell'applicazione.

 

 



