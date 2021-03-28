---
description: Per il disegno nell'area client della finestra viene usato un contesto di dispositivo comune.
ms.assetid: 63c4f775-b1a3-4f7c-808b-81c596f26353
title: Contesti di dispositivo di visualizzazione comuni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890b0235784ec1ed11c8ce3a553244629a008d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967063"
---
# <a name="common-display-device-contexts"></a>Contesti di dispositivo di visualizzazione comuni

Per il disegno nell'area client della finestra viene usato un *contesto di dispositivo comune* . Per impostazione predefinita, il sistema fornisce un contesto di dispositivo comune per qualsiasi finestra la cui classe di finestra non specifica in modo esplicito uno stile del contesto del dispositivo di visualizzazione. I contesti di dispositivo comuni vengono in genere usati con le finestre che possono essere disegnate senza modifiche estese agli attributi del contesto di dispositivo. I contesti di dispositivo comuni sono pratici perché non richiedono risorse di memoria o di sistema aggiuntive, ma possono risultare poco pratici se l'applicazione deve configurare molti attributi prima di utilizzarli.

Il sistema recupera tutti i contesti di dispositivo comuni dalla cache del contesto del dispositivo di visualizzazione. Un'applicazione può recuperare un contesto di dispositivo comune immediatamente dopo la creazione della finestra. Poiché il contesto di dispositivo comune è dalla cache, l'applicazione deve sempre rilasciare il contesto di dispositivo appena possibile dopo il disegno. Dopo che il contesto di dispositivo comune è stato rilasciato, non è più valido e l'applicazione non deve tentare di eseguire il progetto. Per ridisegnare, l'applicazione deve recuperare un nuovo contesto di dispositivo comune e continuare a recuperare e rilasciare un contesto di dispositivo comune ogni volta che viene disegnato nella finestra. Se l'applicazione recupera l'handle del contesto di dispositivo usando la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , deve usare la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) per rilasciare l'handle. Analogamente, per ogni funzione [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) , l'applicazione deve usare una funzione [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) corrispondente.

Quando l'applicazione recupera il contesto di dispositivo, il sistema regola l'origine in modo che sia allineata all'angolo superiore sinistro dell'area client. Imposta anche l'area di visualizzazione in modo che l'output nel contesto di dispositivo venga ritagliato nell'area client. Qualsiasi output che altrimenti verrebbe visualizzato all'esterno dell'area client viene troncato. Se l'applicazione recupera il contesto di dispositivo comune usando [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), il sistema include anche l'area di aggiornamento nell'area di ridimensionamento per limitare ulteriormente l'output.

Quando un'applicazione rilascia un contesto di dispositivo comune, il sistema ripristina i valori predefiniti per gli attributi del contesto di dispositivo. Un'applicazione che modifica i valori di attributo deve eseguire tale operazione ogni volta che viene recuperato un contesto di dispositivo comune. Quando si rilascia il contesto di dispositivo, vengono rilasciati tutti gli oggetti Drawing che l'applicazione potrebbe avere selezionato, pertanto l'applicazione non deve rilasciare questi oggetti prima di rilasciare il contesto di dispositivo. In tutti i casi, un'applicazione non deve mai presupporre che il contesto di dispositivo comune mantenga le selezioni non predefinite dopo il rilascio.

 

 



