---
description: Questo argomento descrive il modo in cui una trasformazione Media Foundation (MFT) deve gestire le modifiche di formato durante il flusso.
ms.assetid: b0a94760-b4dd-4e50-a5ce-a1f674dde156
title: Gestione delle modifiche dei flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2adf3cbc0504a37fe611b77047c73f85b9d1e742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226461"
---
# <a name="handling-stream-changes"></a>Gestione delle modifiche dei flussi

Questo argomento descrive il modo in cui una trasformazione Media Foundation (MFT) deve gestire le modifiche di formato durante il flusso.

> [!IMPORTANT]
>
> Questo argomento non si applica ai codificatori. I codificatori non devono propagare le modifiche al formato, come descritto in questo argomento. I codificatori devono accettare solo un tipo di input corrispondente al tipo di output attualmente configurato.

 

## <a name="overview-of-format-changes"></a>Panoramica delle modifiche al formato

In genere, esistono due motivi per cui un formato può cambiare durante il flusso.

-   Il client può passare a un flusso con un nuovo formato. Ad esempio, in Digital Television questa situazione può verificarsi a causa di una modifica del canale.
-   In alcuni formati video, ad esempio H. 264, il bitstream può segnalare una modifica del formato. Tali modifiche possono includere modifiche al dominanza dei campi, alla risoluzione del video o alle proporzioni di pixel.

Se il tipo di codifica viene modificato, il client potrebbe dover rimuovere la MFT dalla pipeline e sostituirla con un'altra MFT. Ad esempio, potrebbe essere necessario scambiare il client in un nuovo decodificatore. Questo argomento non copre questa situazione. In questo argomento vengono illustrati solo i casi in cui il MFT corrente è in grado di gestire il nuovo formato.

Se il formato viene modificato, la MFT potrebbe richiedere un nuovo tipo di input, un nuovo tipo di output o entrambi.

-   Le modifiche apportate al tipo di input vengono avviate dal client. Un MFT non modifica mai il proprio tipo di input.
-   Le modifiche al tipo di output vengono avviate da MFT. Il MFT segnala che è necessario un nuovo tipo di output e il client negozia il nuovo tipo di output con MFT.

Sono pertanto possibili tre casi distinti:

-   Il client imposta un nuovo tipo di input. Il MFT usa il nuovo formato, senza alcuna modifica al tipo di output.
-   Il client imposta un nuovo tipo di input e attiva una modifica nel tipo di output.
-   Il tipo di input non cambia, ma il MFT rileva una modifica del formato in Bitstream, che richiede un nuovo tipo di output.

## <a name="implementing-format-changes"></a>Implementazione delle modifiche al formato

Nella parte restante di questo argomento viene descritto il modo in cui il client deve elaborare una modifica di formato e come implementare le modifiche al formato in un MFT.

### <a name="output-type"></a>Tipo di output

Qualsiasi MFT può avviare una modifica al tipo di output, come indicato di seguito:

