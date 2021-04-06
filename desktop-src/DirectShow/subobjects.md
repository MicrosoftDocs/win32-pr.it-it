---
description: Oggetti secondari
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Oggetti secondari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883726"
---
# <a name="subobjects"></a>Oggetti secondari

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Origini, effetti e transizioni hanno puntatori interni ad altri oggetti COM, detti *sottooggetti*. Il sottooggetto esegue il lavoro effettivo dell'oggetto. Il sottooggetto di un'origine è il componente che crea il video o i dati audio. Il sottooggetto di un effetto o di una transizione è il componente che trasforma i dati. ad esempio, in un effetto video, viene creato l'effetto visivo nel flusso video.

Il tipo di oggetto SubObject dipende dal tipo di oggetto:

-   Origine: qualsiasi filtro di origine o filtro del parser DirectShow che supporta la ricerca e produce un formato supportato da DES. Può trattarsi di un formato compresso se esistono filtri DirectShow per decodificarlo.
-   Effetto: per i video, qualsiasi oggetto 2D® DirectX® Transform a input singolo. Per audio, qualsiasi filtro effetto audio DirectShow.
-   Transizione: per video, qualsiasi oggetto di trasformazione DirectX a due input 2D. L'audio non supporta le transizioni.

Gruppi, composizioni e tracce non dispongono di sottooggetti.

L'applicazione non imposta direttamente il puntatore del sottooggetto. Per gli effetti e le transizioni, l'applicazione chiama il metodo [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) per specificare il GUID dell'oggetto SubObject. Per gli oggetti di origine, un'applicazione chiama in genere [**IAMTimelineSrc:: Semedianame**](iamtimelinesrc-setmedianame.md) per specificare il nome di un file di origine. Tuttavia, il metodo **SetSubObjectGUID** può essere usato anche per gli oggetti di origine, per specificare l'identificatore di classe (CLSID) di un filtro.

Per ulteriori informazioni, vedere [utilizzo di origini](working-with-sources.md) e [utilizzo di effetti e transizioni](working-with-effects-and-transitions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dei componenti della sequenza temporale](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



