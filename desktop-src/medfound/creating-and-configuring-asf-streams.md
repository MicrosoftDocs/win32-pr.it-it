---
description: Ogni file ASF contiene uno o più flussi. L'oggetto profilo ASF rappresenta una raccolta di flussi ASF. Per la codifica ASF, è necessario creare e configurare i flussi che si desidera codificare.
ms.assetid: cc89e8bc-58ff-48e2-9668-0dcd6cfd25e1
title: Creazione e configurazione di flussi ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eabce588022dd66947f34e4dcd9db61f26448b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305466"
---
# <a name="creating-and-configuring-asf-streams"></a>Creazione e configurazione di flussi ASF

Ogni file ASF contiene uno o più flussi. L'oggetto [profilo ASF](asf-profile.md) rappresenta una raccolta di flussi ASF. Per la codifica ASF, è necessario creare e configurare i flussi che si desidera codificare.

Con l'oggetto profilo ASF, un'applicazione può eseguire le attività seguenti:

-   Aggiungere o rimuovere un flusso.
-   Ottenere le impostazioni di configurazione di un flusso.
-   Configurare le estensioni del payload.
-   Aggiunta, rimozione o modifica di un oggetto di esclusione reciproca ASF.

In questo argomento sono contenute le sezioni seguenti.

