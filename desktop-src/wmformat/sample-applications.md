---
title: Applicazioni di esempio di Windows Media Format SDK
description: Applicazioni di esempio di Windows Media Format SDK
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Media Format SDK, applicazioni di esempio
- Digital Rights Management (DRM), applicazioni di esempio
- DRM (Digital Rights Management), applicazioni di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474867"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Applicazioni di esempio di Windows Media Format SDK

Il codice di esempio fornito con questo SDK è sotto forma di progetti per Microsoft Visual Studio 2005. La maggior parte degli esempi è in C++, ma ManagedWMFSDKWrapper e ManagedMetadataEdit richiedono C#.

Questi esempi non funzioneranno a meno che non sia stato installato Windows Media Format SDK o Windows Player SDK.

Le informazioni sull'utilizzo per ogni campione sono contenute in un file di readme.txt in ogni directory di esempio.



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
<td>AudioPlayer</td>
<td>Riproduce file Windows Media, inclusi i file protetti da DRM. Viene controllata tramite un'interfaccia utente grafica e i comandi includono Play, pause, seek e stop. Può riprodurre file o file locali letti da Internet (incluso l'output in Internet usando l'esempio WMVNetWrite).
<blockquote>
[!Note]<br />
Le parti DRM di questo esempio non sono supportate nelle versioni di Windows basate su x64.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>DRMHeader</td>
<td>DRMHeader è un'applicazione console che usa l'interfaccia <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> dell'editor dei metadati per leggere gli attributi DRM dei file senza collegarsi alla libreria statica DRM.
<blockquote>
[!Note]<br />
Questo esempio non è supportato nelle versioni di Windows basate su x64.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>DRMShow</td>
<td>DRMShow è un'applicazione console che Mostra come leggere le proprietà <a href="wmformat-glossary.md"><em>DRM</em></a> di un file Windows Media usando il metodo <strong>IWMDRMReader:: GetDRMProperty</strong> . Questo esempio illustra l'uso del metodo <strong>IWMDRMReader:: GetDRMProperty</strong> e delle proprietà che possono essere recuperate dal lettore DRM. Non viene illustrato come acquisire una licenza per il contenuto protetto da DRM. Questo esempio richiede la libreria stub DRM WMStubDRM. lib per la compilazione.<br/>
<blockquote>
[!Note]<br />
Questo esempio non è supportato nelle versioni di Windows basate su x64.
</blockquote>
<br/> Quando si acquisisce WMStubDRM. lib da Microsoft, alla libreria viene assegnato un livello di sicurezza dell'applicazione. Se il livello di sicurezza della libreria ricevuta non è sufficiente per riprodurre un file protetto, in questo esempio verrà visualizzato un errore.<br/></td>
</tr>
<tr class="even">
<td>DirectShowInterop/DSCopy</td>
<td>Consente di eseguire la transcodifica di uno o più file in un file ASF usando il filtro del writer ASF di DirectShow WM. Il file di input può essere qualsiasi formato compresso o non compresso supportato da DirectShow.</td>
</tr>
<tr class="odd">
<td>DirectShowInterop/DSPlay</td>
<td>Questo esempio è un lettore di file multimediale audio/video interattivo con supporto <a href="wmformat-glossary.md"><em>DRM</em></a> . Usa il filtro per i lettori WM ASF di DirectShow per riprodurre file Windows Media (ASF, WMA, WMV) senza protezione DRM e file che usano DRM a un livello di 100 o di seguito. Per ulteriori informazioni, vedere readme.txt nella directory dell'esempio.</td>
</tr>
<tr class="even">
<td>DirectShowInterop/DSSeekFm</td>
<td>In questo esempio viene illustrato come utilizzare il filtro lettore ASF di DirectShow WM per riprodurre contenuto ASF in un grafico filtro DirectShow e come utilizzare il frame che cerca supporto in Windows Media Format SDK.</td>
</tr>
<tr class="odd">
<td>Gestito/WMFSDKWrapper</td>
<td>Questo assembly gestito funge da wrapper utilizzato dagli esempi di codice gestito per accedere ad alcune interfacce di metadati di questo SDK.</td>
</tr>
<tr class="even">
<td>Gestito/MetadataEdit</td>
<td>Questa applicazione C# può essere usata per visualizzare e modificare i metadati dai file di Windows Media.</td>
</tr>
<tr class="odd">
<td>MetaDataEdit</td>
<td>Si tratta di una versione C++ dell'applicazione MetadataEdit gestita.</td>
</tr>
<tr class="even">
<td>ReadFromStream</td>
<td>Questo esempio di applicazione console Mostra come leggere i dati da <strong>IStream</strong> con WMReader. L'origine <strong>IStream</strong> è stata implementata per usare un file in formato Windows Media (WMA/WMV/ASF).
<blockquote>
[!Note]<br />
Questo esempio non Mostra come elaborare gli esempi di supporti provenienti da WMReader. Per esempi su come elaborare audio/video o altri tipi di esempi multimediali, fare riferimento ad altri esempi, ad esempio AudioPlayer, inclusi in Windows Media Format SDK.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>UncompAVIToWMV</td>
<td>Questo esempio di applicazione console mostra il codice necessario per comprimere un file AVI in un file WMV. Mostra come unire esempi per flussi audio e video da diversi file AVI e unirli in flussi simili o creare un nuovo flusso basato sul profilo del flusso di origine. Viene inoltre illustrato come creare un flusso arbitrario, eseguire la codifica Multipass, aggiungere codice ora SMPTE e applicare la protezione DRM versione 1.</td>
</tr>
<tr class="even">
<td>WMGenProfile/exe</td>
<td>Questo esempio è stato aggiornato dalla versione 7,1. È ora un'applicazione di dialogo MFC. L'esempio WMGenProfile illustra l'uso della libreria statica WMGenProfile. Funge anche da strumento per la creazione di profili. Questo strumento è destinato agli sviluppatori che hanno familiarità con il formato Windows Media. L'interfaccia utente non è stata testata per l'esperienza utente e non è destinata a una raccomandazione su come presentare queste informazioni a un utente.</td>
</tr>
<tr class="odd">
<td>WMGenProfile/lib</td>
<td>Nell'esempio di libreria GenProfile viene illustrata la creazione di profili. Viene illustrato come creare flussi e tipi di supporti per diversi tipi di flusso (audio, video, script, immagine, trasferimento di file e Web). Non viene illustrato come utilizzare i profili di sistema o come convertire i profili di sistema in profili che specificano i codec della serie Windows Media Audio e video 9.</td>
</tr>
<tr class="even">
<td>WMProp</td>
<td>In questa applicazione console viene illustrato come recuperare gli attributi utilizzando l'oggetto dell'editor dei metadati e le informazioni sul profilo dal reader.</td>
</tr>
<tr class="odd">
<td>WMStats</td>
<td>Questa applicazione console Visualizza le statistiche di Reader e writer. È anche possibile usare più istanze di WMStats contemporaneamente in un computer. Avviare un'istanza di come server per inviare il flusso alla rete e quindi eseguire una seconda istanza come client per verificare che il flusso del server sia corretto.</td>
</tr>
<tr class="even">
<td>WMSyncReader</td>
<td>Questo esempio di applicazione console Mostra come leggere un file multimediale usando <strong>IWMSyncReader</strong> senza creare alcun thread aggiuntivo o usare i callback. Sono state implementate le funzionalità seguenti: lettura di esempi compressi o decompressi<br/> Ricerca basata sul tempo<br/> Ricerca basata su frame<br/> Origine derivata <strong>IStream</strong><br/></td>
</tr>
<tr class="odd">
<td>WMVAppend</td>
<td>Questa applicazione console accetta due file di Windows Media per l'input e tenta di creare un file di output con il contenuto del primo seguito dal secondo. Nell'esempio vengono confrontati i profili dei due file di input per assicurarsi che siano sufficientemente simili da accodare. In caso contrario, viene visualizzato un messaggio di errore. Ad esempio, un messaggio di errore si verifica quando un file è solo audio e il secondo è un file audio-video o quando due file audio hanno velocità in bit diverse. L'esempio accetta le origini della velocità in bit variabile (VBR). Tuttavia, quando si confrontano i profili delle due origini VBR, l'esempio Ignora la differenza media della velocità in bit perché due flussi VBR avranno frequenze di bit medie diverse anche se sono state create con lo stesso profilo. WMVAppend non è in grado di confrontare la velocità in bit massima dei flussi VBR non vincolati basati sulla velocità in bit o il livello di qualità dei flussi VBR basati sulla qualità, perché queste informazioni non sono presenti nei file di origine. È pertanto responsabilità dell'utente verificare che vengano creati due file di origine usando lo stesso profilo. In caso contrario, è possibile creare contenuto non valido.<br/></td>
</tr>
<tr class="even">
<td>WMVCopy</td>
<td>In questo esempio viene illustrato il codice necessario per copiare un file WMV. Viene illustrato come leggere e scrivere esempi compressi, leggere gli attributi e gli script di intestazione e modificare gli attributi dell'intestazione.</td>
</tr>
<tr class="odd">
<td>WMVNetWrite</td>
<td>Questa applicazione console Mostra come un file di Windows Media viene trasmesso attraverso Internet. Per l'esempio è necessario specificare una porta e quindi il file può essere riprodotto utilizzando un lettore.</td>
</tr>
<tr class="even">
<td>WMVRecompress</td>
<td>Questa applicazione console Mostra come ricomprimere un file WMV. Viene illustrata la lettura di esempi non compressi, la scrittura di esempi non compressi e la codifica Multipass, l'output multicanale e la ricompressione intelligente.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 





