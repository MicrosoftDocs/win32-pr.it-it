---
title: Funzionalità aggiunte in Windows Media 9.5 SDK
description: Funzionalità aggiunte in Windows Media 9.5 SDK
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Media Format SDK, funzionalità
- Windows Media Format SDK, nuove funzionalità
- Windows Media Format SDK, interfaccia per l'elaborazione specifica dell'applicazione
- Windows Media Format SDK, Accelerazione video DirectX (DXVA)
- Windows Media Format SDK, interfaccia IWMPlayerHook
- IWMPlayerHook
- Windows Media Format SDK, versioni basate su x64 di Windows
- Windows Media Format SDK, codec Windows Media Video Image
- Windows MEDIA Format SDK, codec audio
- Windows Media Format SDK,DRM 10 per dispositivi di rete
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, codec Advanced Profile
- Windows Media Format SDK, Rtf/Philips Digital Interconnect Format (S/PDIF)
- Windows MEDIA Format SDK, formati a ritardo ridotto
- Windows MEDIA Format SDK, modalità di ricerca approssimativa
- Windows MEDIA Format SDK, playlist playlist
- Windows Media Format SDK, supporto per più lingue
- Windows Media Format SDK,Windows Media Device Manager SDK
- Windows Media Format SDK, interfacce codec
- codec, Windows video multimediale
- digital rights management (DRM), protocollo di trasferimento sicuro dei dispositivi di rete
- DRM (Digital Rights Management),Protocollo di trasferimento sicuro dei dispositivi di rete
- digital rights management (DRM), licenze
- DRM (Digital Rights Management),licenze
- codecs, codec Advanced Profile
- Formato S/PDIF (Digital Interconnect Format), trasferimento o trasmissione tramite
- S/PDIF (Formato di interconnessione digitale Disambiente Disarticolata),trasferimento o trasmissione tramite
- modalità di ricerca approssimativa
- metadati, supporto per più lingue
- Windows Media Device Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbcabd2fd3ae1b1030b04c0be342bcb64678e98eef601c83570ad68a13567820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591401"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a>Funzionalità aggiunte in Windows Media 9.5 SDK

L Windows SDK di Media Format 9.5 ha introdotto nuove funzionalità per offrire maggiore sicurezza e flessibilità per i contenuti. Le modifiche seguenti sono state apportate all'SDK a partire dalla versione serie 9.

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a>Nuova interfaccia per l'elaborazione specifica dell'applicazione durante l'accelerazione video DirectX

Le applicazioni lettore che supportano l'accelerazione video DirectX possono ora implementare [**l'interfaccia IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) per eseguire l'elaborazione specifica dell'applicazione durante la decodifica DirectX VA. Il lettore chiama il metodo di callback [**IWMPLayerHook::P reDecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) prima di passare campioni video compressi al processore video per la decodifica.

> [!Note]  
> Per usare **l'interfaccia IWMPlayerHook** e l'interfaccia [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) associata, è necessario aver installato il numero di aggiornamento 888656 in Windows Media Format SDK. È possibile scaricare l'aggiornamento dal [sito Web Microsoft](https://support.microsoft.com/?id=888656).

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a>Windows Versione di Media Format SDK per le versioni basate su x64 di Windows

È disponibile una versione basata su x64 di Windows Media Format SDK. Questa documentazione si applica sia alle versioni a 32 bit che alla versione basata su x64 dell'SDK. La gestione dei diritti digitali (DRM, Digital Rights Management) non è tuttavia supportata in Windows Media Format SDK basato su x64.

## <a name="new-version-of-the-windows-media-video-image-codec"></a>Nuova versione del codec Windows video multimediale

Il codec Windows Media Video 9 Image v2 semplifica i calcoli della geometria di esempio per la panoramica e lo zoom. Il nuovo codec supporta anche diverse transizioni complesse tra le immagini.

## <a name="new-version-of-the-windows-media-audio-codecs"></a>Nuova versione dei Windows audio multimediali

L'SDK Windows Media Format 9.5 include i codec audio aggiornati seguenti:

-   Windows Audio multimediale 9.1
-   Windows Audio multimediale 9.1 Professional
-   Windows Audio multimediale 9.1 senza perdita di dati

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a>Windows Supporto del protocollo Media DRM 10 per dispositivi di rete

L Windows Media Format 9.5 SDK supporta il nuovo protocollo di trasferimento sicuro Windows Media DRM 10 per dispositivi di rete. Questo protocollo può essere usato per trasmettere il contenuto crittografato in una rete locale a un dispositivo di riproduzione, ad esempio un ricevitore video di livello superiore.

