---
description: Utilizzo degli effetti e delle transizioni
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Utilizzo degli effetti e delle transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968688"
---
# <a name="working-with-effects-and-transitions"></a>Utilizzo degli effetti e delle transizioni

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Gli effetti modificano un singolo clip, traccia o composizione. Le transizioni creano un seques da una traccia o compositionsto un altro.

I [servizi di modifica DirectShow](directshow-editing-services.md) usano oggetti di trasformazione DirectX per le transizioni video e gli effetti video. Per le transizioni video, usare qualsiasi oggetto di trasformazione DirectX a due input 2D. Per gli effetti video, usare qualsiasi oggetto trasformazione DirectX a input singolo 2D. Microsoft non supporta più lo sviluppo di oggetti di trasformazione DirectX di terze parti. Tuttavia, diverse sono fornite con DirectShow e altre sono fornite con Microsoft Internet Explorer. Per ulteriori informazioni sulle transizioni fornite con Internet Explorer, vedere [riferimenti a filtri visivi e transizioni](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).

Per gli effetti audio, è possibile usare qualsiasi filtro effetto audio DirectShow. DES fornisce anche un [effetto busta volume](volume-envelope-effect.md) per l'impostazione del volume su una traccia o un clip. DES non supporta le transizioni audio.

Questa sezione contiene i seguenti argomenti:

-   [Aggiunta di oggetti Effect e Transition](adding-effect-and-transition-objects.md)
-   [Anteprima degli effetti e delle transizioni](previewing-effects-and-transitions.md)
-   [Enumerazione degli effetti e delle transizioni](enumerating-effects-and-transitions.md)
-   [Impostazione delle proprietà per effetti e transizioni](setting-properties-on-effects-and-transitions.md)
-   [Direzione della transizione](transition-direction.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei servizi di modifica DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 
