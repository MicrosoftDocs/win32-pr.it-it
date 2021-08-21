---
description: In questo argomento viene descritto come una trasformazione Media Foundation (MFT) deve gestire le modifiche del formato durante il flusso.
ms.assetid: b0a94760-b4dd-4e50-a5ce-a1f674dde156
title: Gestione delle modifiche ai flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e238073bf518bc875b7b2d536c758eab48c8502278aae6780999c7616430337e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974430"
---
# <a name="handling-stream-changes"></a>Gestione delle modifiche ai flussi

In questo argomento viene descritto come una trasformazione Media Foundation (MFT) deve gestire le modifiche del formato durante il flusso.

> [!IMPORTANT]
>
> Questo argomento non si applica ai codificatori. I codificatori non devono propagare le modifiche al formato come descritto in questo argomento. I codificatori devono accettare solo un tipo di input corrispondente al tipo di output attualmente configurato.

 

## <a name="overview-of-format-changes"></a>Panoramica delle modifiche al formato

In genere, esistono due motivi per cui un formato può cambiare durante il flusso.

-   Il client potrebbe passare a un flusso con un nuovo formato. Ad esempio, nel digital tv ciò può verificarsi a causa di una modifica del canale.
-   In alcuni formati video, ad esempio H.264, il flusso di bit può segnalare una modifica del formato. Tali modifiche possono includere modifiche nella dominanza del campo, nella risoluzione video o nelle proporzioni dei pixel.

Se il tipo di codifica cambia, il client potrebbe dover rimuovere MFT dalla pipeline e sostituirlo con un altro MFT. Ad esempio, il client potrebbe dover scambiare un nuovo decodificatore. In questo argomento non viene trattata tale situazione. In questo argomento viene illustrato solo il caso in cui il MFT corrente può gestire il nuovo formato.

Se il formato cambia, il MFT potrebbe richiedere un nuovo tipo di input, un nuovo tipo di output o entrambi.

-   Le modifiche al tipo di input vengono avviate dal client. Un MFT non modifica mai il proprio tipo di input.
-   Le modifiche al tipo di output vengono avviate da MFT. MFT segnala che è necessario un nuovo tipo di output e il client negozia il nuovo tipo di output con MFT.

Di conseguenza, sono possibili tre casi distinti:

-   Il client imposta un nuovo tipo di input. MFT utilizza il nuovo formato, senza alcuna modifica al tipo di output.
-   Il client imposta un nuovo tipo di input e viene attivata una modifica nel tipo di output.
-   Il tipo di input non cambia, ma MFT rileva una modifica del formato nel flusso di bit, che richiede un nuovo tipo di output.

## <a name="implementing-format-changes"></a>Implementazione delle modifiche al formato

Nella parte restante di questo argomento viene descritto come il client deve elaborare una modifica del formato e come implementare le modifiche di formato in un MFT.

### <a name="output-type"></a>Tipo di output

Qualsiasi MFT può avviare una modifica al tipo di output, come indicato di seguito:

