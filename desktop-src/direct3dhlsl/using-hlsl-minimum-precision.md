---
title: Uso della precisione minima HLSL
description: A partire Windows 8, i driver di grafica possono implementare tipi di dati scalari HLSL a precisione minima usando qualsiasi precisione maggiore o uguale alla precisione in bit specificata.
ms.assetid: 422B0C45-5CEB-4235-AD05-62D36C36CFC6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4981cd80fdd80fbccf1b2610cbfeb210a9894a857fb2d7af1ddd84b9e2772e70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067281"
---
# <a name="using-hlsl-minimum-precision"></a>Uso della precisione minima HLSL

A partire Windows 8, i driver di grafica possono implementare tipi di dati [scalari HLSL](dx-graphics-hlsl-scalar.md) a precisione minima usando qualsiasi precisione maggiore o uguale alla precisione in bit specificata. Quando il codice HLSL dello shader con precisione minima viene usato su hardware che implementa la precisione minima HLSL, si usa meno larghezza di banda di memoria e di conseguenza si usa anche meno potenza di sistema.

È possibile eseguire una query per ottenere il supporto della precisione minima fornito dal driver di grafica chiamando [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con il valore [**D3D11 \_ FEATURE SHADER MIN PRECISION \_ \_ \_ \_ SUPPORT.**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) Per altre informazioni, vedere [Supporto della precisione minima HLSL.](/windows/desktop/direct3d11/direct3d-11-1-features)

-   [Dichiarare variabili con tipi di dati con precisione minima](#declare-variables-with-minimum-precision-data-types)
-   [Test del codice shader con precisione minima](#testing-your-minimum-precision-shader-code)
-   [Argomenti correlati](#related-topics)

## <a name="declare-variables-with-minimum-precision-data-types"></a>Dichiarare variabili con tipi di dati con precisione minima

Per usare la precisione minima nel codice dello shader HLSL, dichiarare singole variabili con tipi come **min16float** (**min16float4** per un vettore), **min16int**, **min10float** e così via. Con queste variabili, il codice dello shader indica che non richiede una precisione maggiore rispetto a quanto indicato nelle variabili. Tuttavia, l'hardware può ignorare gli indicatori di precisione minima ed essere eseguito con una precisione a 32 bit completa. Quando il codice dello shader viene usato su hardware che sfrutta la precisione minima, si usa meno larghezza di banda di memoria e di conseguenza si usa anche meno potenza di sistema, purché il codice dello shader non si aspetti una precisione maggiore di quella specificata.

Non è necessario creare più shader che usano e non usano la precisione minima. Creare invece shader con precisione minima e le variabili di precisione minima si comportano con una precisione a 32 bit completa se il driver di grafica segnala che non supporta alcuna precisione minima. Gli shader con precisione minima HLSL non funzionano nei sistemi operativi precedenti a Windows 8, quindi se si prevede di usare come destinazione sistemi operativi precedenti, sarà necessario creare più shader, alcuni che lo fanno e altri che non usano la precisione minima.

> [!Note]  
> Non eseguire il commutamento dei dati tra livelli di precisione diversi all'interno di uno shader perché questi tipi di conversioni sono disarticiati e riducono le prestazioni. L'eccezione è che le costanti shader sono sempre a 32 bit, ma i fornitori possono progettare hardware grafico in grado di eseguire liberamente la conversione a qualsiasi precisione inferiore potrebbe essere utilizzata dalla lettura delle istruzioni HLSL.

 

Usando la precisione minima, è possibile controllare la precisione dei calcoli in varie parti del codice dello shader.

Le regole per la precisione minima HLSL sono simili a quelle di C/C++, in cui i tipi in un'espressione determinano la precisione dell'operazione, non il tipo in cui viene eseguita la scrittura.

## <a name="testing-your-minimum-precision-shader-code"></a>Test del codice shader con precisione minima

L'rasterizzazione dei riferimenti [**(D3D \_ DRIVER \_ TYPE \_ REFERENCE)**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)offre un'idea approssimativa del comportamento della precisione minima nel codice dello shader HLSL quantificando ogni istruzione HLSL alla precisione specificata. In questo modo è possibile individuare codice che potrebbe basarsi accidentalmente su una precisione superiore alla precisione minima. L'rasterizzazione dei riferimenti non viene eseguita più velocemente quando il codice dello shader HLSL usa la precisione minima, ma è possibile usarlo per verificare la correttezza del codice. [WARP](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) [**(D3D \_ DRIVER \_ TYPE \_ WARP)**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)non supporta l'uso della precisione minima nel codice dello shader HLSL. WARP viene eseguito solo con una precisione a 32 bit completa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 