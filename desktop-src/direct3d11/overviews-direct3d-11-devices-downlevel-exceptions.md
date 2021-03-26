---
title: Eccezioni
description: Questo argomento descrive le eccezioni quando si usa Direct3D 11 su hardware di livello inferiore.
ms.assetid: b3f85036-8572-40ee-b522-3b677443b840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97920ae42347cf618b22df82abc3b6e06bd5200d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338991"
---
# <a name="exceptions"></a>Eccezioni

Alcune funzionalità di Direct3D 11 non sono completamente specificate dai livelli di funzionalità. Questo argomento descrive le eccezioni quando si usa Direct3D 11 su hardware di livello inferiore. Probabilmente è stata aggiunta una funzionalità dopo che il livello di funzionalità è stato definito (e richiede un driver aggiornato) o se le GPU diverse implementano implementazioni molto diverse. Le eccezioni a livello di funzionalità possono essere raccolte nei gruppi seguenti:

-   [Formati estesi](#extended-formats)
-   [Anti-aliasing di multicampionamento](#multisample-anti-aliasing)
-   [Dimensioni Texture2D](#texture2d-sizes)
-   [Comportamento speciale degli adapter per il livello di funzionalità 9](#special-behavior-of-adapters-for-feature-level-9)
-   [Argomenti correlati](#related-topics)

Nella sezione di [riferimento 10Level9](d3d11-graphics-reference-10level9.md) sono elencate le differenze tra il comportamento di diversi metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a diversi livelli di funzionalità di 10Level9.

## <a name="extended-formats"></a>Formati estesi

Un formato esteso è un formato pixel aggiunto a Direct3D 10,1 e Direct3D 11 per i livelli di funzionalità 10 \_ 0 e 10 \_ 1. Un formato esteso richiede un driver aggiornato (per Direct3D 10 \_ 1 o versione successiva). Usare [**ID3D11Device:: CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) e [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) per eseguire una query per il supporto di questi formati estesi.

Formato esteso:

-   Aggiunge il supporto per l'ordine BGRA delle risorse per componente a 8 bit.
-   Consente il cast di un buffer a catena di scambio valore intero. Questo consente a un'applicazione di aggiungere o rimuovere il \_ suffisso sRGB o eseguire il rendering in una \_ catena di scambio di distorsione XR.
-   Aggiunge il supporto facoltativo per il \_ formato DXGI \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM.
-   Garantisce che un \_ formato DXGI \_ R16G16B16A16 \_ float swap chain venga presentato come se i dati contenuti non sono codificati con sRGB.

Il set completo di formati estesi è completamente supportato o non supportato, ad eccezione del \_ formato di distorsione XR. Il \_ formato di distorsione XR è:

-   Non supportato in qualsiasi livello 9
-   Facoltativo nel \_ livello 10 0 o 10 \_ 1
-   Garantita a livello 11 \_ 0

## <a name="multisample-anti-aliasing"></a>Anti-aliasing di multicampionamento

Le implementazioni di MSAA hanno poco in comune tra implementazioni GPU. Il livello di funzionalità 10,1 ha aggiunto un valore minimo ben definito, ma a livelli di funzionalità inferiori, MSAA deve essere testato in modo esplicito usando [**ID3D11Device:: CheckMultisampleQualityLevels**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkmultisamplequalitylevels).

## <a name="texture2d-sizes"></a>Dimensioni Texture2D

Un livello di funzionalità garantisce che sia possibile creare una dimensione minima. Tuttavia, un'applicazione può creare trame più grandi fino alle dimensioni massime supportate dalla GPU. Un'applicazione deve prevedere un errore da un metodo, ad esempio [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) , se viene superato il valore massimo.

## <a name="special-behavior-of-adapters-for-feature-level-9"></a>Comportamento speciale degli adapter per il livello di funzionalità 9

I tre livelli di funzionalità più bassi sono i livelli di funzionalità D3D \_ \_ \_ 9 \_ 1, il \_ livello di funzionalità D3D \_ \_ 9 \_ 2 e il \_ \_ livello di funzionalità D3D \_ 9 \_ 3, condividono una DLL di implementazione comune e considerano l'argomento [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) per D3D11CreateDevice \[ AndSwapchain \] come adattatore modello e creano la propria scheda come parte della creazione del dispositivo. Ciò significa che il **IDXGIAdapter** passato nella routine di creazione non sarà uguale a quello recuperato dal dispositivo tramite IDXGIDevice:: GetAdapter. L'effetto di questa operazione è che i **IDXGIOutputs** enumerati dall'adapter passato non possono essere usati per accedere a schermo intero usando un dispositivo di livello 9, poiché tali output non sono di proprietà dell'adattatore del dispositivo. È consigliabile rimuovere l'adattatore del modello passato e recuperare l'adattatore creato dal dispositivo usando IDXGIDevice:: GetAdapter, dove [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) può essere recuperato usando QueryInterface dall'interfaccia del dispositivo Direct3D.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direct3D 11 su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 