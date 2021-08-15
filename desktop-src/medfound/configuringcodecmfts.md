---
description: Configurazione dei codec MFT
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Configurazione dei codec MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb4a9ae53c0aee61e30fb5d61b2ad78fd4fe8e624df394f462dd01618272476
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743333"
---
# <a name="configuring-codec-mfts"></a>Configurazione dei codec MFT

Questo argomento descrive il processo di configurazione dei codec MFT. Ogni codec ha procedure specifiche, ma le informazioni comuni a tutti sono descritte qui.

## <a name="configuring-mft-inputs-and-outputs"></a>Configurazione di input e output MFT

Ogni MFT supporta tipi di input e output specifici. È possibile recuperare i tipi di input supportati chiamando ripetutamente [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementando l'indice dei tipi con ogni chiamata. Quando si trova un tipo appropriato, impostare il tipo di input chiamando [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype). È quindi possibile ripetere il processo per il tipo di output usando le chiamate [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) e [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). È necessario eseguire una query o impostare i tipi di output disponibili solo dopo aver impostato il tipo di input.

## <a name="configuring-the-codec-mfts-for-encoding"></a>Configurazione dei codec MFT per la codifica

Tutti i codec Windows audio e video multimediali supportano un'ampia gamma di funzionalità di codifica. Queste funzionalità vengono in genere configurate impostando le proprietà in MFT usando i metodi **dell'interfaccia IPropertyStore.** Alcune proprietà vengono configurate usando interfacce codec specializzate. Queste interfacce sono elencate per ogni codec nella sezione [Oggetti codec](codecobjects.md).

L'ordine generale delle operazioni per la configurazione di una codifica MFT è il seguente:

1.  Configurare le funzionalità del codec in base alle esigenze usando i metodi di **IPropertyStore**.
2.  Usare le interfacce MFT del codec per configurare funzionalità aggiuntive, se necessario.
3.  Configurare i tipi di input e output. L'ordine di configurazione dei tipi varia per i singoli codec. Per altre informazioni, vedere [Uso dell'audio e](workingwithaudio.md) [Uso di video.](workingwithvideo.md)

## <a name="configuring-the-codec-mfts-for-decoding"></a>Configurazione dei codec MFT per la decodifica

La decodifica è più semplice della codifica, poiché sono supportate meno funzionalità del decodificatore.

L'ordine generale delle operazioni per la configurazione di un MFT di decodifica è il seguente:

1.  Configurare le funzionalità del decodificatore in base alle esigenze usando i metodi di **IPropertyStore**.
2.  Impostare il tipo di input sul tipo usato per l'output del codificatore.
3.  Configurare il tipo di output. I tipi di output supportati sono diversi per input diversi.

> [!Note]  
> È importante usare lo stesso tipo di supporto per l'input del decodificatore usato per l'output del codificatore. Ciò è dovuto al Windows codec audio e video multimediali che usano formati multimediali con dati aggiuntivi. Senza i dati in formato esteso, non è possibile decodificare il contenuto compresso.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei codec MFT](workingwithcodecmfts.md)
</dt> </dl>

 

 



