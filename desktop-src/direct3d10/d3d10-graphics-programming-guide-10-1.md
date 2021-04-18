---
description: Funzionalità di Direct3D 10,1
ms.assetid: e60c6116-e2f9-46b7-aed8-13e3e5ae2b90
title: Funzionalità di Direct3D 10,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99935941f60a984407c688e4ae67f0a125b0130d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304804"
---
# <a name="direct3d-101-features"></a>Funzionalità di Direct3D 10,1

Direct3D 10,1 estende il set di funzionalità di Direct3D 10,0 con le seguenti nuove funzionalità:

-   Modalità di Blend: modalità di Blend indipendenti per ogni destinazione di rendering usando la nuova interfaccia di stato di Blend (vedere [**interfaccia ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)). Le operazioni di fusione di origine doppie sono limitate allo slot di destinazione di rendering 0; non è possibile scrivere in altri output o avere destinazioni di rendering vincolate a slot diversi dallo slot 0.
-   Comportamento di eliminazione: i visi con zero aree vengono automaticamente abbattuti; Questa operazione influisca solo sul rendering wireframe.
-   Regole a virgola mobile: usa le stesse regole IEEE-754 per le operazioni a virgola mobile a virgola mobile, ad eccezione del fatto che le operazioni a virgola mobile a 32 bit sono state ristrette per produrre un risultato entro 0,5 unità-ultimo posto (0,5 ULP rispetto) del risultato preciso. Questo vale per l'addizione, la sottrazione e la moltiplicazione. (accuratezza a 0,5 ULP rispetto per Multiply, 1,0 ULP rispetto per reciproca).
-   Formati: la precisione della fusione float16 è aumentata fino a 0,5 ULP rispetto. La fusione è necessaria anche per i formati UNORM16/SNORM16/SNORM8.
-   Anti-aliasing di multicampionamento: il campionamento multiplo è stato migliorato per generalizzare la trasparenza basata sul code coverage e rendere più efficiente il multicampionamento con il rendering a più passaggi. A tale scopo, la semantica multisample viene definita come se il pixel shader venga eseguito sempre una volta per campione (frequenza di campionamento), calcolando un colore separato per campione. Se in un pixel shader non vengono utilizzati attributi per campione, verrà calcolato lo stesso valore per ogni campione coperto in un pixel. In tal caso, è equivalente all'hardware che esegue lo shader una volta per pixel (frequenza pixel), replicando il risultato in tutti gli esempi analizzati. Naturalmente, l'esecuzione a pixel-Frequency produce sempre gli stessi risultati dell'esecuzione dello stesso shader alla frequenza di campionamento, quando gli attributi vengono campionati con frequenza in pixel. Il numero di statistiche della pipeline PSInvocations viene incrementato alla frequenza di campionamento, a meno che lo shader non sia in esecuzione a frequenza di pixel.
-   Larghezza di banda della fase della pipeline: aumento della quantità di dati che è possibile passare tra le fasi dello shader: 

    | Risorsa                        | Limiti                    |
    |---------------------------------|---------------------------|
    | Registri tra fasi dello shader | 32 (32-bit x 4-componente) |
    | Registri di input vertex shader   | 32                        |
    | Slot input assembler input     | 32                        |

    

     

-   Regole di rasterizzazione: le regole per la rasterizzazione sono state modificate per le linee, inoltre sono state aggiunte nuove funzionalità.
    -   MultisampleEnable interessa solo la rasterizzazione delle righe (punti e triangoli non sono interessati) e viene usato per scegliere un algoritmo di disegno di linea. Ciò significa che la rasterizzazione di più campioni da Direct3D 10 non è più supportata.
    -   Nuova esecuzione del pixel shader di frequenza di esempio con la rasterizzazione primitiva.
-   Risorse-CopyResource è abilitato in due nuovi scenari:
    -   È ora possibile usare sia il colore che la profondità/stencil MSAA Surfaces con CopyResource come origine o destinazione
    -   Conversione del formato durante la copia tra alcune risorse prestrutturate a 32/64/128 bit, le risorse tipizzate e le rappresentazioni compresse con le stesse larghezze di bit.