La maggior parte delle procedure usate per implementare il supporto Windows media DRM 10 per dispositivi di rete deve essere eseguita dall'applicazione. È tuttavia possibile usare i metodi di Windows Media Format SDK per fornire le funzionalità seguenti:

-   Gestire un database di dispositivi, inclusi quelli abilitati per Windows Media DRM 10 per i dispositivi di rete.
-   Convalidare i dispositivi per assicurarsi che siano sufficientemente "vicini" al client in rete per lo streaming sicuro.
-   Convertire i file protetti da DRM in Windows flussi di Media DRM 10 per dispositivi di rete.
-   Scrivere file usando dati crittografati in precedenza.

## <a name="support-for-new-drm-licenses"></a>Supporto per nuove licenze DRM

Le nuove licenze create usando Windows Media Rights Manager SDK usano i livelli di protezione dell'output (OPL) per specificare i diritti e le restrizioni per la riproduzione e la copia del contenuto. L Windows Media Format SDK fornisce il supporto per la lettura degli OPL da una licenza.

## <a name="new-video-codec"></a>Nuovo codec video

Il codec Windows Media Video 9 Advanced Profile si basa sull'alta qualità del codec Windows Media Video 9, aggiungendo al tempo stesso il supporto per la codifica interlacciata.

## <a name="spdif-output"></a>S/PDIF Output

Il contenuto codificato con uno dei codec Windows Media Audio Professional può ora essere trasferito o trasmesso usando il formato S/PDIF (Digital Interconnect Format) Di Utf/Philips.

## <a name="low-delay-audio"></a>Low-Delay audio

I codec Windows Media Audio 9.1 e Windows Media Audio 9.1 Professional ora supportano diversi formati a basso ritardo. Questi formati producono flussi audio che possono essere avviati più rapidamente, riducendo la latenza negli scenari di cambio di flusso. La latenza complessiva nelle trasmissioni live è stata migliorata anche usando formati a basso ritardo.

## <a name="approximate-seeking-mode"></a>Modalità di ricerca approssimativa

È ora possibile cercare un'ora approssimativa in un file ASF con il lettore. Questa modalità migliora le prestazioni quando si esegue una ricerca imprecisa, ad esempio quando un utente fa clic sulla barra di ricerca Windows Media Player. La ricerca approssimativa restituisce il campione multimediale per il punto di pulizia precedente anziché ricostruire il campione per l'ora esatta cercata.

## <a name="playlist-burning"></a>Playlist Disasserta

Windows Media DRM 10 supporta i diritti per la copia di file audio in Red Book CD come parte di una playlist. L Windows Media Format SDK fornisce metodi per verificare se i file in una playlist possono essere copiati.

## <a name="improved-multiple-language-support-for-metadata"></a>Miglioramento del Multiple-Language per i metadati

Nell'SDK Windows Media Format 9 Series tutti i metadati aggiunti a un file sono stati assegnati a un elenco di lingue a cui è stato assegnato l'identificatore della lingua predefinita. Ciò ha causato problemi quando i distributori di contenuti in impostazioni locali diverse hanno aggiunto alcuni metadati, perché gli utenti nelle impostazioni locali del server di distribuzione vedono solo i pochi attributi aggiunti per la lingua. Il Windows Media Format 9.5 SDK risolve questo problema non creando un elenco di lingue fino a quando non sono presenti attributi di due lingue nel file. A questo punto, tutti i metadati sono associati alle impostazioni locali della seconda lingua, che diventa quindi l'impostazione predefinita. In questo modo, un distributore di contenuti può mantenere intatti tutti i metadati originali per un file, ad esempio titolo e autore, aggiungendo alcuni attributi pertinenti alle impostazioni locali.

## <a name="windows-media-device-manager-sdk-included-in-installation"></a>Windows Media Device Manager SDK incluso nell'installazione

Il pacchetto di installazione per Windows Media Format 9.5 SDK installa Windows Media Device Manager SDK. La documentazione per Windows Media Device Manager SDK è disponibile nella cartella C: \\ WMSDK \\ WMFSDK95 \\ WMDM docs (la cartella sarà diversa se non si installa Windows Media Format SDK nella cartella \\ predefinita).

## <a name="codec-interface-documentation"></a>Documentazione dell'interfaccia codec

Questa documentazione include informazioni sull'uso Windows codec audio e video multimediali all'esterno di Windows Media Format SDK. Questa documentazione è stata originariamente rilasciata come parte di un download dalla Sviluppatore Microsoft rete. Le applicazioni di esempio che illustrano l'uso diretto del codec DMO sono incluse nell'installazione dell'SDK Windows Media Format insieme alle intestazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




