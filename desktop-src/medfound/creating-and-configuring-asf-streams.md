---
description: Ogni file ASF contiene uno o più flussi. L'oggetto Profilo ASF rappresenta una raccolta di flussi ASF. Per la codifica ASF, è necessario creare e configurare i flussi da codificare.
ms.assetid: cc89e8bc-58ff-48e2-9668-0dcd6cfd25e1
title: Creazione e configurazione di asf Flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c780de3fa0abb5db29e3e5e5ed049b78aca7898966e8f7e8595b504804da91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743240"
---
# <a name="creating-and-configuring-asf-streams"></a>Creazione e configurazione di asf Flussi

Ogni file ASF contiene uno o più flussi. [L'oggetto Profilo ASF](asf-profile.md) rappresenta una raccolta di flussi ASF. Per la codifica ASF, è necessario creare e configurare i flussi da codificare.

Un'applicazione può eseguire le attività seguenti con l'oggetto profilo ASF:

-   Aggiungere o rimuovere un flusso.
-   Ottenere le impostazioni di configurazione di un flusso.
-   Configurare le estensioni del payload.
-   Aggiungere, rimuovere o modificare un oggetto di esclusione reciproca di ASF.

In questo argomento sono contenute le sezioni seguenti.

-   [Creazione di un nuovo flusso](#creating-a-new-stream)
-   [Assegnazione di numeri di flusso](#assigning-stream-numbers)
-   [Impostazione dei valori dei bucket persi](#setting-leaky-bucket-values)
-   [Estensioni del payload](#payload-extensions)
-   [Aggiunta di un flusso al profilo](#adding-a-stream-to-the-profile)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-new-stream"></a>Creazione di un nuovo flusso

Un oggetto profilo ASF deve contenere le impostazioni di configurazione per almeno un flusso ASF. Ogni flusso è rappresentato da un *oggetto di configurazione* del flusso, che espone l'interfaccia [**IMFASFStreamConfig.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) Le informazioni nell'oggetto di configurazione del flusso corrispondono all'oggetto Proprietà flusso e agli oggetti proprietà del flusso esteso nell'intestazione del file ASF. Vedere [Struttura del file ASF.](asf-file-structure.md)

Per aggiungere un flusso a un profilo asf, seguire questa procedura:

1.  Creare un oggetto di configurazione del flusso vuoto.
2.  Configurare il flusso in base ai requisiti dell'applicazione.
3.  Aggiungere il flusso al profilo.

Per creare un flusso per il profilo, chiamare [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) per creare un oggetto di configurazione del flusso vuoto e ricevere il puntatore nel *parametro ppIStream.* **CreateStream** deve conoscere il tipo di flusso da creare. I tipi più comuni di flussi usati nei file ASF sono i flussi audio e video. In Media Foundation, i tipi di flusso vengono denoti dall'oggetto tipo di supporto che espone [**l'interfaccia IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Il tipo principale del tipo di supporto definisce la categoria del flusso multimediale digitale, ad esempio audio o video. Il sottotipo definisce il formato del tipo principale. Il tipo di supporto iniziale impostato da **CreateStream** può essere modificato usando l'oggetto di configurazione stream. Per recuperare il tipo di supporto per il flusso, chiamare [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) o per recuperare il tipo principale [**chiamare IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype). Il tipo di supporto iniziale per un flusso può essere sostituito con un nuovo tipo di supporto configurato chiamando [**IMFASFStreamConfig::SetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setmediatype).

Se un'applicazione crea un profilo da un descrittore di presentazione valido chiamando [**MFCreateASFProfileFromPresentationDescriptor.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) La funzione imposta automaticamente gli oggetti di configurazione del flusso per ognuno dei flussi e li imposta nel profilo. I tipi di supporti di flusso vengono impostati in base ai descrittori di flusso associati al descrittore di presentazione.

## <a name="assigning-stream-numbers"></a>Assegnazione di numeri di flusso

Flussi di tutti i tipi deve essere assegnato un numero di flusso. I numeri di flusso non devono essere sequenziali, ma devono essere nell'intervallo compreso tra 1 e 127. Per assegnare i numeri di flusso, [**chiamare IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber). Per ottenere la chiamata al numero di flusso, [**IMFASFStreamConfig::GetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamnumber).

> [!Note]  
> Un numero di flusso è diverso da un indice di flusso, che viene utilizzato quando si ottengono flussi in un profilo usando [**IMFASFProfile::GetStream.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) L'indice del flusso è un numero assegnato al flusso dall'oggetto profilo. Gli indici di flusso sono compresi tra 0 e uno minore del numero di flussi recuperati da [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount). È anche possibile ottenere un flusso dal profilo in base al numero di flusso chiamando [**IMFASFProfile::GetStreamByNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber).

 

## <a name="setting-leaky-bucket-values"></a>Impostazione dei valori dei bucket persi

A ogni oggetto di configurazione del flusso che rappresenta un flusso devono essere associati parametri di bucket persi, velocità in bit e valori della finestra del buffer.

Questi valori sono disponibili per l'applicazione tramite [**l'attributo MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) e l'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2.**](mf-asfstreamconfig-leakybucket2-attribute.md) Per la codifica dei file, i valori effettivi dipendono dal tipo di codifica e vengono deciso dal codificatore. Se si dispone già di un codificatore configurato e il tipo di output è impostato sul codificatore, l'applicazione deve eseguire una query sul codificatore per i parametri di bucket persi e impostare i valori in questi attributi.

Se si usano i componenti del livello pipeline e si configurano i flussi per il sink multimediale asf, molto probabilmente non si dispone di un codificatore configurato. In questo caso, è necessario eseguire una query sul tipo di media post-media del codificatore e impostare il valore aggiornato nella proprietà [**MFPKEY \_ ASFSTREAMSINK \_ CORRECTED \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) dell'archivio delle proprietà del sink multimediale ASF. L'archivio delle proprietà di codifica viene recuperato tramite dell'oggetto ContentInfo associato al profilo. I valori aggiornati si riflettono automaticamente nei valori dell'attributo bucket persa del flusso. Per informazioni generali sui bucket persi e su come ottenere il valore del bucket di perdita dal codificatore, vedere [Il modello](the-leaky-bucket-buffer-model.md)di buffer di bucket persi.

## <a name="payload-extensions"></a>Estensioni del payload

I dati multimediali per i flussi vengono aggiunti all'oggetto dati ASF come [campioni multimediali](media-samples.md) da [ASF Multiplexer.](asf-multiplexer.md) Questi esempi multimediali possono contenere dati di estensione del payload: dati SMPTE time code, proporzioni pixel non quadrate, durata del campione e, se l'esempio lo contiene, un fotogramma chiave video. Per un elenco dei tipi di estensione di payload supportati, vedere GUID [dell'estensione del payload ASF.](asf-payload-extension-guids.md)

È necessario configurare un flusso per accettare l'estensione del payload in modo che durante la generazione del campione il multiplexer possa aggiungere i dati supplementari a ogni esempio per tale flusso.

Per ottenere il numero totale di estensioni di payload impostate nel flusso, chiamare [**IMFASFStreamConfig::GetPayloadExtensionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount) e quindi enumerare l'elenco chiamando [**IMFASFStreamConfig::GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension). Per aggiungere l'estensione del payload per il flusso, [**chiamare IMFASFStreamConfig::AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension). Verranno aggiunti dati supplementari ai singoli campioni multimediali generati per il flusso.

Per rimuovere le estensioni di payload esistenti associate al flusso, chiamare [**IMFASFStreamConfig::RemoveAllPayloadExtensions**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-removeallpayloadextensions).

## <a name="adding-a-stream-to-the-profile"></a>Aggiunta di un flusso al profilo

Dopo aver configurato un flusso, chiamare [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) per aggiungere il flusso al profilo.

Per rimuovere un flusso esistente nel profilo, chiamare [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).

Il profilo configurato deve essere impostato nell'oggetto ContentInfo chiamando [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Se si apportano modifiche a un flusso esistente, è necessario aggiungerlo nuovamente al profilo e impostare il profilo nell'oggetto ContentInfo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Profilo ASF](asf-profile.md)
</dt> <dt>

[Supporto di ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



