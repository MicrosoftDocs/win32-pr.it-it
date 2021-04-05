---
description: Controllo flusso
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Controllo flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41cee586737e131d4a32508b9ba6dd9ef1bd3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883118"
---
# <a name="stream-control"></a>Controllo flusso

L'interfaccia [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) nei pin di input di VMR consente alle applicazioni e ai filtri upstream di controllare il comportamento del componente mixer, inclusi l'ordine Z e lo stato attivo dei flussi di input del VMR. Anche se questa interfaccia viene esposta nei pin, agisce sul componente mixer di VMR, pertanto è disponibile solo quando il mixer viene caricato, ovvero quando il VMR elabora più flussi di input. I filtri upstream usano i metodi [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) e [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) per controllare la chiave del colore di origine. Questi metodi consentono effetti come la sovrapposizione dell'animazione sul video. È sufficiente impostare la chiave di colore sul colore di sfondo del flusso di animazione e il VMR mescolerà il flusso con un altro flusso video. Le applicazioni devono prestare attenzione a non modificare la chiave di colore impostando un valore diverso dal valore usato da un filtro upstream, ad esempio un decodificatore.

I filtri usano i metodi [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) e [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) per indicare al mixer se prevedere i dati di input da un PIN specificato. Ad esempio, il decodificatore Line21 usa questi metodi per attivare il pin di input di VMR per i dati Line21 solo quando i dati sono presenti nel flusso. L'impostazione di un pin su uno stato inattivo indica al mixer di non attendere i dati da un PIN specificato prima di comporre l'immagine.

 

 



