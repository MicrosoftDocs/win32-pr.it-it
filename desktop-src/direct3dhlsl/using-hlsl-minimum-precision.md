---
title: Uso della precisione minima HLSL
description: A partire da Windows 8, i driver grafici possono implementare i tipi di dati scalari HLSL precisione minima usando una precisione maggiore o uguale alla precisione dei bit specificata.
ms.assetid: 422B0C45-5CEB-4235-AD05-62D36C36CFC6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7f66f35aef3e870edb4e8564a280be89ce34be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728167"
---
# <a name="using-hlsl-minimum-precision"></a>Uso della precisione minima HLSL

A partire da Windows 8, i driver grafici possono implementare i [tipi di dati scalari HLSL](dx-graphics-hlsl-scalar.md) precisione minima usando una precisione maggiore o uguale alla precisione dei bit specificata. Quando il codice shader con precisione minima di HLSL viene usato nell'hardware che implementa la precisione minima di HLSL, si usa una minore larghezza di banda di memoria e, di conseguenza, si usa meno energia del sistema.

È possibile eseguire una query per il supporto di precisione minima fornito dal driver di grafica chiamando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con il valore di supporto della precisione minima dello [**\_ shader della funzionalità \_ \_ \_ \_ d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) . Per altre informazioni, vedere [supporto della precisione minima di HLSL](/windows/desktop/direct3d11/direct3d-11-1-features).

-   [Dichiarare le variabili con tipi di dati con precisione minima](#declare-variables-with-minimum-precision-data-types)
-   [Test del codice shader con precisione minima](#testing-your-minimum-precision-shader-code)
-   [Argomenti correlati](#related-topics)

## <a name="declare-variables-with-minimum-precision-data-types"></a>Dichiarare le variabili con tipi di dati con precisione minima

Per usare la precisione minima nel codice dello shader HLSL, dichiarare le singole variabili con tipi come **min16float** (**min16float4** per un vettore), **min16int**, **min10float** e così via. Con queste variabili, il codice dello shader indica che non richiede una maggiore precisione rispetto a quanto indicato dalle variabili. Tuttavia, l'hardware può ignorare gli indicatori di precisione minimi ed eseguire a una precisione completa a 32 bit. Quando il codice dello shader viene usato nell'hardware che sfrutta la precisione minima, si usa una minore larghezza di banda di memoria e, di conseguenza, si usa meno energia del sistema purché il codice dello shader non preveda una maggiore precisione rispetto a quanto specificato.

Non è necessario creare più shader che non usano la precisione minima. Al contrario, creare shader con precisione minima e le variabili di precisione minime si comportano con una precisione a 32 bit completa se il driver di grafica segnala che non supporta alcuna precisione minima. Gli shader con precisione minima di HLSL non funzionano con i sistemi operativi precedenti a Windows 8, pertanto se si prevede di usare sistemi operativi precedenti, è necessario creare più shader, ad altre operazioni che non usano la precisione minima.

> [!Note]  
> Non eseguire commutazioni di dati tra diversi livelli di precisione all'interno di uno shader, perché questi tipi di conversione sono inutili e riducono le prestazioni. L'eccezione è che le costanti dello shader sono sempre di 32 bit, ma i fornitori possono progettare hardware grafico che può essere convertito liberamente in una precisione inferiore che la lettura dell'istruzione HLSL potrebbe usare.

 

Con la precisione minima è possibile controllare la precisione dei calcoli in varie parti del codice dello shader.

Le regole per la precisione minima HLSL sono simili a C/C++, in cui i tipi in un'espressione determinano la precisione dell'operazione, non il tipo in cui viene eseguita la scrittura.

## <a name="testing-your-minimum-precision-shader-code"></a>Test del codice shader con precisione minima

L'unità di rasterizzazione dei riferimenti ([**\_ riferimento al \_ tipo \_ di driver D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) offre un'idea approssimativa del modo in cui la precisione minima nel codice dello shader HLSL si comporta quantizzando ciascuna istruzione HLSL alla precisione specificata. In questo modo è possibile individuare il codice che potrebbe inavvertitamente basarsi su un valore superiore alla precisione minima. L'rasterizzazione dei riferimenti non viene eseguita più velocemente quando il codice dello shader HLSL usa la precisione minima, ma è possibile usarlo per verificare la correttezza del codice. [Warp](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) ([**\_ tipo di driver D3D \_ \_ Warp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) non supporta l'utilizzo della precisione minima nel codice dello shader HLSL. WARP viene eseguito solo a una precisione a 32 bit completa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 