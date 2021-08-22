---
description: L'attributo style specifica il motivo linea che viene visualizzato quando viene usata una penna geometrica o geometrica specifica. Sono disponibili otto stili di penna predefiniti. La figura seguente mostra i sette di questi stili definiti dal sistema.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Stile penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42cc82510c58d36cec76039488ecc13c826609a0870b929f18d82282a87ba8cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666511"
---
# <a name="pen-style"></a>Stile penna

L'attributo style specifica il motivo linea che viene visualizzato quando viene usata una penna geometrica o geometrica specifica. Sono disponibili otto stili di penna predefiniti. La figura seguente mostra i sette di questi stili definiti dal sistema.

![illustrazione che mostra sette linee, ognuna disegnata con uno stile predefinito diverso](images/cspen-01.png)

Lo stile all'interno della cornice è identico allo stile a tinta unita per le penne della cornice. Tuttavia, funziona in modo diverso quando viene usato con una penna geometrica. Se la penna geometrica è più larga di un singolo pixel e una funzione di disegno usa la penna per disegnare un bordo intorno a un oggetto pieno, il sistema disegna il bordo all'interno della cornice dell'oggetto. Usando lo stile all'interno del frame, un'applicazione può garantire che un oggetto venga visualizzato interamente all'interno delle dimensioni specificate, indipendentemente dalla larghezza geometrica della penna.

Oltre ai sette stili definiti dal sistema, esiste un ottavo stile definito dall'utente (o dall'applicazione). Uno stile definito dall'utente genera linee con una serie personalizzata di trattini e punti.

Usare la [**funzione CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) per creare una penna con gli stili definiti dal sistema. Usare la **funzione ExtCreatePen** per creare una penna con uno stile definito dall'utente.

 

 



