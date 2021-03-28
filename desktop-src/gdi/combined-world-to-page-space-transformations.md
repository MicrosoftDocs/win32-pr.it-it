---
description: Le cinque trasformazioni da mondo a pagina possono essere combinate in una singola matrice 3 per 3.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Trasformazioni di spazi globali combinate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978730"
---
# <a name="combined-world-to-page-space-transformations"></a>Trasformazioni di spazi globali combinate

Le cinque trasformazioni da mondo a pagina possono essere combinate in una singola matrice 3 per 3. La funzione [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) può essere usata per combinare due trasformazioni dello spazio globale per la pagina. Le trasformazioni combinate possono essere usate per modificare l'output associato a un particolare contesto di dispositivo (DC) chiamando la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) e fornendo gli elementi per questa matrice. Quando un'applicazione chiama **SetWorldTransform**, archivia gli elementi della matrice 3 per 3 [**in una struttura**](/windows/win32/api/wingdi/ns-wingdi-xform) . I membri di questa struttura corrispondono alle prime due colonne di una matrice 3 per 3. L'ultima colonna della matrice non è obbligatoria perché i relativi valori sono costanti.

Gli elementi della matrice di trasformazione globale corrente possono essere riattivati chiamando la funzione [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) e specificando un puntatore a una [**struttura di**](/windows/win32/api/wingdi/ns-wingdi-xform) un elemento di un oggetto.

 

 



