---
title: Funzionalità aggiunte in Windows Media 9,5 SDK
description: Funzionalità aggiunte in Windows Media 9,5 SDK
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Media Format SDK, funzionalità
- Windows Media Format SDK, nuove funzionalità
- Windows Media Format SDK, interfaccia per l'elaborazione specifica dell'applicazione
- Windows Media Format SDK, accelerazione video DirectX (DXVA)
- Windows Media Format SDK, interfaccia IWMPlayerHook
- IWMPlayerHook
- Windows Media Format SDK, versioni basate su x64 di Windows
- Windows Media Format SDK, Windows Media Video image codec
- Windows Media Format SDK, codec audio
- Windows Media Format SDK, DRM 10 per i dispositivi di rete
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, Advanced Profile codec
- Windows Media Format SDK, formato di interconnessione digitale Sony/Philips (S/PDIF)
- Windows Media Format SDK, formati a basso ritardo
- Windows Media Format SDK, modalità di ricerca approssimativa
- Windows Media Format SDK, Burning delle playlist
- Windows Media Format SDK, supporto per più lingue
- Windows Media Format SDK, Windows Media Gestione dispositivi SDK
- Windows Media Format SDK, interfacce codec
- codec, immagine Windows Media Video
- Digital Rights Management (DRM), dispositivi di rete Secure Transfer Protocol
- DRM (Digital Rights Management), dispositivi di rete Secure Transfer Protocol
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- codec, Advanced Profile codec
- Formato di interconnessione digitale Sony/Philips (S/PDIF), trasferimento o trasmissione tramite
- S/PDIF (formato di interconnessione digitale Sony/Philips), trasferimento o trasmissione tramite
- modalità di ricerca approssimativa
- metadati, supporto per più linguaggi
- Windows Media Gestione dispositivi SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117411"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a>Funzionalità aggiunte in Windows Media 9,5 SDK

Windows Media Format 9,5 SDK ha introdotto nuove funzionalità per offrire maggiore flessibilità e sicurezza del contenuto. Le modifiche seguenti sono state apportate all'SDK dalla versione 9 della serie.

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a>Nuova interfaccia per l'elaborazione specifica dell'applicazione durante l'accelerazione video DirectX

Le applicazioni lettore che supportano l'accelerazione video DirectX ora possono implementare l'interfaccia [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) per eseguire l'elaborazione specifica dell'applicazione durante la decodifica di DirectX va. Il lettore chiama il metodo di callback [**IWMPLayerHook::P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) prima di passare gli esempi video compressi al processore video per la decodifica.

