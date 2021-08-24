---
description: Un contesto di dispositivo comune viene usato per disegnare nell'area client della finestra.
ms.assetid: 63c4f775-b1a3-4f7c-808b-81c596f26353
title: Contesti di dispositivo di visualizzazione comuni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506d9de2d9908be735d959a85ca6bdfe99abf7f33489c74175ab2882551393cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105690"
---
# <a name="common-display-device-contexts"></a>Contesti di dispositivo di visualizzazione comuni

Un *contesto di dispositivo comune* viene usato per disegnare nell'area client della finestra. Il sistema fornisce un contesto di dispositivo comune per impostazione predefinita per qualsiasi finestra la cui classe di finestra non specifica in modo esplicito uno stile del contesto di dispositivo di visualizzazione. I contesti di dispositivo comuni vengono in genere usati con finestre che possono essere disegnate senza modifiche estese agli attributi del contesto di dispositivo. I contesti di dispositivo comuni sono utili perché non richiedono memoria aggiuntiva o risorse di sistema, ma possono risultare poco pratici se l'applicazione deve configurare molti attributi prima di usarli.

Il sistema recupera tutti i contesti di dispositivo comuni dalla cache dei contesti di dispositivo di visualizzazione. Un'applicazione può recuperare un contesto di dispositivo comune immediatamente dopo la creazione della finestra. Poiché il contesto di dispositivo comune deriva dalla cache, l'applicazione deve sempre rilasciare il contesto di dispositivo appena possibile dopo il disegno. Dopo il rilascio, il contesto di dispositivo comune non è più valido e l'applicazione non deve tentare di disegnarlo. Per disegnare di nuovo, l'applicazione deve recuperare un nuovo contesto di dispositivo comune e continuare a recuperare e rilasciare un contesto di dispositivo comune ogni volta che viene disegnata nella finestra. Se l'applicazione recupera l'handle del contesto di dispositivo usando la [**funzione GetDC,**](/windows/desktop/api/Winuser/nf-winuser-getdc) deve usare la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) per rilasciare l'handle. Analogamente, per ogni funzione [**BeginPaint,**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) l'applicazione deve usare una funzione [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) corrispondente.

Quando l'applicazione recupera il contesto di dispositivo, il sistema regola l'origine in modo che sia allineata all'angolo superiore sinistro dell'area client. Imposta anche l'area di ritaglio in modo che l'output nel contesto di dispositivo sia ritagliato nell'area client. Qualsiasi output che altrimenti verrebbe visualizzato all'esterno dell'area client viene ritagliato. Se l'applicazione recupera il contesto di dispositivo comune usando [**BeginPaint,**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)il sistema include anche l'area di aggiornamento nell'area di ritaglio per limitare ulteriormente l'output.

Quando un'applicazione rilascia un contesto di dispositivo comune, il sistema ripristina i valori predefiniti per gli attributi del contesto di dispositivo. Un'applicazione che modifica i valori degli attributi deve eseguire questa operazione ogni volta che recupera un contesto di dispositivo comune. Il rilascio del contesto di dispositivo rilascia tutti gli oggetti di disegno che l'applicazione potrebbe aver selezionato al suo interno, quindi l'applicazione non deve rilasciare questi oggetti prima di rilasciare il contesto di dispositivo. In tutti i casi, un'applicazione non deve mai presupporre che il contesto di dispositivo comune manteni selezioni non predefinite dopo il rilascio.

 

 



