---
description: Panoramica di DXVA 2 e relativa relazione con DXVA 1.
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: Informazioni su DXVA 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d6ab595be1f167f777e50001c8d31658dc697866c8d11db3865e66e87508ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606821"
---
# <a name="about-dxva-20"></a>Informazioni su DXVA 2.0

L'accelerazione video DirectX (DXVA) è un'API e un'interfaccia DDI corrispondente per l'uso dell'accelerazione hardware per velocizzare l'elaborazione video. I codec software e i processori video software possono usare DXVA per eseguire l'offload di determinate operazioni a elevato utilizzo di CPU nella GPU. Ad esempio, un decodificatore software può eseguire l'offload della trasformazione del coseno discreto inverso (iDCT) alla GPU.

In DXVA alcune operazioni di decodifica vengono implementate dal driver hardware grafico. Questo set di funzionalità è il termine *acceleratore*. Altre operazioni di decodifica vengono implementate dal software applicativo in modalità utente, denominato *decodificatore host* o *decodificatore software.* I termini *decodificatore host* e *decodificatore software* sono equivalenti. L'elaborazione eseguita dall'acceleratore è detta *elaborazione off-host.* In genere l'acceleratore usa la GPU per velocizzare alcune operazioni. Ogni volta che l'acceleratore esegue un'operazione di decodifica, il decodificatore host deve comunicare ai buffer dell'acceleratore contenenti le informazioni necessarie per eseguire l'operazione

L'API DXVA 2 richiede Windows Vista o versioni successive. L'API DXVA 1 è ancora supportata in Windows Vista per la compatibilità con le versioni precedenti. Viene fornito un livello di emulazione che esegue la conversione tra una delle due versioni dell'API e la versione opposta dell'interfaccia DDI:

-   Se il driver di grafica è conforme Windows Display Driver Model (WDDM), le chiamate API DXVA 1 vengono convertite in chiamate DXVA 2 DDI.
-   Se i driver di grafica utilizzano la versione precedente di Windows XP Display Driver Model (XPDM), le chiamate API DXVA 2 vengono convertite in chiamate DXVA 1 DDI.

La tabella seguente illustra i requisiti del sistema operativo e i renderer video supportati per ogni versione dell'API DXVA.



| Versione API | Requisiti          | Supporto del renderer video                        |
|-------------|-----------------------|-----------------------------------------------|
| DXVA 1      | Windows 2000 o versione successiva | Overlay Mixer, VMR-7, VMR-9 (solo DirectShow) |
| DXVA 2      | Windows Vista         | EVR (DirectShow e Media Foundation)         |



 

In DXVA 1 il decodificatore software deve accedere all'API tramite il renderer video. Non è possibile usare l'API DXVA 1 senza chiamare il renderer video. Questa limitazione è stata rimossa con DXVA 2. Usando DXVA 2, il decodificatore host (o qualsiasi applicazione) può accedere direttamente all'API tramite [**l'interfaccia IDirectXVideoDecoderService.**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)

La documentazione di DXVA 1 descrive le strutture di decodifica usate per gli standard video seguenti:

-   ITU-T Rec. H.261
-   ITU-T Rec. H.263
-   Video MPEG-1
-   Video sul profilo principale MPEG-2

Le specifiche seguenti definiscono le estensioni DXVA per altri standard video:

-   [Specifica DXVA per la decodifica H.264/AVC](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [Specifica DXVA per H.264/MPEG-4 AVC Multiview Video Coding (MVC), incluso il profilo Stereo High](https://www.microsoft.com/download/details.aspx?id=25200)
-   [Specifica DXVA per la decodifica video MPEG-1 VLD e MPEG-1/MPEG-2 combinata.](https://www.microsoft.com/download/details.aspx?id=9374)
-   [Specifica DXVA per Off-Host VLD per la decodifica video MPEG-4 parte 2](https://www.microsoft.com/download/details.aspx?id=21100)
-   [Specifica DXVA per Windows Media Video® v8, v9 e decodifica vA (incluso SMPTE 421M "VC-1")](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [Specifica DXVA (DirectX Video Acceleration) per H.264/MPEG-4 Scalable Video Coding (SVC) Off-Host decodifica in modalità VLD](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [Specifica dell'accelerazione video DirectX per la codifica video VP8 e VP9](https://www.microsoft.com/download/details.aspx?id=49188)

DXVA 1 e DXVA 2 usano le stesse strutture di dati per la decodifica. Tuttavia, la procedura per la configurazione della sessione di decodifica è stata modificata. DXVA 1 usa un meccanismo di "probe e blocco", in cui il decodificatore host può testare varie configurazioni prima di impostare la configurazione desiderata sull'acceleratore. In DXVA 2 l'acceleratore restituisce un elenco di configurazioni supportate e il decodificatore host ne seleziona una dall'elenco. I dettagli sono disponibili nelle sezioni seguenti:

-   [Supporto di DXVA 2.0 in DirectShow](supporting-dxva-2-0-in-directshow.md)
-   [Supporto di DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Specifica DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
