---
description: Utilizzo dei tipi di supporto DMO
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Utilizzo dei tipi di supporto DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968877"
---
# <a name="working-with-dmo-media-types"></a>Utilizzo dei tipi di supporto DMO

I tipi di supporto di input e di output utilizzati dal codec DMOs vengono definiti utilizzando la struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Questa struttura è identica a entrambi [**i \_ \_ tipi di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), che è definito in Windows Media Format SDK e il [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type), definito in Microsoft DirectShow®. A seconda dell'applicazione, è possibile utilizzare le variabili definite come uno di questi tre tipi. È possibile eseguire il cast di un puntatore a una delle strutture del tipo di supporto come un altro. Ad esempio:


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



I tipi di formato usati dai codec sono generalmente limitati a quelli descritti dalle strutture **VIDEOINFOHEADER** e **WAVEFORMATEX** . Per praticità, le costanti per questi tipi di formato sono incluse nel file di intestazione wmcodecconst. h. I nomi delle costanti sono \_ rispettivamente WMCFORMAT videoinfo e WMCFORMAT \_ WAVEFORMATEX. In alcune circostanze, i codec audio possono funzionare con la struttura **WAVEFORMATEXTENSIBLE** e devono essere usati in altri. Tuttavia, **DMO \_ media \_ Type. formatType** è impostato sullo stesso valore di **WAVEFORMATEX**. Per altre informazioni sull'uso di **WAVEFORMATEXTENSIBLE**, vedere [uso di High-Definition audio](usinghighdefinitionaudio.md).

> [!Note]  
>    È necessario includere la struttura del tipo di formato usata come output del codificatore in qualsiasi contenitore usato per archiviare i dati compressi. I decodificatori richiedono la struttura del formato originale per decomprimere il contenuto. Oltre ai membri della struttura, i tipi compressi Windows Media Audio e video richiedono informazioni aggiuntive sul formato, che vengono aggiunte alla struttura. Per ulteriori informazioni, vedere [utilizzo di audio](workingwithaudio.md) e [utilizzo di video](workingwithvideo.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
