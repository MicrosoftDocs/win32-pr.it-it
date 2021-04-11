---
title: Uso dei modelli di conformità dei dispositivi
description: Uso dei modelli di conformità dei dispositivi
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- profili, modelli di conformità del dispositivo
- profili, modelli di conformità
- codec, modelli di conformità del dispositivo
- codec, modelli di conformità
- modelli di conformità del dispositivo, informazioni
- modelli di conformità
- modelli, modelli di conformità dei dispositivi
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117359"
---
# <a name="working-with-device-conformance-templates"></a>Uso dei modelli di conformità dei dispositivi

A causa dell'elevata flessibilità dei file ASF, è spesso difficile determinare se un file è adatto per la riproduzione in un dispositivo specifico. Ad esempio, i file scritti per la riproduzione locale nei computer desktop non sono ottimali per l'utilizzo nei dispositivi palmari. I modelli di conformità del dispositivo consentono alle applicazioni di identificare rapidamente il tipo di dispositivo di riproduzione per cui è previsto un file. Se il modello di conformità del dispositivo non corrisponde al dispositivo, l'applicazione può informare l'utente che il file non è appropriato per il dispositivo. In questo modo, l'utente può garantire una migliore esperienza di riproduzione.

Se i file vengono scritti esclusivamente per l'uso in Personal computer, i modelli di conformità dei dispositivi non saranno più fattori per la creazione di profili. Lo scopo principale di questi modelli è garantire che i file creati per l'uso con hardware speciale siano compatibili con un intero intervallo di dispositivi e non solo con un singolo dispositivo.

Un modello di conformità del dispositivo è un'asserzione che un file ASF contiene dati codificati all'interno di determinati parametri. Per altre informazioni sulle impostazioni appropriate per i singoli modelli, vedere [parametri di modello di conformità del dispositivo](device-conformance-template-parameters.md).

I codec seguenti supportano i modelli di conformità dei dispositivi:

-   Windows Media Video 9
-   Windows Media Audio 9 e versioni successive
-   Windows Media Audio 9 Professional e versioni successive
-   Windows Media Audio 9 Voice

Non è necessario eseguire alcun passaggio speciale per usare i modelli di conformità del dispositivo. Il codec scrive automaticamente una stringa di modello per ogni flusso appropriato nel file. Il codec deciderà il modello da usare, in base alle impostazioni di configurazione del flusso nel profilo. Ci sono alcune sovrapposizioni nei parametri del modello di conformità del dispositivo, quindi è possibile richiedere un modello specifico anziché consentire al codec di assegnarne uno. È possibile specificare il modello desiderato impostando la proprietà g \_ wszDecoderComplexityRequested con i metodi dell'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso appropriato.

Quando viene scritto un file ASF, il modello di conformità effettivo del dispositivo per ogni flusso viene impostato sul valore passato al writer dal codec. Quando si apre un file per la lettura, è possibile individuare il modello a cui i flussi del file sono conformi usando i metodi dell'interfaccia [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) per recuperare l' \_ attributo wszDeviceConformanceTemplate a livello di flusso g. Per ulteriori informazioni sugli attributi, vedere [utilizzo dei metadati](working-with-metadata.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Progettazione di profili**](designing-profiles.md)
</dt> <dt>

[**Parametri del modello di conformità del dispositivo**](device-conformance-template-parameters.md)
</dt> </dl>

 

 




