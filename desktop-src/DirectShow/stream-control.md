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
# <a name="stream-control"></a><span data-ttu-id="23b00-103">Controllo flusso</span><span class="sxs-lookup"><span data-stu-id="23b00-103">Stream Control</span></span>

<span data-ttu-id="23b00-104">L'interfaccia [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) nei pin di input di VMR consente alle applicazioni e ai filtri upstream di controllare il comportamento del componente mixer, inclusi l'ordine Z e lo stato attivo dei flussi di input del VMR.</span><span class="sxs-lookup"><span data-stu-id="23b00-104">The [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) interface on the VMR's input pin(s) enables applications and upstream filters to control the behavior of the mixer component, including the Z-order and the active state of the VMR's input streams.</span></span> <span data-ttu-id="23b00-105">Anche se questa interfaccia viene esposta nei pin, agisce sul componente mixer di VMR, pertanto è disponibile solo quando il mixer viene caricato, ovvero quando il VMR elabora più flussi di input.</span><span class="sxs-lookup"><span data-stu-id="23b00-105">Although this interface is exposed on the pins, it operates on the VMR's mixer component, so it is only available when the mixer is loaded, which is when the VMR is processing multiple input streams.</span></span> <span data-ttu-id="23b00-106">I filtri upstream usano i metodi [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) e [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) per controllare la chiave del colore di origine.</span><span class="sxs-lookup"><span data-stu-id="23b00-106">Upstream filters use the [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) and [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) methods to control the source color key.</span></span> <span data-ttu-id="23b00-107">Questi metodi consentono effetti come la sovrapposizione dell'animazione sul video.</span><span class="sxs-lookup"><span data-stu-id="23b00-107">These methods enable effects such as the overlay of animation over video.</span></span> <span data-ttu-id="23b00-108">È sufficiente impostare la chiave di colore sul colore di sfondo del flusso di animazione e il VMR mescolerà il flusso con un altro flusso video.</span><span class="sxs-lookup"><span data-stu-id="23b00-108">Simply set the color key to the animation stream's background color, and the VMR will mix that stream with another video stream.</span></span> <span data-ttu-id="23b00-109">Le applicazioni devono prestare attenzione a non modificare la chiave di colore impostando un valore diverso dal valore usato da un filtro upstream, ad esempio un decodificatore.</span><span class="sxs-lookup"><span data-stu-id="23b00-109">Applications should take care not to change the color key to some value that is different than the value being used by an upstream filter, such as a decoder.</span></span>

<span data-ttu-id="23b00-110">I filtri usano i metodi [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) e [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) per indicare al mixer se prevedere i dati di input da un PIN specificato.</span><span class="sxs-lookup"><span data-stu-id="23b00-110">Filters use the [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) and [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) methods to tell the mixer whether to expect input data from a specified pin.</span></span> <span data-ttu-id="23b00-111">Ad esempio, il decodificatore Line21 usa questi metodi per attivare il pin di input di VMR per i dati Line21 solo quando i dati sono presenti nel flusso.</span><span class="sxs-lookup"><span data-stu-id="23b00-111">For example, the Line21 Decoder uses these methods to activate the VMR's input pin for Line21 data only when that data is present in the stream.</span></span> <span data-ttu-id="23b00-112">L'impostazione di un pin su uno stato inattivo indica al mixer di non attendere i dati da un PIN specificato prima di comporre l'immagine.</span><span class="sxs-lookup"><span data-stu-id="23b00-112">Setting a pin to an inactive state instructs the mixer not to wait for data from a specified pin before compositing the image.</span></span>

 

 



