---
description: Uso dei DMO multimediali
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Uso dei DMO multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a75d7eb65e92a89d5d413d8cc04a7dbb9f1891d6b23a9cc3c1242fbae46f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100919"
---
# <a name="working-with-dmo-media-types"></a>Uso dei DMO multimediali

I tipi di supporti di input e output usati dagli oggetti DMO del codec vengono definiti usando la [**DMO \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Questa struttura è identica sia a [**WM \_ MEDIA \_ TYPE,**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)definito in Windows Media Format SDK, sia ad [**AM MEDIA \_ \_ TYPE,**](/windows/win32/api/strmif/ns-strmif-am_media_type)definito in Microsoft DirectShow®. A seconda dell'applicazione, è possibile usare variabili definite come uno di questi tre tipi. È possibile eseguire il cast di un puntatore a una delle strutture del tipo di supporto come un'altra. Esempio:


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



I tipi di formato usati dai codec sono in genere limitati a quelli descritti dalle strutture **VIDEOINFOHEADER** e **WAVEFORMATEX.** Per praticità, le costanti per questi tipi di formato sono incluse nel file di intestazione wmcodecconst.h. I nomi delle costanti sono rispettivamente WMCFORMAT VideoInfo e \_ WMCFORMAT \_ WaveFormatEx. I codec audio possono funzionare con la **struttura WAVEFORMATEXTENSIBLE** in alcune circostanze e devono usarli in altri. Tuttavia, **DMO \_ MEDIA \_ TYPE.formattype** è impostato sullo stesso valore di **per WAVEFORMATEX.** Per altre informazioni sull'uso **di WAVEFORMATEXTENSIBLE,** vedere [Uso di High-Definition audio.](usinghighdefinitionaudio.md)

> [!Note]  
>    È necessario includere la struttura del tipo di formato usata come output del codificatore in qualsiasi contenitore usato per archiviare i dati compressi. I decodificatori richiedono la struttura del formato originale per decomprimere il contenuto. Oltre ai membri della struttura, i tipi compressi Windows audio e video multimediali richiedono informazioni aggiuntive sul formato, che vengono aggiunte alla struttura. Per altre informazioni, vedere [Working with Audio (Uso dell'audio)](workingwithaudio.md) [e Working with Video (Uso di video).](workingwithvideo.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli oggetti DMO codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
