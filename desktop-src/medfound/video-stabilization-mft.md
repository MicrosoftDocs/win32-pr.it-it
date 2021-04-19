---
description: La stabilizzazione video MFT è una trasformazione Microsoft Media Foundation (MFT) che esegue la stabilizzazione delle immagini in un flusso video.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: Stabilizzazione video MFT (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332596"
---
# <a name="video-stabilization-mft"></a>Stabilizzazione video MFT

La stabilizzazione video MFT è una trasformazione Microsoft Media Foundation (MFT) che esegue la stabilizzazione delle immagini in un flusso video.

## <a name="clsid"></a>CLSID

\_CMSVIDEODSPMFT CLSID

## <a name="interfaces"></a>Interfacce

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMediaExtension**](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a>Formati di input

Il tipo di supporto di input e le combinazioni di sottotipi accettati dalla MFT per la stabilizzazione video per i video non compressi sono:

-   **VIDEO di MEDIATYPE \_**
-   **\_NV12 MEDIASUBTYPE**
-   **\_YUY2 MEDIASUBTYPE**

## <a name="output-formats"></a>Formati di output

Il tipo di supporto di output e le combinazioni di sottotipi accettati dalla MFT per la stabilizzazione video sono:

-   **VIDEO di MEDIATYPE \_**
-   **\_NV12 MEDIASUBTYPE**

Il tipo di supporto di input deve essere impostato prima del tipo di supporto di output. Nella maggior parte dei casi, il supporto per il formato limitato non è un problema perché la pipeline inserisce automaticamente le conversioni dei colori necessarie.

Il componente MFT per la stabilizzazione video è in grado di modificare il formato dinamico in caso di modifica dell'input. Quando le dimensioni dell'immagine di input cambiano o il sottotipo viene modificato, viene attivata una modifica del formato dinamico nel flusso di output.

La stabilizzazione video MFT effettuerà la conversione dei colori nei casi seguenti:

-   Quando il formato di input è **MEDIASUBTYPE \_ YUY2**.
-   Quando viene utilizzata la modalità di compatibilità Microsoft DirectX 9,0.

### <a name="attributes"></a>Attributi

Gli attributi seguenti sono supportati dalla stabilizzazione video MFT tramite l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

-   L'attributo [MF \_ VIDEODSP \_ mode](mf-videodsp-mode.md) imposta la stabilizzazione video MFT in modalità di stabilizzazione o pass-through. L'applicazione deve chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) sul tipo GUID **MF \_ VIDEODSP \_** con un numero intero corrispondente a uno dei valori validi seguenti: **\_ stabilizzazione MFVideoDSPMode** = 4, **MFVideoDSPMode \_ PassThrough** = 1. \_ \_ La modalità MF VIDEODSP può essere modificata in qualsiasi momento durante la riproduzione. Questo comporta una modifica della modalità dinamica. L'output passerà a stabilizzato o pass-through dopo 16 o 2 frame, a seconda della modalità di latenza, dopo la modifica dell'attributo.
-   Con l'attributo [MF \_ bassa \_ latenza](mf-low-latency.md) , la stabilizzazione del video è in modalità a bassa latenza o alta qualità. L'applicazione deve chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) sul GUID **MF \_ low \_ latenza** con un numero intero corrispondente a uno dei valori validi seguenti: latenza bassa = 1 alta qualità = 0
-   L'attributo [MF \_ sa \_ d3d11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) viene usato dalla pipeline per specificare i flag di associazione d3d11 per la creazione degli esempi di output con. Qualsiasi combinazione di valori dall'enumerazione [**del \_ \_ flag di binding d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) è valida.
-   Il numero di campioni di **\_ \_ \_ output \_ \_ minimo dell'attributo MF SA** viene usato dalla pipeline per specificare il numero minimo di campioni che questo componente deve supportare nell'output.
-   L'attributo [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) viene impostato su ogni campione prodotto dalla stabilizzazione per indicare l' [effettiva \_ \_ modalità MF VIDEODSP](mf-videodsp-mode.md) applicata a tale campione (indipendentemente dal fatto che l'esempio sia stato stabilizzato). In determinate condizioni, è possibile che gli esempi non siano stabilizzati (a causa del carico elevato del sistema o delle richieste da parte dell'utente). Questo attributo ha gli stessi valori dell'attributo della \_ modalità MF VIDEODSP \_ (**\_ stabilizzazione MFVideoDSPMode** e **\_ PassThrough MFVideoDSPMode**). Per ottenere il valore di questa applicazione di attributo, è necessario chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) SETVALUE sul GUID **MFSampleExtension \_ VideoDSPMode**.

## <a name="remarks"></a>Commenti

È possibile creare un'istanza del DSP per la stabilizzazione video in uno dei modi seguenti:

-   Chiamando [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). La stabilizzazione del video DSP è registrata nella categoria dell' **\_ \_ \_ effetto video della categoria MFT** .
-   Chiamando la funzione COM **CoCreateInstance** passando il CLSID CLSID **\_ CMSVideoDSPMFT**. Per usare questo metodo, è necessario includere wmcodecdsp. h e il collegamento a wmcodecdspuuid. lib.

Inoltre, la stabilizzazione video supporta la creazione di istanze utilizzando Windows Runtime come estensione per Windows Media. Viene definito in [**Windows. Media. VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)e il nome completo è "Windows. Media. VideoEffects. VideoStabilization".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnale digitale](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
