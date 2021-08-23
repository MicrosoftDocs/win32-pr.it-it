---
title: Windows Applicazioni di esempio di Media Format SDK
description: Windows Applicazioni di esempio di Media Format SDK
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Media Format SDK, applicazioni di esempio
- digital rights management (DRM), applicazioni di esempio
- DRM (digital rights management),applicazioni di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381f489cf00aa044a26e25438c3c2a724b23e1975e2de5712f695e4ddb6e8a0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547141"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Windows Applicazioni di esempio di Media Format SDK

Il codice di esempio fornito con questo SDK è sotto forma di progetti per Microsoft Visual Studio 2005. La maggior parte degli esempi è in C++, ma ManagedWMFSDKWrapper e ManagedMetadataEdit richiedono C#.

Questi esempi non funzionano a meno che non sia stato installato Windows Media Format SDK o Windows Player SDK.

Le informazioni sull'utilizzo per ogni esempio sono contenute in un file readme.txt in ogni directory di esempio.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Samle</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Audioplayer</td>
<td>Riproduce Windows file multimediali, inclusi i file protetti da DRM. È controllato tramite un'interfaccia utente grafica e i comandi includono Play, Pause, Seek e Stop. Può riprodurre file locali o file letti da Internet (inclusi quelli in Internet usando l'esempio WMVNetWrite).
<blockquote>
[!Note]<br />
Le parti DRM di questo esempio non sono supportate nelle versioni basate su x64 di Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>DRMHeader</td>
<td>DRMHeader è un'applicazione console che usa l'interfaccia <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> dell'editor di metadati per leggere gli attributi DRM dei file senza collegarsi alla libreria statica DRM.
<blockquote>
[!Note]<br />
Questo esempio non è supportato nelle versioni basate su x64 di Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>DRMShow</td>
<td>DRMShow è un'applicazione console che illustra come leggere le proprietà <a href="wmformat-glossary.md"><em>DRM</em></a> di un file Windows Media usando il metodo <strong>IWMDRMReader::GetDRMProperty.</strong> Questo esempio illustra l'uso del metodo <strong>IWMDRMReader::GetDRMProperty</strong> e delle proprietà che possono essere recuperate dal lettore DRM. Non illustra come acquisire una licenza per il contenuto protetto da DRM. Questo esempio richiede la compilazione della libreria stub DRM WMStubDRM.lib.<br/>
<blockquote>
[!Note]<br />
Questo esempio non è supportato nelle versioni basate su x64 di Windows.
</blockquote>
<br/> Quando si acquisisce WMStubDRM.lib da Microsoft, alla libreria viene assegnato un livello di sicurezza dell'applicazione. Se il livello di sicurezza della libreria ricevuta non è sufficiente per riprodurre un file protetto, in questo esempio verrà visualizzato un errore.<br/></td>
</tr>
<tr class="even">
<td>DirectShowInterop/DSCopy</td>
<td>Transcodifica uno o più file in un file ASF usando il filtro DirectShow WM ASF Writer. Il file di input può essere qualsiasi formato compresso o non compresso supportato da DirectShow.</td>
</tr>
<tr class="odd">
<td>DirectShowInterop/DSPlay</td>
<td>Questo esempio è un lettore di file multimediali audio/video interattivo con <a href="wmformat-glossary.md"><em>supporto DRM.</em></a> Usa il filtro WM ASF Reader di DirectShow per riprodurre file multimediali Windows (ASF, WMA, WMV) senza protezione DRM e file che usano DRM a un livello di 100 o inferiore. Per altre readme.txt, vedere readme.txt nella directory dell'esempio.</td>
</tr>
<tr class="even">
<td>DirectShowInterop/DSSeekFm</td>
<td>Questo esempio illustra come usare il filtro lettore ASF DirectShow WM per riprodurre contenuto ASF in un grafo di filtro DirectShow e come usare il supporto per la ricerca di frame in Windows Media Format SDK.</td>
</tr>
<tr class="odd">
<td>Managed/WMFSDKWrapper</td>
<td>Questo assembly gestito funge da wrapper usato dagli esempi di codice gestito per accedere ad alcune interfacce di metadati di questo SDK.</td>
</tr>
<tr class="even">
<td>Managed/MetadataModifica</td>
<td>Questa applicazione C# può essere usata per visualizzare e modificare i metadati Windows file multimediali.</td>
</tr>
<tr class="odd">
<td>MetaDataModifica</td>
<td>Si tratta di una versione C++ dell'applicazione Managed MetadataEdit.</td>
</tr>
<tr class="even">
<td>ReadFromStream</td>
<td>Questo esempio di applicazione console illustra come leggere dati da <strong>IStream</strong> con WMReader. <strong>L'origine IStream</strong> è stata implementata per usare un file in Windows Media Format (WMA/WMV/ASF).
<blockquote>
[!Note]<br />
Questo esempio non illustra come elaborare gli esempi multimediali provenienti da WMReader. Per esempi su come elaborare audio/video o altri tipi di esempi multimediali, vedere altri esempi, ad esempio AudioPlayer, inclusi in Windows Media Format SDK.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>UncompAVIToWMV</td>
<td>Questo esempio di applicazione console mostra il codice necessario per comprimere un file AVI in un file WMV. Viene illustrato come unire esempi per flussi audio e video da diversi file AVI e unire questi in flussi simili o creare un nuovo flusso basato sul profilo del flusso di origine. Illustra anche come creare un flusso arbitrario, eseguire la codifica multipass, aggiungere SMPTE time code e applicare la protezione DRM versione 1.</td>
</tr>
<tr class="even">
<td>WMGenProfile/exe</td>
<td>Questo esempio è stato aggiornato dalla versione 7.1. Si tratta ora di un'applicazione finestra di dialogo MFC. L'esempio WMGenProfile illustra l'uso della libreria statica WMGenProfile. Funge anche da strumento per la creazione di profili. Questo strumento è destinato agli sviluppatori che hanno familiarità con Windows Media Format. L'interfaccia utente non è stata testata per l'esperienza utente e non è stata concepita come raccomandazione su come presentare queste informazioni a un utente.</td>
</tr>
<tr class="odd">
<td>WMGenProfile/lib</td>
<td>L'esempio di libreria GenProfile illustra la creazione di profili. Viene illustrato come creare tipi di supporti e flussi per vari tipi di flusso (audio, video, script, immagine, trasferimento di file e Web). Non illustra come usare i profili di sistema o come convertire i profili di sistema in profili che specificano i codec Windows Media Audio e Video serie 9.</td>
</tr>
<tr class="even">
<td>WMProp</td>
<td>Questa applicazione console illustra come recuperare gli attributi usando l'oggetto dell'editor dei metadati e le informazioni sul profilo dal lettore.</td>
</tr>
<tr class="odd">
<td>WMStats</td>
<td>Questa applicazione console visualizza le statistiche reader e writer. È anche possibile usare più istanze di WMStats contemporaneamente in un computer. Avviare un'istanza come server per inviare il flusso alla rete e quindi eseguire una seconda istanza come client per verificare che il server sia in streaming correttamente.</td>
</tr>
<tr class="even">
<td>WMSyncReader</td>
<td>Questo esempio di applicazione console illustra come leggere un file multimediale usando <strong>IWMSyncReader</strong> senza creare thread aggiuntivi o usare callback. Vengono implementate le funzionalità seguenti: Lettura di esempi compressi o decompressi<br/> Ricerca basata sul tempo<br/> Ricerca basata su frame<br/> <strong>Origine derivata da IStream</strong><br/></td>
</tr>
<tr class="odd">
<td>WMVAppend</td>
<td>Questa applicazione console accetta due Windows file multimediali per l'input e tenta di creare un file di output con il contenuto del primo seguito dal secondo. L'esempio confronta i profili dei due file di input per assicurarsi che siano sufficientemente simili da essere aggiunti. In caso contrario, viene visualizzato un messaggio di errore. Ad esempio, un messaggio di errore si verifica quando un file è solo audio e il secondo è un file audio-video o quando due file audio hanno velocità in bit diverse. L'esempio accetta origini vbr (Variable Bit Rate). Tuttavia, quando si confrontano i profili delle due origini VBR, l'esempio ignora la differenza di velocità in bit media perché due flussi VBR avranno velocità in bit medie diverse anche se sono state create usando lo stesso profilo. WMVAppend non è in grado di confrontare la velocità in bit di picco dei flussi VBR basati su velocità in bit non vincolata o il livello di qualità dei flussi VBR basati sulla qualità, perché queste informazioni non esistono nei file di origine. È quindi responsabilità dell'utente assicurarsi che due file di origine siano creati usando lo stesso profilo. In caso contrario, è possibile creare contenuto non valido.<br/></td>
</tr>
<tr class="even">
<td>WMVCopy</td>
<td>Questo esempio illustra il codice necessario per copiare un file WMV. Viene illustrato come leggere e scrivere esempi compressi, leggere gli attributi e gli script dell'intestazione e modificare gli attributi di intestazione.</td>
</tr>
<tr class="odd">
<td>WMVNetWrite</td>
<td>Questa applicazione console mostra come un Windows file multimediale viene trasmesso tramite Internet. L'esempio richiede che sia specificata una porta e che il file possa essere riprodotto usando un lettore.</td>
</tr>
<tr class="even">
<td>WMVRecompress</td>
<td>Questa applicazione console illustra come ricomprimere un file WMV. Illustra la lettura di esempi non compressi, la scrittura di esempi non compressi e l'applicazione di codifica multipassaggio, output multicanale e ricompressione intelligente.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 