-   [Creazione di un nuovo flusso](#creating-a-new-stream)
-   [Assegnazione di numeri di flusso](#assigning-stream-numbers)
-   [Impostazione dei valori bucket persi](#setting-leaky-bucket-values)
-   [Estensioni del payload](#payload-extensions)
-   [Aggiunta di un flusso al profilo](#adding-a-stream-to-the-profile)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-new-stream"></a>Creazione di un nuovo flusso

Un oggetto profilo ASF deve contenere le impostazioni di configurazione per almeno un flusso ASF. Ogni flusso è rappresentato da un oggetto di *configurazione del flusso* , che espone l'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . Le informazioni contenute nell'oggetto di configurazione del flusso corrispondono all'oggetto proprietà del flusso e agli oggetti proprietà del flusso esteso nell'intestazione del file ASF. (Vedere la [struttura di file ASF](asf-file-structure.md)).

Per aggiungere un flusso a un profilo ASF, seguire questa procedura:

1.  Creare un oggetto di configurazione del flusso di flusso vuoto.
2.  Configurare il flusso in base ai requisiti dell'applicazione.
3.  Aggiungere il flusso al profilo.

Per creare un flusso per il profilo, chiamare [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) per creare un oggetto di configurazione del flusso vuoto e ricevere il puntatore nel parametro *ppIStream* . **CreateStream** deve essere in grado di stabilire il tipo di flusso da creare. I tipi più comuni di flussi usati nei file ASF sono i flussi audio e video. In Media Foundation i tipi di flusso sono identificati dall'oggetto del tipo di supporto che espone l'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Il tipo principale del tipo di supporto definisce la categoria del flusso multimediale digitale, ad esempio audio o video. Il sottotipo definisce il formato del tipo principale. Il tipo di supporto iniziale impostato da **CreateStream** può essere modificato usando l'oggetto configurazione di Steam. Per recuperare il tipo di supporto per il flusso, chiamare [**IMFASFStreamConfig:: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) o per recuperare la chiamata al tipo principale [**IMFASFStreamConfig:: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype). Il tipo di supporto iniziale per un flusso può essere sostituito con un nuovo tipo di supporto configurato chiamando [**IMFASFStreamConfig:: SetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setmediatype).

Se un'applicazione crea un profilo da un descrittore di presentazione valido chiamando [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor). La funzione imposta automaticamente gli oggetti di configurazione del flusso per ognuno dei flussi e li imposta sul profilo. I tipi di supporto del flusso vengono impostati in base ai descrittori di flusso associati al descrittore di presentazione.

## <a name="assigning-stream-numbers"></a>Assegnazione di numeri di flusso

È necessario assegnare un numero di flusso a flussi di tutti i tipi. I numeri di flusso non devono essere sequenziali, ma devono essere compresi tra 1 e 127. Per assegnare i numeri di flusso, chiamare [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber). Per ottenere la chiamata al numero di flusso, [**IMFASFStreamConfig:: GetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamnumber).

> [!Note]  
> Un numero di flusso è diverso da un indice del flusso, che è possibile usare quando si recuperano i flussi in un profilo usando [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream). L'indice del flusso è un numero assegnato al flusso dall'oggetto profilo. Gli indici di flusso sono compresi tra 0 e uno inferiore al numero di flussi recuperato da [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount). È anche possibile ottenere un flusso dal profilo per numero di flusso chiamando [**IMFASFProfile:: GetStreamByNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber).

 

## <a name="setting-leaky-bucket-values"></a>Impostazione dei valori bucket persi

A ogni oggetto di configurazione del flusso che rappresenta un flusso devono essere associati parametri di bucket di perdita, velocità in bit e valori della finestra del buffer.

Questi valori sono disponibili per l'applicazione tramite l'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) e l'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) . Per la codifica dei file, i valori effettivi dipendono dal tipo di codifica e vengono decisi dal codificatore. Se si dispone già di un codificatore configurato e il tipo di output è impostato sul codificatore, l'applicazione deve eseguire una query sul codificatore per i parametri di bucket a perdita e impostare i valori in questi attributi.

Se si utilizzano i componenti del livello pipeline e si configurano i flussi per il sink multimediale ASF, molto probabilmente non è presente un codificatore configurato. In questo caso, è necessario eseguire una query sui negoziatori dei tipi post-supporto del codificatore e impostare il valore aggiornato nella proprietà [**\_ \_ \_ LEAKYBUCKET ASFSTREAMSINK MFPKEY con correzione**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) dell'archivio delle proprietà del sink multimediale ASF. L'archivio delle proprietà di codifica viene recuperato tramite l'oggetto dell'oggetto ContentInfo associato al profilo. I valori aggiornati vengono riflessi automaticamente nei valori dell'attributo bucket Leaky del flusso. Per informazioni generali sui bucket a perdita e su come ottenere il valore del bucket di perdita dal codificatore, vedere il [modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md).

## <a name="payload-extensions"></a>Estensioni del payload

I dati multimediali per i flussi vengono aggiunti all'oggetto dati ASF come [esempi di supporto](media-samples.md) da parte di [ASF Multiplexer](asf-multiplexer.md). Questi esempi di supporti possono contenere dati di estensione del payload: dati del codice ora SMPTE, proporzioni di pixel non quadrati, durata del campione e se l'esempio lo contiene, un fotogramma chiave video. Per un elenco dei tipi di estensione del payload supportati, vedere [GUID dell'estensione del payload ASF](asf-payload-extension-guids.md).

Un flusso deve essere configurato per accettare l'estensione del payload in modo che durante la generazione di esempio il multiplexer possa aggiungere i dati supplementari a ogni esempio per quel flusso.

Per ottenere il numero totale di estensioni di payload impostate nel flusso, chiamare [**IMFASFStreamConfig:: GetPayloadExtensionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount) e quindi enumerare l'elenco chiamando [**IMFASFStreamConfig:: GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension). Per aggiungere l'estensione del payload per il flusso, chiamare [**IMFASFStreamConfig:: AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension). In questo modo vengono aggiunti dati supplementari ai singoli esempi di supporti generati per il flusso.

Per rimuovere le estensioni di payload esistenti associate al flusso, chiamare [**IMFASFStreamConfig:: RemoveAllPayloadExtensions**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-removeallpayloadextensions).

## <a name="adding-a-stream-to-the-profile"></a>Aggiunta di un flusso al profilo

Dopo la configurazione di un flusso, chiamare [**IMFASFProfile:: sestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) per aggiungere il flusso al profilo.

Per rimuovere un flusso esistente nel profilo, chiamare [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).

Il profilo configurato deve essere impostato sull'oggetto ContentInfo chiamando [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Se si apportano modifiche a un flusso esistente, è necessario aggiungerlo di nuovo al profilo e impostare il profilo sull'oggetto ContentInfo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Profilo ASF](asf-profile.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