> [!Note]  
> Per usare l'interfaccia **IWMPlayerHook** e l'interfaccia [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) associata, è necessario aver installato l'aggiornamento numero 888656 in Windows Media Format SDK. È possibile scaricare l'aggiornamento dal [sito Web Microsoft](https://support.microsoft.com/?id=888656).

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a>Windows Media Format SDK versione per versioni basate su x64 di Windows

È disponibile una versione basata su x64 di Windows Media Format SDK. Questa documentazione si applica sia alle versioni a 32 bit che alla versione basata su x64 dell'SDK. Tuttavia, Digital Rights Management (DRM) non è supportato in Windows Media Format SDK basato su x64.

## <a name="new-version-of-the-windows-media-video-image-codec"></a>Nuova versione del codec di immagine Windows Media Video

Il codec Windows Media Video 9 image V2 semplifica i calcoli Geometry di esempio per la panoramica e lo zoom. Il nuovo codec supporta inoltre diverse transizioni complesse tra le immagini.

## <a name="new-version-of-the-windows-media-audio-codecs"></a>Nuova versione dei codec Windows Media Audio

Windows Media Format 9,5 SDK include i codec audio aggiornati seguenti:

-   Windows Media Audio 9,1
-   Windows Media Audio 9,1 Professional
-   Windows Media Audio 9,1 senza perdita di perdite

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a>Supporto del protocollo Windows Media DRM 10 per dispositivi di rete

Windows Media Format 9,5 SDK supporta il nuovo protocollo Windows Media DRM 10 per i dispositivi di rete Secure Transfer Protocol. Questo protocollo può essere usato per trasmettere il contenuto crittografato in una rete locale a un dispositivo di riproduzione, ad esempio un ricevitore video di set-top.

La maggior parte delle procedure utilizzate per implementare il supporto per Windows Media DRM 10 per i dispositivi di rete deve essere eseguita dall'applicazione. Tuttavia, è possibile usare i metodi di Windows Media Format SDK per fornire le funzionalità seguenti:

-   Gestire un database di dispositivi, inclusi quelli abilitati per Windows Media DRM 10 per i dispositivi di rete.
-   Convalidare i dispositivi per assicurarsi che siano sufficientemente vicini al client in rete per lo streaming protetto.
-   Convertire i file protetti da DRM in Windows Media DRM 10 per i flussi di dispositivi di rete.
-   Scrivere file usando dati precedentemente crittografati.

## <a name="support-for-new-drm-licenses"></a>Supporto per le nuove licenze DRM

Le nuove licenze create mediante Windows Media Rights Manager SDK utilizzano i livelli di protezione dell'output (OPLs) per specificare i diritti e le restrizioni per la riproduzione e la copia del contenuto. Windows Media Format SDK fornisce il supporto per la lettura di OPLs da una licenza.

## <a name="new-video-codec"></a>Nuovo codec video

Il Windows Media Video 9 Advanced Profile codec si basa sull'elevata qualità del codec Windows Media Video 9, mentre aggiunge il supporto per la codifica interlacciata.

## <a name="spdif-output"></a>Output S/PDIF

Il contenuto codificato con uno dei codec professionali Windows Media Audio ora può essere trasferito o trasmesso usando il formato di interconnessione digitale (S/PDIF) di Sony/Philips.

## <a name="low-delay-audio"></a>Audio Low-Delay

I codec Windows Media Audio 9,1 e Windows Media Audio 9,1 Professional supportano ora diversi formati a basso ritardo. Questi formati producono flussi audio che possono essere avviati più rapidamente, riducendo la latenza negli scenari di cambio di flusso. La latenza complessiva nelle trasmissioni live viene anche migliorata usando formati a ritardo ridotto.

## <a name="approximate-seeking-mode"></a>Modalità di ricerca approssimativa

È ora possibile cercare un'ora approssimativa in un file ASF con il lettore. Questa modalità migliora le prestazioni quando si esegue una ricerca imprecisa, ad esempio quando un utente fa clic sulla barra di ricerca in Windows Media Player. La ricerca approssimativa restituisce l'esempio di supporto per il cleanpoint precedente invece di ricostruire l'esempio per il tempo esatto ricercato.

## <a name="playlist-burning"></a>Masterizzazione playlist

Windows Media DRM 10 supporta i diritti per la copia dei file audio nel CD di Red Book come parte di una playlist. Windows Media Format SDK fornisce i metodi per verificare se i file in una playlist possono essere copiati.

## <a name="improved-multiple-language-support-for-metadata"></a>Supporto Multiple-Language migliorato per i metadati

In Windows Media Format 9 Series SDK tutti i metadati aggiunti a un file sono stati assegnati a un elenco di lingue a cui è stato assegnato l'identificatore della lingua predefinita. Ciò ha causato problemi quando i distributori di contenuti in impostazioni locali diverse hanno aggiunto alcuni metadati, perché gli utenti nelle impostazioni locali del server di distribuzione visualizzano solo i pochi attributi aggiunti per la lingua. Il Windows Media Format 9,5 SDK risolve questo problema non creando un elenco di lingue fino a quando non sono presenti attributi di due lingue presenti nel file. A questo punto, tutti i metadati sono associati alle impostazioni locali della seconda lingua, che diventa quindi il valore predefinito. In questo modo, un server di distribuzione del contenuto può mantenere tutti i metadati originali per un file, ad esempio titolo e autore, intatti durante l'aggiunta di alcuni attributi pertinenti alle rispettive impostazioni locali.

## <a name="windows-media-device-manager-sdk-included-in-installation"></a>Windows Media Gestione dispositivi SDK incluso nell'installazione

Il pacchetto di installazione per Windows Media Format 9,5 SDK installa Windows Media Gestione dispositivi SDK. La documentazione relativa a Windows Media Gestione dispositivi SDK si trova nella cartella C: \\ WMSDK \\ WMFSDK95 \\ WMDM \\ docs (la cartella sarà diversa se non si installa Windows Media Format SDK nella cartella predefinita).

## <a name="codec-interface-documentation"></a>Documentazione dell'interfaccia codec

Questa documentazione include informazioni sull'uso dei codec Windows Media Audio e video al di fuori di Windows Media Format SDK. Questa documentazione è stata originariamente rilasciata come parte di un download da Microsoft Developer Network. Le applicazioni di esempio che illustrano l'uso diretto del codec DMOs sono incluse nell'installazione di Windows Media Format SDK con le intestazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