-   Campionamento di trama: \_ le istruzioni c di esempio c e \_ \_ LZ c di esempio sono definite per funzionare sia con Texture2DArrays che con TextureCubeArrays, usare il membro location (il componente alfa) per specificare un indice di matrice.
-   Views: TextureCube e il nuovo TextureCubeArray (vedere [**D3D10 \_ TEXCUBE \_ array \_ srv1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)) non sono risorse effettive, ma sono nuove viste in una risorsa Texture2DArray. Creare una visualizzazione risorse da una risorsa Texture2DArray con un nuovo flag di utilizzo ( \_ risorsa D3D10 \_ varie \_ TEXTURECUBE), usare la nuova interfaccia dell' [**interfaccia ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) per associare una visualizzazione di trama al cubo alla pipeline.

Le nuove funzionalità richiedono un tipo di dispositivo 10,1 (vedere [**interfaccia ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)) che può essere creato chiamando [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1)oppure è possibile creare il dispositivo e la catena di scambio contemporaneamente chiamando [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1).

In Windows Vista Service Pack 1, le dll Direct3D 10,0 e Direct3D 10,1 esistono side-by-side nel sistema. Per accedere alle funzionalità di 10,1, effettuare una delle operazioni seguenti:

## <a name="accessing-101-features-on-vista-gold-and-vista-service-pack-1"></a>Accesso alle funzionalità di 10,1 in vista di Gold e Vista Service Pack 1

Gli sviluppatori che desiderano supportare Vista Gold e SP1 dovranno tenere conto della mancanza delle nuove estensioni API 10,1 in vista Gold. Sia DXUT che D3DX10 forniranno funzioni utili per creare il dispositivo appropriato, in base alle DLL disponibili nel sistema e all'hardware disponibile (10,0 o 10,1). Il dispositivo 10,1 eredita dal dispositivo 10,0 e può essere recuperato usando QueryInterface (). È consigliabile che ogni applicazione tenga traccia del tipo di dispositivo e mantenga un puntatore al dispositivo 10,1 (se disponibile) per evitare frequenti chiamate QueryInterface quando si desidera la funzionalità 10,1. Analogamente, in cui 10,1 visualizzazioni di risorse e oggetti di stato sono associati dalla classe personalizzata di un'applicazione, è consigliabile che l'applicazione ritenga che l'oggetto sia un tipo 10,0 o 10,1 per evitare chiamate di QueryInterface () ridondanti. D3DX10 include un set di funzioni di utilità per semplificare questo processo (vedere [**D3DX10CreateDevice**](d3dx10createdevice.md) e [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md)).

## <a name="accessing-101-features-on-vista-service-pack-1-exclusively"></a>Accesso esclusivo alle funzionalità di 10,1 in Vista Service Pack 1

Alcuni sviluppatori possono scegliere di richiedere il Service Pack 1 di vista, che verrà distribuito in modo estensivo agli utenti finali e include una serie di miglioramenti al di fuori di Direct3D 10,1. Questi sviluppatori possono usare esclusivamente le intestazioni e le librerie Direct3D 10,1, assumendo una dipendenza dalle DLL Direct3D 10,1 che supportano sia l'hardware 10,0 che 10,1 (alcune chiamate potrebbero non riuscire, tuttavia, nei dispositivi 10,0 in cui la nuova funzionalità non è supportata).

Note aggiuntive:

-   Le API esposte nella D3DX10.dll accetteranno entrambi i dispositivi 10,0 e 10,1 e utilizzeranno la funzionalità 10,1, se disponibile.
-   D3D10SDKLayers.dll supporta un dispositivo 10,1 ed è in grado di restituire le funzionalità di debug di vomito appropriate per 10,1.
-   D3D10Ref.dll implementa un dispositivo software 10,0 e 10,1.
-   D3DX10 e FXC supportano il modello di shader 10,1 aggiornato con le seguenti destinazioni: vs \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1 e FX \_ 4 \_ 1 che può essere associato a un dispositivo 10,1. Un dispositivo 10,1 supporta Shader Model 4,0 e 4,1 shader.
-   Il Framework degli effetti Direct3D 10,0 supporta i dispositivi 10,0 e 10,1. Tuttavia, qualsiasi tecnica che includa Shader Model 4,1 shaders o le nuove funzionalità di 10,1 deve usare un dispositivo 10,1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



