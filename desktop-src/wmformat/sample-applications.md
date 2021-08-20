---
title: Windows Applicazioni di esempio di Media Format SDK
description: Windows Applicazioni di esempio di Media Format SDK
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Media Format SDK, applicazioni di esempio
- DRM (Digital Rights Management), applicazioni di esempio
- DRM (Digital Rights Management),applicazioni di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c778ef1613359f6f3dc6c08d918e32f2f29bade
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475007"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Windows Applicazioni di esempio di Media Format SDK

Il codice di esempio fornito con questo SDK è sotto forma di progetti per Microsoft Visual Studio 2005. La maggior parte degli esempi è in C++, ma ManagedWMFSDKWrapper e ManagedMetadataEdit richiedono C#.

Questi esempi non funzionano a meno che non sia stato installato Windows Media Format SDK o Windows Player SDK.

Le informazioni sull'utilizzo per ogni esempio sono contenute in un file readme.txt in ogni directory di esempio.




| Samle | Descrizione | 
|-------|-------------|
| Audioplayer | Riproduce Windows file multimediali, inclusi i file protetti da DRM. È controllato tramite un'interfaccia utente grafica e i comandi includono Play, Pause, Seek e Stop. Può riprodurre file locali o file letti da Internet (inclusi quelli di output in Internet usando l'esempio WMVNetWrite).<blockquote>[!Note]<br />Le parti DRM di questo esempio non sono supportate nelle versioni basate su x64 di Windows.</blockquote><br /> | 
| DRMHeader | DRMHeader è un'applicazione console che usa l'interfaccia <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> dell'editor dei metadati per leggere gli attributi DRM dei file senza collegarsi alla libreria statica DRM.<blockquote>[!Note]<br />Questo esempio non è supportato nelle versioni basate su x64 di Windows.</blockquote><br /> | 
| DRMShow | DRMShow è un'applicazione console che illustra come leggere le proprietà <a href="wmformat-glossary.md"><em>DRM</em></a> di un file Windows Media usando il metodo <strong>IWMDRMReader::GetDRMProperty.</strong> Questo esempio illustra l'uso del metodo <strong>IWMDRMReader::GetDRMProperty</strong> e delle proprietà che possono essere recuperate dal lettore DRM. Non viene illustrato come acquisire una licenza per il contenuto protetto da DRM. Questo esempio richiede la compilazione della libreria stub DRM WMStubDRM.lib.<br /><blockquote>[!Note]<br />Questo esempio non è supportato nelle versioni basate su x64 di Windows.</blockquote><br /> Quando si acquisisce WMStubDRM.lib da Microsoft, alla libreria viene assegnato un livello di sicurezza dell'applicazione. Se il livello di sicurezza della libreria ricevuta non è sufficiente per riprodurre un file protetto, in questo esempio verrà visualizzato un errore.<br /> | 
| DirectShowInterop/DSCopy | Transcodifica uno o più file in un file ASF usando il DirectShow WM ASF Writer. Il file di input può essere qualsiasi formato compresso o non compresso supportato da DirectShow. | 
| DirectShowInterop/DSPlay | Questo esempio è un lettore di file multimediali audio/video interattivo con <a href="wmformat-glossary.md"><em>supporto DRM.</em></a> Usa il filtro lettore ASF WM di DirectShow per riprodurre file multimediali di Windows (ASF, WMA, WMV) senza protezione DRM e file che usano DRM a un livello di 100 o inferiore. Per altre readme.txt, vedere l'readme.txt nella directory dell'esempio. | 
| DirectShowInterop/DSSeekFm | Questo esempio illustra come usare il filtro lettore ASF di DirectShow WM per riprodurre contenuto ASF in un grafo del filtro DirectShow e come usare il supporto per la ricerca di frame in Windows Media Format SDK. | 
| Managed/WMFSDKWrapper | Questo assembly gestito funge da wrapper usato dagli esempi di codice gestito per accedere ad alcune interfacce di metadati di questo SDK. | 
| Managed/MetadataEdit | Questa applicazione C# può essere usata per visualizzare e modificare metadati da Windows file multimediali. | 
| MetaDataEdit | Si tratta di una versione C++ dell'applicazione Managed MetadataEdit. | 
| ReadFromStream | Questo esempio di applicazione console illustra come leggere dati da <strong>IStream</strong> con WMReader. <strong>L'origine IStream</strong> è stata implementata per usare un file in Windows Media Format (WMA/WMV/ASF).<blockquote>[!Note]<br />Questo esempio non illustra come elaborare gli esempi multimediali provenienti da WMReader. Per esempi su come elaborare audio/video o altri tipi di esempi multimediali, vedere altri esempi, ad esempio AudioPlayer, inclusi in Windows Media Format SDK.</blockquote><br /> | 
| UncompAVIToWMV | Questo esempio di applicazione console mostra il codice necessario per comprimere un file AVI in un file WMV. Illustra come unire esempi per flussi audio e video da diversi file AVI e come unire questi in flussi simili o creare un nuovo flusso basato sul profilo di flusso di origine. Illustra anche come creare un flusso arbitrario, eseguire la codifica multipass, aggiungere SMPTE time code e applicare la protezione DRM versione 1. | 
| WMGenProfile/exe | Questo esempio è stato aggiornato dalla versione 7.1. È ora un'applicazione di dialogo MFC. L'esempio WMGenProfile illustra l'uso della libreria statica WMGenProfile. Funge anche da strumento per la creazione di profili. Questo strumento è destinato agli sviluppatori che hanno familiarità con Windows Media Format. L'interfaccia utente non è stata testata per l'esperienza utente e non è concepita come raccomandazione su come presentare queste informazioni a un utente. | 
| WMGenProfile/lib | L'esempio di libreria GenProfile illustra la creazione di profili. Illustra come creare tipi di file multimediali e flussi per vari tipi di flusso (audio, video, script, immagine, trasferimento di file e Web). Non viene illustrato come usare i profili di sistema o come convertire i profili di sistema in profili che specificano i codec Windows Media Audio e Video 9 Series. | 
| WMProp | Questa applicazione console illustra come recuperare gli attributi tramite l'oggetto dell'editor di metadati e le informazioni sul profilo dal lettore. | 
| WMStats | Questa applicazione console visualizza le statistiche reader e writer. È anche possibile usare più istanze di WMStats contemporaneamente in un unico computer. Avviare un'istanza come server per inviare il flusso alla rete e quindi eseguire una seconda istanza come client per verificare che il server sia in streaming correttamente. | 
| WMSyncReader | Questo esempio di applicazione console illustra come leggere un file multimediale usando <strong>IWMSyncReader</strong> senza creare thread aggiuntivi o usare callback. Sono implementate le funzionalità seguenti: Lettura di esempi compressi o decompressi<br /> Ricerca basata sul tempo<br /> Ricerca basata su frame<br /><strong>Origine derivata IStream</strong><br /> | 
| WMVAppend | Questa applicazione console accetta due Windows file multimediali per l'input e tenta di creare un file di output con il contenuto del primo seguito dal secondo. Nell'esempio vengono confrontati i profili dei due file di input per assicurarsi che siano abbastanza simili da essere aggiunti. In caso contrario, viene visualizzato un messaggio di errore. Ad esempio, un messaggio di errore si verifica quando un file è solo audio e il secondo è un file audio-video o quando due file audio hanno velocità in bit diverse. L'esempio accetta origini vbr (Variable Bit Rate). Tuttavia, quando si confrontano i profili delle due origini VBR, l'esempio ignora la differenza di velocità in bit media perché due flussi VBR avranno velocità in bit medie diverse anche se sono state create usando lo stesso profilo. WMVAppend non è in grado di confrontare la velocità in bit massima dei flussi VBR non vincolati basati sulla velocità in bit o il livello di qualità dei flussi VBR basati sulla qualità, perché queste informazioni non esistono nei file di origine. È quindi responsabilità dell'utente assicurarsi che due file di origine siano creati usando lo stesso profilo. In caso contrario, è possibile creare contenuto non valido.<br /> | 
| WMVCopy | Questo esempio illustra il codice necessario per copiare un file WMV. Illustra come leggere e scrivere esempi compressi, leggere gli attributi e gli script dell'intestazione e modificare gli attributi di intestazione. | 
| WMVNetWrite | Questa applicazione console mostra come un Windows file multimediale viene trasmesso in Internet. L'esempio richiede che sia specificata una porta e quindi il file può essere riprodotto usando un lettore. | 
| WMVRecompress | Questa applicazione console mostra come ricomprimere un file WMV. Illustra la lettura di esempi non compressi, la scrittura di esempi non compressi e l'applicazione della codifica multipassaggio, dell'output multicanale e della ricompressione intelligente. | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 





