---
description: Una risorsa è una raccolta di dati usata dalla pipeline 3D.
ms.assetid: 802400fa-a606-4d3d-a61d-1cdb5a9f0437
title: Scelta di una risorsa (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be887fb94f04783b01f8873fb61812bca20faa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748967"
---
# <a name="choosing-a-resource-direct3d-10"></a>Scelta di una risorsa (Direct3D 10)

Una risorsa è una raccolta di dati usata dalla pipeline 3D. La creazione di risorse e la definizione del relativo comportamento è il primo passo verso la programmazione dell'applicazione. Questa guida illustra gli argomenti di base per la scelta delle risorse richieste dall'applicazione.

-   [Identificare le fasi della pipeline che necessitano di risorse](#identify-pipeline-stages-that-need-resources)
-   [Identificare il modo in cui ogni risorsa verrà utilizzata](#identify-how-each-resource-will-be-used)
-   [Associazione di risorse alle fasi della pipeline](#binding-resources-to-pipeline-stages)
-   [Argomenti correlati](#related-topics)

## <a name="identify-pipeline-stages-that-need-resources"></a>Identificare le fasi della pipeline che necessitano di risorse

Il primo passaggio consiste nel scegliere la [fase](d3d10-graphics-programming-guide-pipeline-stages.md) o le fasi della pipeline che utilizzeranno una risorsa. Ovvero identificare ogni fase che leggerà i dati da una risorsa e le fasi in cui i dati vengono scritti in una risorsa. Conoscere le fasi della pipeline in cui verranno usate le risorse determina le API che verranno chiamate per associare la risorsa alla fase.

Questa tabella elenca i tipi di risorse che è possibile associare a ogni fase della pipeline. Indica se la risorsa può essere associata come input o come output, nonché l'API bind.



| Fase pipeline  | Ingresso/Uscita | Risorsa               | Tipo di risorsa                           | API bind                                                                                                                                                                                                |
|-----------------|--------|------------------------|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Assembler input | In     | Buffer vertex          | Buffer                                  | [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)                                                                                                                                           |
| Assembler input | In     | Buffer indice           | Buffer                                  | [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)                                                                                                                                               |
| Fasi dello shader   | In     | Shader-ResourceView    | Buffer, Texture1D, Texture2D, Texture3D | [**VSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshaderresources), [**GSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshaderresources), [**PSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshaderresources) |
| Fasi dello shader   | In     | Buffer Shader-Constant | Buffer                                  | [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers), [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers) |
| Output flusso   | In uscita    | Buffer                 | Buffer                                  | [**SOSetTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-sosettargets)                                                                                                                                                       |
| Unione output   | In uscita    | Visualizzazione destinazione rendering     | Buffer, Texture1D, Texture2D, Texture3D | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |
| Unione output   | In uscita    | Visualizzazione profondità/stencil     | Texture1D, Texture2D                    | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |



 

## <a name="identify-how-each-resource-will-be-used"></a>Identificare il modo in cui ogni risorsa verrà utilizzata

Dopo aver scelto le fasi della pipeline che verranno usate dall'applicazione (e quindi le risorse necessarie per ogni fase), il passaggio successivo consiste nel determinare la modalità di utilizzo di ogni risorsa, ovvero se è possibile accedere a una risorsa dalla CPU o dalla GPU.

L'hardware su cui è in esecuzione l'applicazione avrà almeno una CPU e una GPU. Per selezionare un valore di utilizzo, valutare il tipo di processore che deve leggere o scrivere nella risorsa dalle opzioni seguenti (vedere [**\_ utilizzo di D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)).



| Resource Usage | Può essere aggiornato da                    | Frequenza di aggiornamento |
|----------------|--------------------------------------|---------------------|
| Predefinito        | GPU                                  | raramente        |
| Dynamic        | CPU                                  | frequente          |
| Staging        | GPU                                  | n/d                 |
| Non modificabile      | CPU (solo al momento della creazione delle risorse) | n/d                 |



 

Usare l'utilizzo predefinito per una risorsa che dovrebbe essere aggiornata raramente dalla CPU (meno di una volta per frame). Idealmente, la CPU non scriverebbe mai direttamente in una risorsa con utilizzo predefinito, in modo da evitare possibili penalizzazioni delle prestazioni.

L'utilizzo dinamico deve essere usato per una risorsa che la CPU aggiorna relativamente spesso (una o più volte per frame). Uno scenario tipico per una risorsa dinamica consiste nel creare buffer di indice e vertex dinamici che verrebbero compilati in fase di esecuzione con dati sulla geometria visibile dal punto di vista dell'utente per ogni frame. Questi buffer verrebbero usati per eseguire il rendering solo della geometria visibile all'utente per quel frame.

L'utilizzo della gestione temporanea deve essere utilizzato per copiare dati da e verso altre risorse. Uno scenario tipico consiste nel copiare i dati in una risorsa con utilizzo predefinito (a cui la CPU non può accedere) a una risorsa con utilizzo di gestione temporanea (a cui la CPU può accedere).

Le risorse non modificabili devono essere usate quando i dati nella risorsa non verranno mai modificati.

Un altro modo per esaminare la stessa idea è pensare a cosa fa un'applicazione con una risorsa.



| Modalità di utilizzo della risorsa da parte dell'applicazione     | Resource Usage       |
|---------------------------------------|----------------------|
| Carica una sola volta e non aggiorna mai            | Non modificabile o predefinito |
| L'applicazione riempie più volte la risorsa | Dynamic              |
| Esegui rendering in trama                     | Predefinito              |
| Accesso alla CPU dei dati GPU                | Staging              |



 

Se non si è certi dell'utilizzo da scegliere, iniziare con l'utilizzo predefinito perché si prevede che sia il caso più comune. Un buffer di Shader-Constant è un tipo di risorsa che deve avere sempre l'utilizzo predefinito.

## <a name="binding-resources-to-pipeline-stages"></a>Associazione di risorse alle fasi della pipeline

Una risorsa può essere associata a più di una fase della pipeline contemporaneamente, purché siano soddisfatte le restrizioni specificate al momento della creazione della risorsa (flag di [**utilizzo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**flag di binding**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag), flag di [**accesso alla CPU**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)). In particolare, una risorsa può essere associata come input e come output contemporaneamente, purché la lettura e la scrittura della parte di una risorsa non possano avvenire nello stesso momento.

Quando si associa una risorsa, è opportuno considerare il modo in cui la GPU e la CPU accedono alla risorsa. Le risorse progettate per un singolo scopo (non usare più flag di utilizzo, di binding e di accesso alla CPU) otterranno prestazioni migliori.

Si consideri ad esempio il caso di una destinazione di rendering utilizzata più volte come trama. Potrebbe essere più veloce avere due risorse: una destinazione di rendering e una trama usata come risorsa dello shader. Ogni risorsa utilizzerebbe un solo flag di binding [**( \_ D3D10 \_ binding \_ target rendering**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) o **D3D10 \_ Bind \_ shader \_ Resource**). I dati verrebbero copiati dalla trama di destinazione di rendering alla trama dello shader tramite [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Questo può migliorare le prestazioni isolando la scrittura della destinazione di rendering dalla lettura della trama dello shader. Naturalmente, l'unico modo per assicurarsi consiste nell'implementare entrambi gli approcci e misurare la differenza delle prestazioni nell'applicazione specifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



