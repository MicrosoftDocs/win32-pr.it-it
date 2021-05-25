---
title: Configurazione dell'ambiente di programmazione Direct3D 12
description: Descrive l'installazione, gli strumenti e le librerie supportate che costituiscono un ambiente di sviluppo Direct3D 12 produttivo.
ms.assetid: B2288866-E95F-46B8-A7A1-19888F029C03
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7079207f91185cc14b37d9056a4fa813b251bce5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342816"
---
# <a name="direct3d-12-programming-environment-setup"></a>Configurazione dell'ambiente di programmazione Direct3D 12

Descrive l'installazione, gli strumenti e le librerie supportate che costituiscono un ambiente di sviluppo Direct3D 12 produttivo.

-   [Ambiente di sviluppo](#development-environment)
-   [Lingue supportate](#supported-languages)
-   [Strutture helper](#helper-structures)
-   [Libreria di gestione della memoria](#memory-management-library)
-   [Strumenti e librerie supportati](#supported-tools-and-libraries)
-   [Esempi](#samples)
-   [Livello di debug](#debug-layer)
-   [Video didattici](#educational-videos)
-   [Argomenti correlati](#related-topics)

## <a name="development-environment"></a>Ambiente di sviluppo

Le intestazioni e le librerie Direct3D 12 fanno parte di Windows 10 SDK. Non è necessario scaricare o installare separatamente per usare Direct3D 12.

Dopo aver installato il software Windows 10 SDK e Visual Studio, la configurazione dell'ambiente di programmazione Direct3D 12 è stata completata. Visual Studio 2019 è consigliato, perché includerà gli strumenti di debug della grafica D3D12, ma le versioni precedenti di Visual Studio per lo sviluppo di programmi.

Per usare [l'API Direct3D 12,](direct3d-12-reference.md)includere D3d12.h e collegarsi a D3d12.lib oppure eseguire una query dei punti di ingresso direttamente in D3d12.dll.

Sono disponibili le intestazioni e le librerie seguenti. Il percorso delle librerie statiche dipende dalla versione (a 32 o 64 bit) del Windows 10 in esecuzione nel computer.



| Nome del file di intestazione o di libreria | Descrizione                         | Percorso di installazione      |
|-----------------------------|-------------------------------------|-----------------------|
| D3d12.h                     | Intestazione dell'API Direct3D 12              | %WindowsSdkDir \\ include \% WindowsSDKVersion% \\ \um |
| D3d12.lib                   | Libreria stub api Direct3D 12 statica | %WindowsSdkDir \\ Lib \% WindowsSDKVersion% \\ \um\arch |
| D3d12.dll                   | Libreria API Direct3D 12 dinamica     | %WINDIR% \\ System32    |
| D3d12SDKLayers.h            | Intestazione di debug Direct3D 12            | %WindowsSdkDir \\ include \% WindowsSDKVersion% \\ \um |
| D3d12SDKLayers.dll          | Libreria di debug Direct3D 12 dinamica   | %WINDIR% \\ System32    |



## <a name="supported-languages"></a>Linguaggi supportati

C++ è l'unico linguaggio supportato per lo sviluppo Direct3D 12, C# e altri linguaggi .NET non sono supportati.

## <a name="helper-structures"></a>Strutture helper

Esistono una serie di strutture helper che, in particolare, semplificano l'inizializzazione di alcune strutture D3D12. Queste strutture e alcune funzioni di utilità sono nell'intestazione D3dx12.h. Questa intestazione è open source e può essere modificata da uno sviluppatore in base alle esigenze. Scaricarla dalla libreria helper [D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12) e fare riferimento a Strutture e funzioni helper per [D3D12.](helper-structures-and-functions-for-d3d12.md)

## <a name="memory-management-library"></a>Libreria di gestione della memoria

È disponibile per il download una libreria helper di gestione della memoria che è possibile integrare nell'app per ottenere una corrispondenza più stretta con il comportamento di gestione della memoria D3D11. In quanto libreria di gestione dello stile D3D11, è più efficace con le app che usano ancora una *strategia* di allocazione dello stile di risorsa di cui è stato eseguito il commit. In particolare, la libreria deve essere considerata come un passo avanti che consente di tornare alla gestione della memoria con prestazioni D3D11 in scenari con vincoli di memoria,ad esempio schede di memoria di fascia bassa, 4K, impostazioni Ultra e così via. Le API D3D12 abilitano tecniche che consentono di ottenere una migliore efficienza della memoria rispetto a D3D11, anche se queste tecniche possono essere difficili e dispendiose in termini di tempo da implementare.

Si noti che questa libreria è in corso e può cambiare nel tempo. Usare i collegamenti seguenti per accedere alla libreria e agli esempi.

-   [Libreria D3D12 Residency Starter](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries)

## <a name="supported-tools-and-libraries"></a>Strumenti e librerie supportati

Con Direct3D 12 è possibile usare tutte le librerie seguenti.



| Libreria                                                                                 |  Scopo                                                                                                                                                                                                                                                                      | Documentazione                                                                                                           |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Kit di strumenti DirectX per DirectX 12](https://github.com/Microsoft/DirectXTK12) | Una raccolta sostanziale di classi helper per la scrittura di codice C++ Direct3D 12 per app piattaforma UWP (Universal Windows Platform) (UWP), applicazioni desktop Win32 per Windows 10 e Xbox One app esclusive.                                                                         | [Wiki di DirectX12TK](https://github.com/Microsoft/DirectXTK12/wiki)                                          |
| [DirectXTex](https://github.com/Microsoft/DirectXTex)                      | Usare questa opzione per la lettura e la scrittura di file DDS e per l'esecuzione di varie operazioni di elaborazione del contenuto della trama, tra cui ridimensionamento, conversione del formato, generazione di mappe mip, compressione a blocchi per le risorse trame di runtime Direct3D e conversione della mappa dell'altezza alla normale mappa. | [Wiki di DirectXTex](https://github.com/Microsoft/DirectXTex/wiki)                                            |
| [DirectXMesh](https://github.com/Microsoft/DirectXMesh)                   | Usare questa opzione per eseguire diverse operazioni di elaborazione del contenuto geometrico, tra cui la generazione di normali e fotogrammi tangenti, i calcoli di adizia dei triangoli e l'ottimizzazione della cache dei vertici.                                                                                | [Wiki di DirectXMesh](https://github.com/Microsoft/DirectXMesh/wiki)                                          |
| [DirectXMath](https://github.com/Microsoft/DirectXMath)                     | Un numero elevato di classi helper e metodi per supportare vettori, scalari, matrici, quaternioni e molte altre operazioni matematiche.                                                                                                                               | [Documentazione di DirectXMath in MSDN](/windows/desktop/dxmath/ovw-xnamath-progguide) |
| [UVAtlas](https://github.com/Microsoft/UVAtlas)                         | Usare questa opzione per creare e imballare un at atlas di trama isochart.                                                                                                                                                                                                           | [Wiki di UVAtlas](https://github.com/Microsoft/UVAtlas/wiki)                                                  |



 

## <a name="samples"></a>Esempi

Per un elenco di esempi D3D12 funzionanti e su come individuarli ed eseguirli, vedere [Esempi di lavoro](working-samples.md).

Per informazioni su come aggiungere codice per abilitare funzionalità specifiche, vedere [D3D12 Code Walk-Throughs](d3d12-code-walk-throughs.md).

## <a name="debug-layer"></a>Livello di debug

Il livello di debug offre un'ampia convalida aggiuntiva dei parametri e della coerenza, ad esempio la convalida del collegamento dello shader e dell'associazione di risorse, la convalida della coerenza dei parametri e la segnalazione di descrizioni degli errori.

> [!Note]  
> Per Windows 10, per creare un dispositivo che supporta il livello di debug, abilitare la funzionalità facoltativa "Strumenti di grafica". Passare al pannello Impostazioni, in Sistema, App & funzionalità, Gestisci funzionalità facoltative, Aggiungi una funzionalità e quindi cercare "Strumenti di grafica".

L'intestazione necessaria per supportare il livello di debug, D3D12SDKLayers.h, è inclusa per impostazione predefinita da d3d12.h.

Quando il livello di debug elenca le perdite di memoria, restituisce un elenco di puntatori a interfaccia oggetto insieme ai relativi nomi descrittivi. Il nome descrittivo predefinito è " &lt; senza &gt; nome ". È possibile impostare il nome descrittivo usando il [**metodo ID3D12Object::SetName.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) In genere, è consigliabile compilare queste chiamate dalla versione di produzione.

È consigliabile usare il livello di debug per eseguire il debug delle app per assicurarsi che siano pulite da errori e avvisi. Il livello di debug consente di scrivere codice Direct3D 12. Inoltre, la produttività può aumentare quando si usa il livello di debug, perché è possibile vedere immediatamente le cause di errori di rendering nascosti o persino di schermate nere all'origine. Il livello di debug fornisce avvisi per molti problemi. Ad esempio:

-   Si è dimenticato di impostare una trama, ma di leggerla nel pixel shader.
-   Profondità di output ma senza stato depth-stencil associato.
-   Creazione della trama non riuscita con INVALIDARG.

Impostare il compilatore define D3DCOMPILE DEBUG per indicare al compilatore \_ HLSL di includere le informazioni di debug nel BLOB dello shader.

``` syntax
#define D3DCOMPILE_DEBUG 1
```

Per informazioni dettagliate su tutte le interfacce e i metodi di debug, vedere Debug Layer Reference (Informazioni di [riferimento sul livello di debug).](direct3d-12-sdklayers-reference.md)

Per informazioni generali sull'uso del livello di debug, vedere [Informazioni sul livello di debug D3D12.](understanding-the-d3d12-debug-layer.md)

## <a name="educational-videos"></a>Video didattici

Sono disponibili diversi video correlati a Direct3D 12 e Windows 10 in Esercitazioni video di apprendimento avanzato di [DirectX,](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)inclusi i video sugli strumenti di debug della grafica e la segnalazione di bug grafici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 