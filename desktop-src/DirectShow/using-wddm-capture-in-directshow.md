---
description: Uso dell'acquisizione WDDM in DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Uso dell'acquisizione WDDM in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e0a442c6929ef2435b05268035bb0b39b196a958440cd7ce5cfe44ea4b4c55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903591"
---
# <a name="using-wddm-capture-in-directshow"></a>Uso dell'acquisizione WDDM in DirectShow

Questo argomento si applica a Windows Vista e versioni successive.

Alcune schede video hanno funzionalità integrate di acquisizione video. In queste schede i fotogrammi video acquisiti vengono inseriti nella memoria video (VRAM). Prima di Windows Vista, non esisteva un meccanismo standard per l'elaborazione dei fotogrammi mentre erano rimasti nella VRAM. I dati dovevano invece essere copiati nella memoria di sistema, elaborati e quindi copiati di nuovo nella VRAM per la visualizzazione. In Windows Vista, DirectShow ora supporta un meccanismo per mantenere i fotogrammi video nella VRAM in tutta la pipeline di elaborazione, dall'acquisizione alla visualizzazione.

Il filtro KsProxy determina se il driver supporta l'acquisizione della superficie di VRAM tramite query sul driver per la proprietà KSPROPERTY \_ PREFERRED \_ CAPTURE \_ SURFACE. Questa proprietà è documentata nella documentazione di Windows Driver Kit. Se il driver supporta l'acquisizione della superficie della VRAM, KsProxy alloca un tipo speciale di campione di supporti che contiene un puntatore a una superficie Direct3D.

Successivamente, KsProxy determina se il filtro downstream supporta DirectX Video Acceleration (DXVA) 2.0, come indicato di seguito:

1.  KsProxy esegue una query sul pin di input downstream per **l'interfaccia IMFGetService.**
2.  Se il pin espone **IMFGetService,** KsProxy chiama **IMFGetService::GetService** per l'interfaccia **IDirect3DDeviceManager.** L'identier del servizio è MR \_ VIDEO \_ ACCELERATION \_ SERVICE.

Entrambe queste interfacce sono documentate nella documentazione Media Foundation SDK.

Se il filtro downstream non supporta DXVA 2.0, KsProxy alloca un buffer di memoria di sistema aggiuntivo. Usa questo buffer per copiare i fotogrammi video dalla VRAM alla memoria di sistema. Il metodo [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) dell'esempio multimediale restituisce un puntatore a questo buffer di memoria di sistema.

Tuttavia, se il filtro downstream supporta DXVA 2.0, KsProxy non alloca un buffer di memoria di sistema. In tal caso, il **metodo GetPointer** restituisce E \_ NOTIMPL. È invece previsto che il filtro downstream accedono direttamente alla superficie Direct3D dell'esempio. Esistono due modi per ottenere un puntatore alla superficie dal filtro downstream, entrambi equivalenti:

-   Eseguire una query **sull'esempio per l'interfaccia IMFGetService** e **chiamare GetService** per **l'interfaccia IDirect3DSurface9.** L'identificatore del servizio è MR \_ BUFFER \_ SERVICE.
-   Eseguire una query [**sull'esempio per l'interfaccia IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) e chiamare [**IMediaSample2Config::GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti di acquisizione avanzata](advanced-capture-topics.md)
</dt> </dl>

 

 



