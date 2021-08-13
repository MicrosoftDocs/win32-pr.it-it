---
description: Quando un'applicazione chiama una funzione di disegno per disegnare una forma, il sistema posiziona un pennello all'inizio dell'operazione di disegno ed esegue il mapping di un pixel nella bitmap del pennello all'area client all'origine della finestra, ovvero l'angolo superiore sinistro della finestra.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Origine pennello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ccdc1dfa370ceb84216c89d562ef56dd206ce744b3be4fd38deb87175c1cf73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400391"
---
# <a name="brush-origin"></a>Origine pennello

Quando un'applicazione chiama una funzione di disegno per disegnare una forma, il sistema posiziona un pennello all'inizio dell'operazione di disegno ed esegue il mapping di un pixel nella bitmap del pennello all'area client all'origine della finestra *,* ovvero l'angolo superiore sinistro della finestra. Le coordinate del pixel mappato dal sistema sono denominate origine *del pennello.* L'origine del pennello predefinita si trova nell'angolo superiore sinistro della bitmap del pennello, in corrispondenza delle coordinate (0,0). Il sistema copia quindi il pennello nell'area client, formando un motivo alto quanto la bitmap. L'operazione di copia continua, riga per riga, fino a riempire l'intera area client. Tuttavia, il motivo del pennello è visibile solo all'interno dei limiti della forma specificata.

Esistono istanze in cui l'origine del pennello predefinita non deve essere usata. Ad esempio, può essere necessario che un'applicazione usi lo stesso pennello per disegnare gli sfondi delle finestre padre e figlio e sfumato lo sfondo di una finestra figlio con quello della finestra padre. A tale scopo, l'applicazione deve reimpostare l'origine del pennello chiamando la [**funzione SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) e spostando l'origine sul numero di pixel richiesto. Un'applicazione può recuperare l'origine del pennello corrente chiamando la [**funzione GetBrushOrgEx.**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)

La figura seguente mostra una stella a cinque punte riempita usando un pennello definito dall'applicazione. La figura mostra un'immagine ingrandita del pennello, nonché la posizione in cui è stato mappato all'inizio dell'operazione di disegno.

![illustrazione che mostra che l'origine del pennello è mappata all'origine della finestra](images/csbru-01.png)

 

 