1.  Il client chiama [**IMFTransform::P rocessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) MFT risponde come segue:
    1.  MFT non produce un esempio di output in [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
    2.  MFT imposta il flag **MFT \_ OUTPUT DATA BUFFER FORMAT \_ \_ \_ \_ CHANGE** nel membro **dwStatus** della [**struttura MFT OUTPUT DATA \_ \_ \_ BUFFER.**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer)
    3.  Il [**metodo ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) restituisce il codice di errore **MF E TRANSFORM STREAM \_ \_ \_ \_ CHANGE**.
2.  Il client chiama [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Questo metodo restituisce un set aggiornato di tipi di output.
3.  Il client chiama [**SetOutputType per**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) impostare un nuovo tipo di output.
4.  Il client riprende a chiamare [**ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) / [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

### <a name="input-type"></a>Tipo di input

Le modifiche al tipo di input vengono avviate dal client, mai dal MFT. Se il tipo di input viene modificato, potrebbe essere attivata una modifica al tipo di output.

La sequenza esatta di eventi dipende dal valore [**dell'attributo MFT \_ SUPPORT DYNAMIC FORMAT \_ \_ \_ CHANGE.**](mft-support-dynamic-format-change-attribute.md)



| Valore     | Descrizione                                                     |
|-----------|-----------------------------------------------------------------|
| **FALSE** | Prima di impostare un nuovo tipo di input, il client deve svuotare il MFT. |
| **TRUE**  | Il client può impostare un nuovo tipo di input senza svuotare il MFT.   |



 

Un MFT espone questo attributo tramite il relativo [**metodo IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Il valore predefinito di questo attributo è **FALSE.** se MFT non imposta l'attributo , considerare il valore **come FALSE.**

**MFT \_ SUPPORT \_ DYNAMIC \_ FORMAT \_ CHANGE is FALSE**

1.  Il client invia il [**messaggio MFT \_ MESSAGE COMMAND \_ \_ DRAIN.**](mft-message-command-drain.md)
2.  Il client svuota MFT chiamando [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) finché **ProcessOutput** non restituisce **MF \_ E TRANSFORM NEED MORE \_ \_ \_ \_ INPUT**.
3.  Il client chiama [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il nuovo tipo di input.
4.  MFT convalida il tipo di input. Se il tipo non è valido, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) restituisce **MF \_ E \_ INVALIDMEDIATYPE** o un altro codice di errore. In caso contrario, **SetInputType** restituisce S \_ OK.
5.  Supponendo che il tipo di input sia valido, il MFT valuta se viene modificato anche il tipo di output. In caso contrario, lo streaming continua e non sono necessarie altre azioni.
6.  Se il tipo di output cambia:
    1.  MFT invalida il tipo di supporto di output corrente e aggiorna l'elenco dei tipi di supporti di output disponibili.
    2.  La chiamata successiva a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) restituisce **MF \_ E TRANSFORM \_ STREAM \_ \_ CHANGE,** come descritto nella sezione precedente.
    3.  Il client chiama [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere l'elenco aggiornato dei tipi di output.
    4.  Il client chiama [**SetOutputType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)

**MFT \_ SUPPORT \_ DYNAMIC \_ FORMAT \_ CHANGE is TRUE**

1.  Il client chiama [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il nuovo tipo di input.
2.  MFT convalida il tipo di input. Se il tipo non è valido, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) restituisce **MF \_ E \_ INVALIDMEDIATYPE** o un altro codice di errore. In caso contrario, **SetInputType** restituisce S \_ OK.
3.  Supponendo che il tipo di input sia valido, il MFT valuta se viene modificato anche il tipo di output. In caso contrario, lo streaming continua e non sono necessarie altre azioni.
4.  Prima della modifica del tipo di output, il MFT deve elaborare tutti gli esempi di input memorizzati nella cache, come indicato di seguito:
    1.  MFT non invalida il tipo di output corrente.
    2.  MFT produce la quantità di output possibile dagli esempi di input memorizzati nella cache.
    3.  È facoltativo se MFT accetta nuovi esempi di input durante l'elaborazione degli esempi memorizzati nella cache. In tal caso, i nuovi esempi di input useranno il nuovo formato di input, quindi il MFT deve tenere traccia del punto in cui è stato modificato il formato.
5.  Dopo l'elaborazione di tutti gli esempi ricevuti prima della modifica del tipo di input, [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) restituisce **MF \_ E TRANSFORM STREAM \_ \_ \_ CHANGE**.
6.  MFT invalida il tipo di output corrente e aggiorna l'elenco dei tipi di supporti di output disponibili.
7.  Il client negozia il nuovo tipo di output, come descritto in precedenza.

[I MFT asincroni](asynchronous-mfts.md) devono restituire il **valore TRUE** per [**l'attributo MFT \_ SUPPORT DYNAMIC FORMAT \_ \_ \_ CHANGE.**](mft-support-dynamic-format-change-attribute.md) Quando si usa un MFT asincrono, il client può presupporre che **l'attributo MFT \_ SUPPORT DYNAMIC FORMAT \_ \_ \_ CHANGE** sia impostato su **TRUE.**

Quando [**MFT \_ SUPPORT DYNAMIC \_ FORMAT \_ \_ CHANGE**](mft-support-dynamic-format-change-attribute.md) è **TRUE,** la differenza principale è che il client non deve svuotare il MFT prima di impostare un nuovo tipo di input. Di conseguenza, il tipo di input potrebbe cambiare mentre MFT tiene i campioni di input. È importante che il MFT non si limita a eliminare questi esempi. Inoltre, il tipo di output non può cambiare fino a quando il MFT non elabora tutti i dati memorizzati nella cache.

Il paragrafo precedente si applica soprattutto ai decodificatori video, che possono ricevere fotogrammi inter-codificati in ordine temporale e quindi devono essere memorizzati nella cache. Se un MFT non memorizza nella cache i campioni di input, lo svuotamento è essenzialmente un'operazione no-op. In tal caso, MFT può impostare [**MFT \_ SUPPORT DYNAMIC \_ FORMAT \_ \_ CHANGE**](mft-support-dynamic-format-change-attribute.md) su **FALSE** (o lasciare l'attributo non impostato).

Si noti inoltre che è previsto che ogni MFT gestirà correttamente le modifiche di formato dopo lo svuotamento. [**L'attributo MFT \_ SUPPORT DYNAMIC FORMAT \_ \_ \_ CHANGE**](mft-support-dynamic-format-change-attribute.md) indica se MFT supporta le modifiche al formato senza svuotamento.

## <a name="change-in-interlace-mode"></a>Modifica della modalità interlacciato

Le modifiche nella modalità di interlacciamento video sono un caso speciale, perché non invalidano il tipo di contenuto multimediale corrente. Al contrario, la modalità interlacciato viene specificata per ogni fotogramma video impostando gli attributi nell'esempio multimediale. Un video MFT deve controllare la presenza di questi flag in ogni esempio di input.

La modalità interlacciamento può cambiare quando la dominanza del campo passa dal campo superiore al campo inferiore o quando il video passa da immagini progressive a immagini interlacciate e progressive.

Per altre informazioni, vedere [Flag interlacciati sugli esempi.](video-interlacing.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 



