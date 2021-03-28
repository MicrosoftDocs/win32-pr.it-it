---
description: Quando un'applicazione chiama una funzione di disegno per disegnare una forma, il sistema posiziona un pennello all'inizio dell'operazione di disegno ed esegue il mapping di un pixel nella bitmap del pennello all'area client all'origine della finestra, che rappresenta l'angolo superiore sinistro della finestra.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Origine pennello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553165"
---
# <a name="brush-origin"></a>Origine pennello

Quando un'applicazione chiama una funzione di disegno per disegnare una forma, il sistema posiziona un pennello all'inizio dell'operazione di disegno ed esegue il mapping di un pixel nella bitmap del pennello all'area client all' *origine della finestra*, che rappresenta l'angolo superiore sinistro della finestra. Le coordinate del pixel mappato dal sistema sono denominate *origine pennello*. L'origine del pennello predefinita si trova nell'angolo superiore sinistro della bitmap del pennello, in corrispondenza delle coordinate (0, 0). Il sistema copia quindi il pennello sull'area client, formando un modello con altezza pari alla bitmap. L'operazione di copia continua, riga per riga, fino a quando non viene riempita l'intera area client. Tuttavia, il modello di pennello è visibile solo entro i limiti della forma specificata.

Sono presenti istanze in cui l'origine del pennello predefinita non deve essere utilizzata. Ad esempio, potrebbe essere necessario che un'applicazione utilizzi lo stesso pennello per disegnare gli sfondi delle finestre padre e figlio e fondere lo sfondo di una finestra figlio con quella della finestra padre. A tale scopo, l'applicazione deve reimpostare l'origine del pennello chiamando la funzione [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) e spostando l'origine sul numero di pixel richiesto. Un'applicazione può recuperare l'origine del pennello corrente chiamando la funzione [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) .

Nella figura seguente viene illustrata una stella a cinque punte riempita utilizzando un pennello definito dall'applicazione. Nell'illustrazione viene mostrata un'immagine con zoom del pennello, nonché la posizione in cui è stato eseguito il mapping all'inizio dell'operazione di disegno.

![illustrazione che mostra che l'origine del pennello è mappata all'origine della finestra](images/csbru-01.png)

 

 