1.  Il client chiama [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Il MFT risponde nel modo seguente:
    1.  MFT non produce un esempio di output in [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
    2.  MFT imposta il flag **di \_ \_ modifica del \_ \_ formato del \_ buffer dei dati di output MFT** nel membro **dwStatus** della struttura del [**\_ \_ \_ buffer dei dati di output di MFT**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) .
    3.  Il metodo [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) restituisce il codice di errore **MF E la \_ \_ \_ \_ modifica del flusso di trasformazione**.
2.  Il client chiama [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Questo metodo restituisce un set aggiornato di tipi di output.
3.  Il client chiama [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare un nuovo tipo di output.
4.  Il client riprende la chiamata a [**ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) / [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

### <a name="input-type"></a>Tipo di input

Le modifiche apportate al tipo di input vengono avviate dal client, mai dalla MFT. Se il tipo di input viene modificato, è possibile che venga attivata una modifica al tipo di output.

La sequenza esatta di eventi dipende dal valore dell'attributo di [**modifica del \_ \_ \_ formato \_ dinamico del supporto MFT**](mft-support-dynamic-format-change-attribute.md) .



| Valore     | Descrizione                                                     |
|-----------|-----------------------------------------------------------------|
| **FALSE** | Prima di impostare un nuovo tipo di input, il client deve svuotare il MFT. |
| **TRUE**  | Il client può impostare un nuovo tipo di input senza svuotare il MFT.   |



 

Un MFT espone questo attributo tramite il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Il valore predefinito di questo attributo è **false**; Se MFT non imposta l'attributo, considerare il valore come **false**.

**\_ \_ La modifica del formato dinamico del supporto MFT \_ \_ è false**

1.  Il client invia il messaggio di [**\_ svuotamento del \_ comando \_ del messaggio MFT**](mft-message-command-drain.md) .
2.  Il client svuota il MFT chiamando [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) fino a quando **ProcessOutput** restituisce **MF \_ E \_ Transform \_ necessita di un \_ maggiore \_ input**.
3.  Il client chiama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il nuovo tipo di input.
4.  Il MFT convalida il tipo di input. Se il tipo non è valido, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) restituisce **MF \_ E \_ INVALIDMEDIATYPE** o un altro codice di errore. In caso contrario, **SetInputType** restituisce S \_ OK.
5.  Supponendo che il tipo di input sia valido, la MFT valuta se il tipo di output cambia anche. In caso contrario, il flusso continua e non è richiesta alcuna azione aggiuntiva.
6.  Se il tipo di output cambia:
    1.  La MFT invalida il tipo di supporto di output corrente e aggiorna l'elenco dei tipi di supporti di output disponibili.
    2.  La chiamata successiva a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) restituisce **la \_ \_ modifica del \_ flusso \_ di trasformazione MF e**, come descritto nella sezione precedente.
    3.  Il client chiama [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere l'elenco aggiornato dei tipi di output.
    4.  Il client chiama [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

**\_ \_ La modifica del formato dinamico del supporto MFT \_ \_ è true**

1.  Il client chiama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il nuovo tipo di input.
2.  Il MFT convalida il tipo di input. Se il tipo non è valido, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) restituisce **MF \_ E \_ INVALIDMEDIATYPE** o un altro codice di errore. In caso contrario, **SetInputType** restituisce S \_ OK.
3.  Supponendo che il tipo di input sia valido, la MFT valuta se il tipo di output cambia anche. In caso contrario, il flusso continua e non è richiesta alcuna azione aggiuntiva.
4.  Prima della modifica del tipo di output, il MFT deve elaborare tutti gli esempi di input memorizzati nella cache, come indicato di seguito:
    1.  Il MFT non invalida il tipo di output corrente.
    2.  Il MFT produce il maggior volume di output possibile dagli esempi di input memorizzati nella cache.
    3.  È facoltativo se MFT accetta nuovi esempi di input mentre elabora gli esempi memorizzati nella cache. In tal caso, i nuovi esempi di input utilizzeranno il nuovo formato di input, quindi il MFT deve tenere traccia del punto in cui il formato è stato modificato.
5.  Quando MFT elabora tutti gli esempi ricevuti prima della modifica del tipo di input, [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) restituisce la modifica del **\_ flusso di \_ trasformazione \_ \_ MF E**.
6.  La MFT invalida il tipo di output corrente e aggiorna l'elenco dei tipi di supporti di output disponibili.
7.  Il client negozia il nuovo tipo di output, come descritto in precedenza.

[MFTS asincrono](asynchronous-mfts.md) deve restituire il valore **true** per l'attributo di [**\_ \_ \_ \_ modifica del formato dinamico del supporto MFT**](mft-support-dynamic-format-change-attribute.md) . Quando si usa un MFT asincrono, il client può presumere che l'attributo di **\_ \_ \_ \_ modifica del formato dinamico del supporto MFT** sia impostato su **true**.

Quando [**MFT \_ supporta \_ la \_ \_ modifica del formato dinamico**](mft-support-dynamic-format-change-attribute.md) è **true**, la differenza principale consiste nel fatto che il client non deve svuotare MFT prima di impostare un nuovo tipo di input. Di conseguenza, il tipo di input potrebbe cambiare mentre il MFT mantiene gli esempi di input. È importante che il MFT non elimini semplicemente questi esempi. Inoltre, il tipo di output non può essere modificato finché il MFT non elabora tutti i dati memorizzati nella cache.

Il paragrafo precedente si applica in particolare ai decodificatori video, che possono ricevere frame intercodificati fuori dall'ordine temporale e quindi devono memorizzarli nella cache. Se un MFT non memorizza nella cache gli esempi di input, lo svuotamento è essenzialmente un no-op. In tal caso, la MFT può impostare [**la \_ \_ modifica del \_ formato \_ dinamico del supporto MFT**](mft-support-dynamic-format-change-attribute.md) su **false** (o lasciare l'attributo non impostato).

Si noti anche che ogni MFT dovrebbe gestire correttamente le modifiche del formato dopo essere state svuotate. L'attributo di [**\_ \_ \_ \_ modifica del formato dinamico del supporto MFT**](mft-support-dynamic-format-change-attribute.md) indica se il MFT supporta le modifiche del formato senza svuotamento.

## <a name="change-in-interlace-mode"></a>Modifica in modalità interlacciata

Le modifiche alla modalità di interlacciamento video costituiscono un caso speciale, perché non invalidano il tipo di supporto corrente. Viene invece specificata la modalità interlacciamento per ogni fotogramma video impostando gli attributi nell'esempio multimediale. Un video MFT deve controllare ogni esempio di input per la presenza di questi flag.

La modalità interlacciamento può variare quando la dominanza del campo passa dal campo superiore a quello inferiore o quando il video passa tra immagini progressive e interlacciate.

Per altre informazioni, vedere [flag interlacciamento](video-interlacing.md)per gli esempi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 



