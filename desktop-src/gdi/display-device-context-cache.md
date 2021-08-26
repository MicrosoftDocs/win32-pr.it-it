---
description: Il sistema gestisce una cache dei contesti di dispositivo di visualizzazione che usa per contesti di dispositivo comuni, padre e finestra.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Visualizzare la cache del contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d96bbf8cb388e31e43a0eacf9200b638fe8a232749dd5e2ef8ab67318b30d9de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062431"
---
# <a name="display-device-context-cache"></a>Visualizzare la cache del contesto di dispositivo

Il sistema gestisce una cache dei contesti di dispositivo di visualizzazione che usa per contesti di dispositivo comuni, padre e finestra. Il sistema recupera un contesto di dispositivo dalla cache ogni volta che un'applicazione chiama la [**funzione GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) [**o BeginPaint.**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) il sistema restituisce il controller di dominio alla cache quando l'applicazione successivamente chiama la [**funzione ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) [**o EndPaint.**](/windows/desktop/api/Winuser/nf-winuser-endpaint)

Non esiste alcun limite predeterminato per la quantità di contesti di dispositivo che una cache può contenere; il sistema crea un nuovo contesto di dispositivo di visualizzazione per la cache se non ne è disponibile nessuno. In questo caso, un'applicazione può avere più di cinque contesti di dispositivo attivi dalla cache alla volta. Tuttavia, l'applicazione deve continuare a rilasciare questi contesti di dispositivo dopo l'uso. Poiché i nuovi contesti di dispositivo di visualizzazione per la cache vengono allocati nello spazio heap dell'applicazione, il mancato rilascio dei contesti di dispositivo alla fine usa tutto lo spazio heap disponibile. Il sistema indica questo errore restituisce un errore quando non è possibile allocare spazio per il nuovo contesto di dispositivo. Anche altre funzioni non correlate alla cache possono restituire errori.

 

 



