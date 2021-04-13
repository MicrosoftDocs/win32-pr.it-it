---
description: Configurazione del codec MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Configurazione del codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484100"
---
# <a name="configuring-codec-mfts"></a>Configurazione del codec MFTs

Questo argomento descrive il processo di configurazione del codec MFTs. Ogni codec ha procedure specifiche, ma le informazioni comuni a tutte sono descritte qui.

## <a name="configuring-mft-inputs-and-outputs"></a>Configurazione degli input e degli output di MFT

Ogni MFT supporta tipi di input e output specifici. È possibile recuperare i tipi di input supportati chiamando ripetutamente [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementando l'indice del tipo con ogni chiamata. Quando si trova un tipo appropriato, impostare il tipo di input chiamando [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype). È quindi possibile ripetere il processo per il tipo di output usando le chiamate a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) e [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). È necessario eseguire una query o impostare i tipi di output disponibili solo dopo aver impostato il tipo di input.

## <a name="configuring-the-codec-mfts-for-encoding"></a>Configurazione del codec MFTs per la codifica

Tutti i codec Windows Media Audio e video supportano un'ampia gamma di funzionalità di codifica. Queste funzionalità vengono in genere configurate impostando le proprietà in MFT usando i metodi dell'interfaccia **IPropertyStore** . Alcune proprietà vengono configurate utilizzando interfacce di codec specializzate. Queste interfacce sono elencate per ogni codec nella sezione [oggetti codec](codecobjects.md).

L'ordine generale delle operazioni per la configurazione di un MFT di codifica è il seguente:

1.  Configurare le funzionalità di codec come desiderato usando i metodi di **IPropertyStore**.
2.  Usare le interfacce del codec MFT per configurare le funzionalità aggiuntive, se necessario.
3.  Configurare i tipi di input e di output. L'ordine in cui devono essere configurati i tipi varia per i singoli codec. Per ulteriori informazioni, vedere [utilizzo di audio](workingwithaudio.md) e [utilizzo di video](workingwithvideo.md).

## <a name="configuring-the-codec-mfts-for-decoding"></a>Configurazione del codec MFTs per la decodifica

La decodifica è più semplice della codifica, in quanto sono supportate meno funzionalità di decodificatore.

L'ordine generale delle operazioni per la configurazione di un MFT di decodifica è il seguente:

1.  Configurare le funzionalità del decodificatore in base alle esigenze usando i metodi di **IPropertyStore**.
2.  Impostare il tipo di input sul tipo usato per l'output del codificatore.
3.  Configurare il tipo di output. I tipi di output supportati sono diversi per gli input diversi.

> [!Note]  
> È importante usare lo stesso tipo di supporto per l'input del decodificatore usato per l'output del codificatore. Ciò è dovuto al fatto che i codec Windows Media Audio e video usano formati multimediali con dati aggiuntivi. Senza i dati di formato esteso, non è possibile decodificare il contenuto compresso.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



