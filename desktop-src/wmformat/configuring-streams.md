---
title: Configurazione di flussi
description: Configurazione di flussi
ms.assetid: d119362f-e23c-4985-aff5-8c084106df30
keywords:
- Windows Media Format SDK, flussi
- profili, flussi
- flussi, configurazione
- codec, configurazione di flussi
- profili, interfaccia IWMStreamConfig
- flussi, interfaccia IWMStreamConfig
- IWMStreamConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc159fbd5390eb430e035db676685153d0cf174
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473131"
---
# <a name="configuring-streams"></a>Configurazione di flussi

L'unica cosa che è necessario in un profilo è almeno un flusso. Le altre opzioni forniscono l'accesso a funzionalità più avanzate, ma con almeno un flusso è possibile creare un file ASF. È essenziale comprendere come configurare i flussi prima di creare profili complessi.

Ai fini dei profili, i flussi possono essere divisi in due tipi: quelli compressi con codec Windows Media e flussi arbitrari che non vengono elaborati con alcun codec. Flussi audio e video sono i tipi che usano i codec Windows Media. Naturalmente, i flussi possono contenere audio o video compressi con un codec di terze parti, ma il processo di configurazione di tale flusso è un caso particolare. Per ulteriori informazioni, vedere [per creare file ASF con codec di terze parti](to-create-asf-files-using-third-party-codecs.md).

Nell'elenco seguente viene riepilogato il processo di configurazione di un flusso.

1.  Ottenere un oggetto di configurazione del flusso per il flusso.
    -   Se si sta creando un flusso usando uno dei codec Windows Media, è necessario ottenere l'oggetto di configurazione del flusso come formato di codec usando i metodi di [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3).
    -   Se il flusso è di tipo arbitrario, ottenere un oggetto di configurazione del flusso vuoto usando [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).
2.  Configurare il flusso per soddisfare le proprie esigenze.
    -   Ai flussi di tutti i tipi devono essere assegnati un nome, un nome di connessione e un numero di flusso.
    -   I flussi che usano codec Windows Media devono essere modificati solo in modi predefiniti dal formato di codec. Per i flussi audio, è necessario modificare solo le impostazioni della velocità in bit variabile (VBR) per VBR a due passaggi. È necessario configurare i flussi video con le proprietà del frame desiderate.
    -   I flussi arbitrari hanno requisiti di configurazione diversi per tipo. Tutti richiedono una velocità in bit e una finestra del buffer.
3.  Aggiungere il flusso al profilo chiamando [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream).

Tutti i flussi vengono definiti tramite oggetti di configurazione del flusso. L'interfaccia principale per un oggetto di configurazione del flusso è [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig), che fornisce metodi per l'impostazione delle impostazioni di base di un flusso, ad esempio il numero di flusso, la velocità in bit e così via. **IWMStreamConfig** viene ereditato dalle interfacce più recenti, [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) e [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3). Come per tutte le revisioni dell'interfaccia numerate, è necessario recuperare sempre la versione più recente usando il metodo **QueryInterface** .

Per accedere alla maggior parte delle impostazioni in un flusso, è possibile usare [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops). Queste impostazioni sono incapsulate in una struttura di [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Per audio e video, la struttura del **\_ \_ tipo di supporto WM** punta a un'altra struttura con ulteriori informazioni specifiche per il tipo di supporto. Questa struttura secondaria è in genere [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) per audio e [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) per il video. Inoltre, i flussi video hanno una struttura terziaria, **BITMAPINFOHEADER**, che descrive le caratteristiche di un singolo frame di video. **BITMAPINFOHEADER** è una struttura comune e si trova nella sezione Graphics Device Interface (GDI) di Platform SDK.

Le sezioni seguenti descrivono come configurare i flussi.



| Sezione                                                                                                          | Descrizione                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configurazione comune a tutti i flussi](configuration-common-to-all-streams.md)                                   | Descrive la configurazione del flusso di base comune a tutti i tipi di flussi.                                                                                        |
| [Recupero delle informazioni di configurazione dei flussi dai codec](getting-stream-configuration-information-from-codecs.md) | Viene descritto come ottenere informazioni sulla configurazione del flusso dai codec per garantire la corretta configurazione dei flussi usando i codec Windows Media Audio e video. |
| [Configurazione di flussi audio](configuring-audio-streams.md)                                                       | Viene descritto come configurare i flussi audio.                                                                                                                       |
| [Configurazione dei flussi video](configuring-video-streams.md)                                                       | Viene descritto come configurare i flussi video.                                                                                                                       |
| [Configurazione dei flussi video per le prestazioni di ricerca](configuring-video-streams-for-seeking-performance.md)       | Viene descritto come configurare i flussi video per i quali è importante la ricerca efficiente.                                                                              |
| [Configurazione di flussi di acquisizione schermo](configuring-screen-capture-streams.md)                                     | Viene descritto come configurare i flussi video per l'acquisizione schermo.                                                                                                    |
| [Configurazione di flussi di immagini](configuring-image-streams.md)                                                       | Viene descritto come configurare i flussi di immagine.                                                                                                                       |
| [Uso di flussi audio e video non compressi](using-uncompressed-audio-and-video-streams.md)                     | Viene descritto come configurare un flusso audio o video non compresso.                                                                                                  |
| [Configurazione di tipi di flusso arbitrari](configuring-arbitrary-stream-types.md)                                     | Viene descritto come configurare i flussi per l'utilizzo dei tipi di flusso arbitrari predefiniti.                                                                                |
| [Configurazione di flussi VBR](configuring-vbr-streams.md)                                                           | Viene descritto come configurare i flussi per l'utilizzo della codifica con velocità in bit variabile (VBR).                                                                                     |
| [Configurazione di estensioni delle unità dati](configuring-data-unit-extensions.md)                                         | Viene descritto come configurare un flusso in modo che sia possibile collegare le estensioni dell'unità dati quando viene scritto il file.                                                      |
| [Riutilizzo delle configurazioni di flusso](reusing-stream-configurations.md)                                               | Vengono descritte le modalità con cui è possibile utilizzare oggetti di configurazione di flusso da profili esistenti per creare nuovi profili.                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Input, flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Utilizzo dei profili**](working-with-profiles.md)
</dt> </dl>

 

 