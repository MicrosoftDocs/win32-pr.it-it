---
description: Una risorsa è una raccolta di dati usata dalla pipeline 3D.
ms.assetid: 802400fa-a606-4d3d-a61d-1cdb5a9f0437
title: Scelta di una risorsa (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de635e9ad5ece322de9c34438be45db991e6700dc6192509f70b6b0f53e351b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119380321"
---
# <a name="choosing-a-resource-direct3d-10"></a>Scelta di una risorsa (Direct3D 10)

Una risorsa è una raccolta di dati usata dalla pipeline 3D. Creare risorse e definirne il comportamento è il primo passaggio per la programmazione dell'applicazione. Questa guida illustra gli argomenti di base per la scelta delle risorse richieste dall'applicazione.

-   [Identificare le fasi della pipeline che necessitano di risorse](#identify-pipeline-stages-that-need-resources)
-   [Identificare la modalità di utilizzo di ogni risorsa](#identify-how-each-resource-will-be-used)
-   [Associazione delle risorse alle fasi della pipeline](#binding-resources-to-pipeline-stages)
-   [Argomenti correlati](#related-topics)

## <a name="identify-pipeline-stages-that-need-resources"></a>Identificare le fasi della pipeline che necessitano di risorse

Il primo passaggio consiste nel scegliere la fase (o le fasi) della [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) che userà una risorsa. In altre informazioni, identificare ogni fase che leggerà i dati da una risorsa e le fasi che scriveranno i dati in una risorsa. Conoscere le fasi della pipeline in cui verranno usate le risorse determina le API che verranno chiamate per associare la risorsa alla fase.

Questa tabella elenca i tipi di risorse che possono essere associate a ogni fase della pipeline. Include se la risorsa può essere associata come input o output, nonché come API di associazione.



| Fase della pipeline  | Ingresso/Uscita | Risorsa               | Tipo di risorsa                           | API di associazione                                                                                                                                                                                                |
|-----------------|--------|------------------------|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Assembler input | In     | Vertex Buffer          | Buffer                                  | [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)                                                                                                                                           |
| Assembler input | In     | Buffer indice           | Buffer                                  | [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)                                                                                                                                               |
| Fasi shader   | In     | Shader-ResourceView    | Buffer, Texture1D, Texture2D, Texture3D | [**VSSetShaderResources,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshaderresources) [**GSSetShaderResources,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshaderresources) [**PSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshaderresources) |
| Fasi shader   | In     | Shader-Constant buffer | Buffer                                  | [**VSSetConstantBuffers,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers) [**GSSetConstantBuffers,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers) [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers) |
| Output del flusso   | In uscita    | Buffer                 | Buffer                                  | [**SOSetTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-sosettargets)                                                                                                                                                       |
| Unione output   | In uscita    | Visualizzazione destinazione di rendering     | Buffer, Texture1D, Texture2D, Texture3D | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |
| Unione output   | In uscita    | Visualizzazione Profondità/Stencil     | Texture1D, Texture2D                    | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |



 

## <a name="identify-how-each-resource-will-be-used"></a>Identificare la modalità di utilizzo di ogni risorsa

Dopo aver scelto le fasi della pipeline che verranno usate dall'applicazione (e quindi le risorse necessarie per ogni fase), il passaggio successivo consiste nel determinare come verrà usata ogni risorsa, ovvero se una risorsa può essere accessibile dalla CPU o dalla GPU.

L'hardware su cui è in esecuzione l'applicazione avrà almeno una CPU e una GPU. Per scegliere un valore di utilizzo, considerare quale tipo di processore deve leggere o scrivere nella risorsa tra le opzioni seguenti (vedere [**D3D10 \_ USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)).



| Resource Usage | Può essere aggiornato da                    | Frequenza di aggiornamento |
|----------------|--------------------------------------|---------------------|
| Predefinito        | GPU                                  | Raramente        |
| Dynamic        | CPU                                  | Frequentemente          |
| Gestione temporanea        | GPU                                  | n/d                 |
| Non modificabile      | CPU (solo al momento della creazione della risorsa) | n/d                 |



 

L'utilizzo predefinito deve essere usato per una risorsa che dovrebbe essere aggiornata raramente dalla CPU (meno di una volta per frame). Idealmente, la CPU non scriverebbe mai direttamente in una risorsa con l'utilizzo predefinito in modo da evitare potenziali penalità per le prestazioni.

L'utilizzo dinamico deve essere usato per una risorsa che la CPU aggiorna relativamente frequentemente (una o più volte per ogni frame). Uno scenario tipico per una risorsa dinamica consiste nel creare buffer di vertici e indici dinamici che verrebbero riempiti in fase di esecuzione con dati sulla geometria visibile dal punto di vista dell'utente per ogni frame. Questi buffer verranno usati per eseguire il rendering solo della geometria visibile all'utente per tale frame.

L'utilizzo dello staging deve essere usato per copiare dati da e verso altre risorse. Uno scenario tipico consiste nel copiare i dati in una risorsa con utilizzo predefinito (a cui la CPU non può accedere) in una risorsa con utilizzo di staging (a cui la CPU può accedere).

Le risorse non modificabili devono essere usate quando i dati nella risorsa non cambieranno mai.

Un altro modo per guardare la stessa idea è quello di pensare a cosa fa un'applicazione con una risorsa.



| Come l'applicazione usa la risorsa     | Resource Usage       |
|---------------------------------------|----------------------|
| Carica una sola volta e non aggiorna mai            | Non modificabile o predefinito |
| L'applicazione riempie ripetutamente la risorsa | Dynamic              |
| Eseguire il rendering su trama                     | Predefinito              |
| Accesso alla CPU dei dati GPU                | Gestione temporanea              |



 

Se non si è certi dell'utilizzo da scegliere, iniziare con l'utilizzo predefinito, in quanto si prevede che sia il caso più comune. Un Shader-Constant buffer è l'unico tipo di risorsa che deve avere sempre l'utilizzo predefinito.

## <a name="binding-resources-to-pipeline-stages"></a>Associazione delle risorse alle fasi della pipeline

Una risorsa può essere associata a più fasi della pipeline contemporaneamente, purché siano soddisfatte le restrizioni specificate al momento della creazione della risorsa [**(**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)flag di utilizzo [**,**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)flag di associazione , flag di accesso alla [**cpu**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)). In particolare, una risorsa può essere associata come input e un output contemporaneamente, purché la lettura e la scrittura di una parte di una risorsa non avvengano contemporaneamente.

Quando si associa una risorsa, è necessario pensare a come la GPU e la CPU accederanno alla risorsa. Le risorse progettate per un singolo scopo (non usano più flag di utilizzo, binding e accesso alla CPU) avranno probabilmente prestazioni migliori.

Si consideri, ad esempio, il caso di una destinazione di rendering usata più volte come trama. Potrebbe essere più veloce avere due risorse: una destinazione di rendering e una trama usata come risorsa shader. Ogni risorsa usa un solo flag di associazione ([**D3D10 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) o **D3D10 \_ BIND SHADER \_ \_ RESOURCE).** I dati vengono copiati dalla trama di destinazione di rendering alla trama dello shader usando [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) [**o CopySubresourceRegion.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) Questo può migliorare le prestazioni isolando la scrittura della destinazione di rendering dalla lettura della trama shader. Naturalmente, l'unico modo per assicurarsi è implementare entrambi gli approcci e misurare la differenza di prestazioni nell'applicazione specifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



