---
description: Panoramica di DXVA 2 e relativa relazione con DXVA 1.
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: Informazioni su DXVA 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f622c863f433be44bbce6460024ffb06bb1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307523"
---
# <a name="about-dxva-20"></a>Informazioni su DXVA 2,0

DirectX Video Acceleration (DXVA) è un'API e un DDI corrispondente per l'uso dell'accelerazione hardware per velocizzare l'elaborazione dei video. I codec software e i processori video software possono usare DXVA per eseguire l'offload di alcune operazioni con utilizzo intensivo della CPU nella GPU. Un decodificatore software, ad esempio, può eseguire l'offload della trasformazione iDCT (discrete coseno) inversa nella GPU.

In DXVA alcune operazioni di decodifica sono implementate dal driver hardware grafico. Questo set di funzionalità viene definito tasto di *scelta rapida*. Altre operazioni di decodifica sono implementate dal software dell'applicazione in modalità utente, denominato *decoder host* o decodificatore *software*. I termini decodificatore *host* e *software decodificatore* sono equivalenti. L'elaborazione eseguita dall'acceleratore viene chiamata *elaborazione fuori host*. In genere l'acceleratore usa la GPU per velocizzare alcune operazioni. Ogni volta che l'acceleratore esegue un'operazione di decodifica, il decodificatore host deve fornire i buffer dell'acceleratore contenenti le informazioni necessarie per eseguire l'operazione

L'API DXVA 2 richiede Windows Vista o versione successiva. L'API DXVA 1 è ancora supportata in Windows Vista per la compatibilità con le versioni precedenti. Viene fornito un livello di emulazione che esegue la conversione tra una versione dell'API e la versione opposta di DDI:

-   Se il driver di grafica è conforme a Windows Display Driver Model (WDDM), le chiamate API DXVA 1 vengono convertite in chiamate DDI DXVA 2.
-   Se i driver della grafica utilizzano il modello di driver di visualizzazione di Windows XP precedente (XPDM), le chiamate API DXVA 2 vengono convertite in chiamate DDI DXVA 1.

La tabella seguente illustra i requisiti del sistema operativo e i renderer video supportati per ogni versione dell'API DXVA.



| Versione API | Requisiti          | Supporto renderer video                        |
|-------------|-----------------------|-----------------------------------------------|
| DXVA 1      | Windows 2000 o versione successiva | Mixer overlay, VMR-7, VMR-9 (solo DirectShow) |
| DXVA 2      | Windows Vista         | EVR (DirectShow e Media Foundation)         |



 

In DXVA 1, il decodificatore software deve accedere all'API tramite il renderer video. Non è possibile usare l'API DXVA 1 senza chiamare il renderer video. Questa limitazione è stata rimossa con DXVA 2. Usando DXVA 2, il decodificatore host (o qualsiasi applicazione) può accedere direttamente all'API tramite l'interfaccia [**IDirectXVideoDecoderService**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .

La documentazione di DXVA 1 descrive le strutture di decodifica usate per gli standard video seguenti:

-   ITU-T REC. H. 261
-   ITU-T REC. H. 263
-   Video MPEG-1
-   Video del profilo principale MPEG-2

Le specifiche seguenti definiscono le estensioni DXVA per altri standard video:

-   [Specifica DXVA per la decodifica H. 264/AVC](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [Specifica DXVA per la codifica video (MVC) H. 264/MPEG-4 AVC, incluso il profilo High stereo](https://www.microsoft.com/download/details.aspx?id=25200)
-   [Specifica DXVA per MPEG-1 VLD e decodifica video combinata MPEG-1/MPEG-2 VLD](https://www.microsoft.com/download/details.aspx?id=9374).
-   [Specifica DXVA per la decodifica del video MPEG-4 Part 2 in modalità VLD Off-Host](https://www.microsoft.com/download/details.aspx?id=21100)
-   [Specifica DXVA per la decodifica Windows Media Video® V8, V9 e vA (incluso SMPTE 421M "VC-1")](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [Specifica DXVA (DirectX Video Acceleration) per la codifica video scalabile H. 264/MPEG-4 (SVC) Off-Host la decodifica in modalità VLD](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [Specifica di accelerazione video DirectX per la codifica video VP8 e VP9](https://www.microsoft.com/download/details.aspx?id=49188)

DXVA 1 e DXVA 2 usano le stesse strutture di dati per la decodifica. Tuttavia, la procedura per la configurazione della sessione di decodifica è cambiata. DXVA 1 usa un meccanismo di probe e blocco, in cui il decodificatore host può testare diverse configurazioni prima di impostare la configurazione desiderata nell'acceleratore. In DXVA 2 il tasto di scelta rapida restituisce un elenco di configurazioni supportate e il decodificatore host ne seleziona uno dall'elenco. I dettagli sono forniti nelle sezioni seguenti:

-   [Supporto di DXVA 2,0 in DirectShow](supporting-dxva-2-0-in-directshow.md)
-   [Supporto di DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Specifica DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
