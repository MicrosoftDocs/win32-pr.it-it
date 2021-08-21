---
title: Uso dei modelli di conformità dei dispositivi
description: Uso dei modelli di conformità dei dispositivi
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- profili, modelli di conformità dei dispositivi
- profili, modelli di conformità
- codec, modelli di conformità dei dispositivi
- codec, modelli di conformità
- modelli di conformità del dispositivo,informazioni
- modelli di conformità
- modelli, modelli di conformità dei dispositivi
- Advanced Systems Format (ASF), modelli di conformità dei dispositivi
- ASF (Advanced Systems Format),modelli di conformità dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e10bc09ccb72ae5b63894d3d7a943f377a0f45980186ab40178896425c733b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653263"
---
# <a name="working-with-device-conformance-templates"></a>Uso dei modelli di conformità dei dispositivi

A causa della grande flessibilità dei file ASF, spesso è difficile determinare se un file è appropriato per la riproduzione in un dispositivo specifico. Ad esempio, i file scritti per la riproduzione locale nei computer desktop non sono ottimali per l'uso nei dispositivi portatili. I modelli di conformità dei dispositivi consentono alle applicazioni di identificare rapidamente il tipo di dispositivo di riproduzione a cui era destinato un file. Se il modello di conformità del dispositivo non corrisponde al dispositivo, l'applicazione può informare l'utente che il file non è appropriato per il dispositivo. In questo modo, l'utente può avere la certezza di una migliore esperienza di riproduzione.

Se si scrivono file esclusivamente per l'uso nei personal computer, i modelli di conformità dei dispositivi non saranno un fattore determinante nella creazione dei profili. Lo scopo principale di questi modelli è garantire che i file creati per l'uso con hardware speciale siano compatibili con un'intera gamma di dispositivi e non con un singolo dispositivo.

Un modello di conformità del dispositivo è un'asserzione che un file ASF contiene dati codificati all'interno di determinati parametri. Per altre informazioni sulle impostazioni appropriate per i singoli modelli, vedere [Parametri del modello di conformità del dispositivo.](device-conformance-template-parameters.md)

I codec seguenti supportano i modelli di conformità dei dispositivi:

-   Windows Video multimediale 9
-   Windows Audio multimediale 9 e versioni successive
-   Windows Media Audio 9 Professional e versioni successive
-   Windows Audio multimediale 9 Voce

Non è necessario eseguire passaggi speciali per usare i modelli di conformità dei dispositivi. Il codec scrive automaticamente una stringa modello per ogni flusso appropriato nel file. Il codec deciderà quale modello usare, in base alle impostazioni di configurazione del flusso nel profilo. I parametri del modello di conformità del dispositivo si sovrappongono, quindi è possibile richiedere un modello specifico anziché consentire al codec di assegnarne uno automaticamente. È possibile specificare il modello desiderato impostando la proprietà g \_ wszDecoderComplexityRequested con i metodi [**dell'interfaccia IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso appropriato.

Quando viene scritto un file ASF, il modello di conformità del dispositivo effettivo per ogni flusso viene impostato sul valore passato al writer dal codec. Quando si apre un file per la lettura, è possibile individuare il modello a cui sono conformi i flussi del file usando i metodi [**dell'interfaccia IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) per recuperare l'attributo g \_ wszDeviceConformanceTemplate a livello di flusso. Per altre informazioni sugli attributi, vedere [Utilizzo dei metadati.](working-with-metadata.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Progettazione di profili**](designing-profiles.md)
</dt> <dt>

[**Parametri del modello di conformità del dispositivo**](device-conformance-template-parameters.md)
</dt> </dl>

 

 




