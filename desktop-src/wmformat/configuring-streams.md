---
title: Configurazione di Flussi
description: Configurazione di Flussi
ms.assetid: d119362f-e23c-4985-aff5-8c084106df30
keywords:
- Windows MEDIA Format SDK, flussi
- profili, flussi
- flussi, configurazione
- codec, configurazione di flussi
- profili,interfaccia IWMStreamConfig
- flussi,interfaccia IWMStreamConfig
- IWMStreamConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d55db0d02c8eae3ddd3ec780f5d6470d87628a6f7b12feceb5faa413b2e4546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199317"
---
# <a name="configuring-streams"></a>Configurazione di Flussi

L'unico elemento necessario in un profilo è almeno un flusso. Le altre opzioni consentono di accedere a funzionalità più avanzate, ma con il minimo di un flusso è possibile creare un file ASF. È essenziale comprendere come configurare i flussi prima di creare profili complessi.

Ai fini dei profili, i flussi possono essere suddivisi in due tipi: quelli compressi con codec multimediali Windows e flussi arbitrari che non vengono elaborati con codec. I flussi audio e video sono i tipi che usano i codec Windows media. Naturalmente, i flussi possono contenere audio o video compressi con un codec di terze parti, ma il processo di configurazione di tale flusso è un caso speciale. Per altre informazioni, vedere [Per creare file ASF usando codec di terze parti.](to-create-asf-files-using-third-party-codecs.md)

L'elenco seguente riepiloga il processo di configurazione di un flusso.

1.  Ottenere un oggetto di configurazione del flusso per il flusso.
    -   Se si crea un flusso usando uno dei codec Windows Media, è necessario ottenere l'oggetto di configurazione del flusso come formato codec usando i metodi di [**IWMCodecInfo3.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)
    -   Se il flusso è un tipo arbitrario, ottenere un oggetto di configurazione del flusso vuoto usando [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).
2.  Configurare il flusso in base alle proprie esigenze.
    -   Flussi di tutti i tipi devono essere assegnati un nome, un nome di connessione e un numero di flusso.
    -   Flussi usare Windows codec multimediali devono essere modificati solo in modi predefiniti dal formato del codec. Per i flussi audio, è necessario modificare solo le impostazioni della velocità in bit variabile (VBR) per VBR a due passi. I flussi video devono essere configurati con le proprietà dei fotogrammi desiderate.
    -   I flussi arbitrari hanno requisiti di configurazione diversi in base al tipo. Tutti richiedono una velocità in bit e una finestra del buffer.
3.  Aggiungere il flusso al profilo chiamando [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream).

Tutti i flussi vengono definiti usando oggetti di configurazione del flusso. L'interfaccia principale per un oggetto di configurazione del flusso [**è IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig), che fornisce metodi per impostare le impostazioni di base di un flusso, ad esempio il numero di flusso, la velocità in bit e così via. **IWMStreamConfig** viene ereditato dalle interfacce più nuove, [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) e [**IWMStreamConfig3.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3) Come per tutte le revisioni dell'interfaccia numerate, è sempre necessario recuperare la versione più recente usando il **metodo QueryInterface.**

La maggior parte delle impostazioni in un flusso è accessibile [**tramite IWMMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) Queste impostazioni sono incapsulate in una [**struttura WM \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Per audio e video, la **struttura WM \_ MEDIA \_ TYPE** punta a un'altra struttura con altre informazioni specifiche del tipo di supporto. Questa struttura secondaria è in [**genere WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) per l'audio e [**WMVIDEOINFOHEADER per**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) il video. Inoltre, i flussi video hanno una struttura terziaria, **BITMAPINFOHEADER,** che descrive le caratteristiche di un singolo fotogramma di video. **BITMAPINFOHEADER** è una struttura comune ed è disponibile nella sezione Graphics Device Interface (GDI) di Platform SDK.

Le sezioni seguenti descrivono come configurare i flussi.



| Sezione                                                                                                          | Descrizione                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configurazione comune a tutti Flussi](configuration-common-to-all-streams.md)                                   | Descrive la configurazione di flusso di base comune a tutti i tipi di flussi.                                                                                        |
| [Recupero delle informazioni di configurazione del flusso dai codec](getting-stream-configuration-information-from-codecs.md) | Viene descritto come ottenere informazioni di configurazione del flusso dai codec per garantire la corretta configurazione dei flussi usando Windows codec audio e video multimediali. |
| [Configurazione dei dispositivi Flussi](configuring-audio-streams.md)                                                       | Descrive come configurare i flussi audio.                                                                                                                       |
| [Configurazione di video Flussi](configuring-video-streams.md)                                                       | Descrive come configurare i flussi video.                                                                                                                       |
| [Configurazione dei Flussi video per la ricerca delle prestazioni](configuring-video-streams-for-seeking-performance.md)       | Descrive come configurare i flussi video per i quali è importante una ricerca efficiente.                                                                              |
| [Configurazione dell'acquisizione schermo Flussi](configuring-screen-capture-streams.md)                                     | Descrive come configurare i flussi video per l'acquisizione dello schermo.                                                                                                    |
| [Configurazione del Flussi](configuring-image-streams.md)                                                       | Viene descritto come configurare i flussi di immagini.                                                                                                                       |
| [Uso di audio e video non compressi Flussi](using-uncompressed-audio-and-video-streams.md)                     | Descrive come configurare un flusso audio o video non compresso.                                                                                                  |
| [Configurazione di tipi di flusso arbitrari](configuring-arbitrary-stream-types.md)                                     | Viene descritto come configurare i flussi per l'uso dei tipi di flusso arbitrari predefiniti.                                                                                |
| [Configurazione di VBR Flussi](configuring-vbr-streams.md)                                                           | Viene descritto come configurare i flussi per l'uso della codifica a velocità in bit variabile (VBR).                                                                                     |
| [Configurazione di estensioni delle unità dati](configuring-data-unit-extensions.md)                                         | Viene descritto come configurare un flusso in modo che le estensioni delle unità dati possano essere collegate quando viene scritto il file.                                                      |
| [Riutilizzo delle configurazioni dei flussi](reusing-stream-configurations.md)                                               | Descrive i modi in cui è possibile usare gli oggetti di configurazione del flusso da profili esistenti per creare nuovi profili.                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Input, Flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Uso dei profili**](working-with-profiles.md)
</dt> </dl>

 

 