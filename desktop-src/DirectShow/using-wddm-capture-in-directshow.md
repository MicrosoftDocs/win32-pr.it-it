---
description: Uso di WDDM Capture in DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Uso di WDDM Capture in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314381"
---
# <a name="using-wddm-capture-in-directshow"></a>Uso di WDDM Capture in DirectShow

Questo argomento si applica a Windows Vista e versioni successive.

Alcune schede video hanno funzionalità di acquisizione video integrate. In queste schede i frame video acquisiti vengono inseriti in memoria video (VRAM). Prima di Windows Vista, non era disponibile un meccanismo standard per l'elaborazione dei frame mentre rimanevano in VRAM. Al contrario, i dati devono essere copiati nella memoria di sistema, elaborati e quindi copiati di nuovo in VRAM per la visualizzazione. In Windows Vista, DirectShow supporta ora un meccanismo per mantenere i frame video in VRAM nell'intera pipeline di elaborazione, dall'acquisizione alla visualizzazione.

Il filtro KsProxy determina se il driver supporta la funzionalità di acquisizione della superficie VRAM eseguendo una query sul driver per la \_ proprietà della superficie di acquisizione preferita di KSPROPERTY \_ \_ . Questa proprietà è documentata nella documentazione di Windows Driver Kit. Se il driver supporta la funzionalità di acquisizione della superficie VRAM, KsProxy alloca un tipo speciale di esempio multimediale che include un puntatore a una superficie Direct3D.

Successivamente, KsProxy determina se il filtro downstream supporta l'accelerazione video DirectX (DXVA) 2,0, come indicato di seguito:

1.  KsProxy esegue una query sul pin di input downstream per l'interfaccia **IMFGetService** .
2.  Se il pin espone **IMFGetService**, ksproxy chiama **IMFGetService:: GetService** per l'interfaccia **IDirect3DDeviceManager** . Il servizio identier è il \_ servizio di accelerazione del video \_ \_ .

Entrambe le interfacce sono documentate nella documentazione di Media Foundation SDK.

Se il filtro downstream non supporta DXVA 2,0, KsProxy alloca un buffer di memoria di sistema aggiuntivo. Usa questo buffer per copiare i fotogrammi video da VRAM a memoria di sistema. Il metodo [**IMediaSample:: Getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) dell'esempio multimediale restituisce un puntatore a questo buffer di memoria di sistema.

Tuttavia, se il filtro downstream supporta DXVA 2,0, KsProxy non alloca un buffer di memoria di sistema. In tal caso, il metodo **Getpointer** restituisce E \_ NOTIMPL. Al contrario, si prevede che il filtro downstream acceda direttamente alla superficie Direct3D dell'esempio. Esistono due modi per il filtro downstream per ottenere un puntatore alla superficie, entrambi equivalenti:

-   Eseguire una query sull'esempio per l'interfaccia **IMFGetService** e chiamare **GetService** per l'interfaccia **IDirect3DSurface9** . L'identificatore del servizio è \_ il \_ servizio buffer di.
-   Eseguire una query sull'esempio per l'interfaccia [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) e chiamare [**IMediaSample2Config:: GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti sull'acquisizione avanzata](advanced-capture-topics.md)
</dt> </dl>

 

 



