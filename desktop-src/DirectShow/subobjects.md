---
description: Suboggetti
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Suboggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf828d0049816c0cbf932b96344b0270c4c9dbfb835a0750736551ff67b319b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633481"
---
# <a name="subobjects"></a>Suboggetti

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Origini, effetti e transizioni hanno puntatori interni ad altri oggetti COM, denominati *oggetti secondari.* Il sottooggetto esegue il lavoro effettivo dell'oggetto. Il sottooggetto di un'origine è il componente che crea i dati audio o video. Il sottooggetto di un effetto o di una transizione è il componente che trasforma i dati. Ad esempio, in un effetto video crea l'effetto visivo nel flusso video.

Il tipo di oggetto secondario dipende dal tipo di oggetto:

-   Origine: DirectShow filtro di origine o del parser che supporta la ricerca e produce un formato supportato da DES. Può essere un formato compresso se DirectShow filtri esistenti per decodificarlo.
-   Effetto: per i video, qualsiasi oggetto Transform ® DirectX ® 2D. Per l'audio, qualsiasi DirectShow di effetto audio.
-   Transizione: per i video, qualsiasi oggetto Transform DirectX a due input 2D. L'audio non supporta le transizioni.

I gruppi, le composizione e le tracce non hanno oggetti secondari.

L'applicazione non imposta direttamente il puntatore del sottooggetto. Per gli effetti e le transizioni, l'applicazione chiama il metodo [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) per specificare il GUID del sottooggetto. Per gli oggetti di origine, un'applicazione chiama in genere [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) per specificare il nome di un file di origine. Tuttavia, il **metodo SetSubObjectGUID** può essere usato anche per gli oggetti di origine, per specificare l'identificatore di classe (CLSID) di un filtro.

Per altre informazioni, vedere [Working with Sources (Uso delle origini)](working-with-sources.md) [e Working with Effects and Transitions (Uso di effetti e transizioni).](working-with-effects-and-transitions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dei componenti della sequenza temporale](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



