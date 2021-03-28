---
description: L'attributo di stile specifica il modello di linea visualizzato quando viene usata una particolare penna cosmetica o geometrica. Sono disponibili otto stili di penna predefiniti. Nella figura seguente sono illustrati i sette stili definiti dal sistema.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Stile penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967056"
---
# <a name="pen-style"></a>Stile penna

L'attributo di stile specifica il modello di linea visualizzato quando viene usata una particolare penna cosmetica o geometrica. Sono disponibili otto stili di penna predefiniti. Nella figura seguente sono illustrati i sette stili definiti dal sistema.

![illustrazione che mostra sette righe, ciascuna disegnata usando uno stile predefinito diverso](images/cspen-01.png)

Lo stile frame interno è identico allo stile solido per le penne cosmetiche. Tuttavia, funziona in modo diverso quando viene usato con una penna geometrica. Se la penna geometrica è più ampia rispetto a un singolo pixel e una funzione di disegno usa la penna per disegnare un bordo intorno a un oggetto riempito, il sistema disegna il bordo all'interno del frame dell'oggetto. Utilizzando lo stile frame interno, un'applicazione può garantire che un oggetto venga visualizzato interamente all'interno delle dimensioni specificate, indipendentemente dalla larghezza della penna geometrica.

Oltre ai sette stili definiti dal sistema, esiste un ottavo stile definito da utente (o applicazione). Uno stile definito dall'utente genera linee con una serie personalizzata di trattini e punti.

Usare la funzione [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) per creare una penna con stili definiti dal sistema. Utilizzare la funzione **ExtCreatePen** per creare una penna con stile definito dall'utente.

 

 



