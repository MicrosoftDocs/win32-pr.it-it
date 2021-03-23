---
title: Configurazione dell'ambiente di programmazione Direct3D 12
description: Descrive l'installazione, gli strumenti e le librerie supportate che costituiscono un ambiente di sviluppo Direct3D 12 produttivo.
ms.assetid: B2288866-E95F-46B8-A7A1-19888F029C03
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e6af0d0a93d55f700478ec839f3864ee0efbcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548891"
---
# <a name="direct3d-12-programming-environment-setup"></a>Configurazione dell'ambiente di programmazione Direct3D 12

Descrive l'installazione, gli strumenti e le librerie supportate che costituiscono un ambiente di sviluppo Direct3D 12 produttivo.

-   [Ambiente di sviluppo](#development-environment)
-   [Lingue supportate](#supported-languages)
-   [Strutture Helper](#helper-structures)
-   [Libreria di gestione della memoria](#memory-management-library)
-   [Strumenti e librerie supportati](#supported-tools-and-libraries)
-   [Esempi](#samples)
-   [Livello di debug](#debug-layer)
-   [Video didattici](#educational-videos)
-   [Argomenti correlati](#related-topics)

## <a name="development-environment"></a>Ambiente di sviluppo

Le intestazioni e le librerie di Direct3D 12 fanno parte di Windows 10 SDK. Non è necessario scaricare o installare separatamente per usare Direct3D 12.

Dopo aver installato il software Windows 10 SDK e Visual Studio, la configurazione dell'ambiente di programmazione Direct3D 12 è stata completata. È consigliabile usare Visual Studio 2019, in quanto includerà gli strumenti di debug della grafica D3D12, ma le versioni precedenti di Visual Studio funzioneranno per lo sviluppo di programmi.

Per usare l' [API Direct3D 12](direct3d-12-reference.md), includere D3d12. h e il collegamento a D3d12. lib oppure eseguire una query sui punti di ingresso direttamente in D3d12.dll.

Sono disponibili le intestazioni e le librerie seguenti. Il percorso delle librerie statiche dipende dalla versione (32 bit o 64 bit) di Windows 10 in esecuzione nel computer.



| Nome file di intestazione o di libreria | Descrizione                         | Percorso di installazione      |
|-----------------------------|-------------------------------------|-----------------------|
| D3d12. h                     | Intestazione dell'API Direct3D 12              | % WindowsSdkDir \\ includere \% WindowsSDKVersion% \\ \um |
| D3d12. lib                   | Libreria stub API Direct3D 12 statica | % WindowsSdkDir \\ lib \% WindowsSDKVersion% \\ \um\arch |
| D3d12.dll                   | Libreria API Direct3D 12 dinamica     | % WINDIR% \\ system32    |
| D3d12SDKLayers. h            | Intestazione di debug Direct3D 12            | % WindowsSdkDir \\ includere \% WindowsSDKVersion% \\ \um |
| D3d12SDKLayers.dll          | Libreria di debug Direct3D 12 dinamica   | % WINDIR% \\ system32    |



## <a name="supported-languages"></a>Lingue supportate

C++ è l'unico linguaggio supportato per lo sviluppo Direct3D 12, C# e altri linguaggi .NET non sono supportati.

## <a name="helper-structures"></a>Strutture Helper

Sono disponibili numerose strutture di supporto che, in particolare, semplificano l'inizializzazione di un numero di strutture D3D12. Queste strutture e alcune funzioni di utilità si trovano nell'intestazione D3dx12. h. Questa intestazione è open source e può essere modificata da uno sviluppatore come richiesto. scaricarla dalla [libreria helper D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12) e fare riferimento alle [strutture e alle funzioni di supporto per D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="memory-management-library"></a>Libreria di gestione della memoria

Una libreria helper di gestione della memoria è disponibile per il download che è possibile integrare nell'app per trovare più vicino il comportamento di gestione della memoria D3D11. Come libreria di gestione dello stile D3D11, è più efficace per le app che usano ancora una strategia di allocazione dello stile *delle risorse vincolata* . In particolare, la libreria deve essere considerata come un trampolino di avanzamento che consente di ottenere la maggior parte delle D3D11 di gestione della memoria in caso di scenari con vincoli di memoria, ad esempio schede di memoria di fascia bassa, 4K, impostazioni Ultra e così via. Le API D3D12 consentono tecniche che consentono di ottenere una maggiore efficienza di memoria rispetto a D3D11, anche se queste tecniche possono essere complesse e richiedere molto tempo per implementare.

Si noti che questa libreria è un lavoro in corso e può cambiare nel tempo. Usare i collegamenti seguenti per accedere alla libreria ed esempi.

-   [Libreria Starter di D3D12 Residency](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries)

## <a name="supported-tools-and-libraries"></a>Strumenti e librerie supportati

Con Direct3D 12 è possibile usare tutte le librerie seguenti.



|                                                                                  |                                                                                                                                                                                                                                                                        |                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Libreria**                                                                      | **Scopo**                                                                                                                                                                                                                                                            | **Documentazione**                                                                                          |
| [DirectX Tool Kit per DirectX 12](https://github.com/Microsoft/DirectXTK12) | Una raccolta sostanziale di classi helper per la scrittura di codice Direct3D 12 C++ per app piattaforma UWP (Universal Windows Platform) (UWP), applicazioni desktop Win32 per Windows 10 e app esclusive per Xbox One.                                                                         | [Wiki DirectX12TK](https://github.com/Microsoft/DirectXTK12/wiki)                                          |
| [DirectXTex](https://github.com/Microsoft/DirectXTex)                      | Usare questa utilità per la lettura e la scrittura di file DDS e per l'esecuzione di varie operazioni di elaborazione del contenuto di trama, tra cui il ridimensionamento, la conversione del formato, la generazione di mappe MIP, la compressione dei blocchi per le risorse di trama di runtime Direct3D e il mapping dell'altezza alla conversione | [Wiki DirectXTex](https://github.com/Microsoft/DirectXTex/wiki)                                            |
| [DirectXMesh](https://github.com/Microsoft/DirectXMesh)                   | Usare questa opzione per eseguire varie operazioni di elaborazione del contenuto geometrico, tra cui la generazione di normali e di frame tangenti, calcoli adiacenza del triangolo e l'ottimizzazione della cache vertex.                                                                                | [Wiki DirectXMesh](https://github.com/Microsoft/DirectXMesh/wiki)                                          |
| [DirectXMath](https://github.com/Microsoft/DirectXMath)                     | Un numero elevato di metodi e classi helper per supportare vettori, scalari, matrici, quaternioni e molte altre operazioni matematiche.                                                                                                                               | [Documentazione di DirectXMath in MSDN](/windows/desktop/dxmath/ovw-xnamath-progguide) |
| [UVAtlas](https://github.com/Microsoft/UVAtlas)                         | Usare questa operazione per creare e impacchettare un Atlante di trama isochart.                                                                                                                                                                                                           | [Wiki UVAtlas](https://github.com/Microsoft/UVAtlas/wiki)                                                  |



 

## <a name="samples"></a>Esempi

Per un elenco di esempi di D3D12 di lavoro e come individuarli ed eseguirli, vedere [esempi di lavoro](working-samples.md).

Per istruzioni dettagliate su come aggiungere codice per abilitare determinate funzionalità, vedere la [Guida dettagliata al codice D3D12](d3d12-code-walk-throughs.md).

## <a name="debug-layer"></a>Livello di debug

Il livello di debug fornisce la convalida estesa di parametri e coerenza, ad esempio la convalida del collegamento shader e dell'associazione di risorse, la convalida della coerenza dei parametri e la segnalazione delle descrizioni degli errori.

> [!Note]  
> Per Windows 10, per creare un dispositivo che supporta il livello di debug, abilitare la funzionalità facoltativa "strumenti di grafica". Passare al pannello impostazioni, in sistema, app & funzionalità, Gestisci funzionalità facoltative, aggiungere una funzionalità, quindi cercare "strumenti di grafica".

L'intestazione richiesta per supportare il livello di debug, D3D12SDKLayers. h, è inclusa per impostazione predefinita da d3d12. h.

Quando il livello di debug elenca le perdite di memoria, viene restituito un elenco di puntatori dell'interfaccia oggetto insieme ai relativi nomi descrittivi. Il nome descrittivo predefinito è " &lt; senza nome &gt; ". È possibile impostare il nome descrittivo usando il metodo [**ID3D12Object::**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) SetValue. In genere, è necessario compilare queste chiamate fuori dalla versione di produzione.

Si consiglia di usare il livello di debug per eseguire il debug delle app per assicurarsi che siano puliti da errori e avvisi. Il livello di debug consente di scrivere codice Direct3D 12. Inoltre, la produttività può aumentare quando si usa il livello di debug, in quanto è possibile visualizzare immediatamente le cause degli errori di rendering oscuri o persino le schermate nere nell'origine. Il livello di debug fornisce avvisi per molti problemi. Ad esempio:

-   Si è dimenticato di impostare una trama ma di leggerla nel pixel shader.
-   Profondità di output senza associazione di stato depth-stencil.
-   Creazione trama non riuscita con INVALIDARG.

Impostare il compilatore define D3DCOMPILE \_ debug per indicare al compilatore HLSL di includere informazioni di debug nel BLOB dello shader.

``` syntax
#define D3DCOMPILE_DEBUG 1
```

Per informazioni dettagliate su tutte le interfacce e i metodi di debug, fare riferimento a [debug layer Reference](direct3d-12-sdklayers-reference.md).

Per informazioni generali sull'uso del livello di debug, vedere informazioni [sul livello di debug di D3D12](understanding-the-d3d12-debug-layer.md).

## <a name="educational-videos"></a>Video didattici

Sono disponibili numerosi video correlati a Direct3D 12 e Windows 10 nelle [esercitazioni video su DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA), inclusi i video sugli strumenti di debug della grafica e la creazione di report sui bug grafici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 