---
description: Il sistema mantiene una cache dei contesti di dispositivo di visualizzazione usati per i contesti di dispositivo comuni, padre e finestra.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Visualizza la cache del contesto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994085"
---
# <a name="display-device-context-cache"></a>Visualizza la cache del contesto del dispositivo

Il sistema mantiene una cache dei contesti di dispositivo di visualizzazione usati per i contesti di dispositivo comuni, padre e finestra. Il sistema Recupera un contesto di dispositivo dalla cache ogni volta che un'applicazione chiama la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ; il sistema restituisce il controller di dominio alla cache quando l'applicazione chiama successivamente la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) o [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .

Non esiste un limite predeterminato per la quantità di contesti di dispositivo che una cache può contenere. Se non ne è disponibile alcuno, il sistema crea un nuovo contesto di dispositivo di visualizzazione per la cache. Dato questo, un'applicazione può avere più di cinque contesti di dispositivo attivi dalla cache alla volta. Tuttavia, l'applicazione deve continuare a rilasciare questi contesti di dispositivo dopo l'utilizzo. Poiché i nuovi contesti di dispositivo di visualizzazione per la cache vengono allocati nello spazio dell'heap dell'applicazione, non è possibile rilasciare i contesti di dispositivo, al fine di utilizzare tutto lo spazio dell'heap disponibile. Il sistema indica questo errore restituendo un errore quando non è possibile allocare spazio per il nuovo contesto di dispositivo. Anche altre funzioni non correlate alla cache possono restituire errori.

 

 



