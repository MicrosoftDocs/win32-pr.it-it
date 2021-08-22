---
description: Controllo di flusso
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Controllo di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8da9f317137904a87356bbdcc10dc68357513cf168a0b7b7ea46398ed47a81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072385"
---
# <a name="stream-control"></a>Controllo di flusso

L'interfaccia [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) sui pin di input della macchina virtuale consente alle applicazioni e ai filtri upstream di controllare il comportamento del componente mixer, incluso l'ordine Z e lo stato attivo dei flussi di input della macchina virtuale. Anche se questa interfaccia è esposta sui pin, opera sul componente mixer della VMR, quindi è disponibile solo quando viene caricato il mixer, ovvero quando la macchina virtuale elabora più flussi di input. I filtri upstream usano [**i metodi SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) [**e GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) per controllare la chiave del colore di origine. Questi metodi abilitano effetti come la sovrapposizione dell'animazione su video. È sufficiente impostare la chiave di colore sul colore di sfondo del flusso di animazione e la macchina virtuale combina tale flusso con un altro flusso video. Le applicazioni devono fare attenzione a non modificare la chiave di colore in un valore diverso da quello usato da un filtro upstream, ad esempio un decodificatore.

I filtri usano [**i metodi GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) e [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) per indicare al mixer se aspettarsi dati di input da un pin specificato. Ad esempio, il decodificatore Line21 usa questi metodi per attivare il pin di input della macchina virtuale per i dati Line21 solo quando tali dati sono presenti nel flusso. L'impostazione di un segnaposto su uno stato inattivo indica al mixer di non attendere i dati da un pin specificato prima di comporre l'immagine.

 

 



