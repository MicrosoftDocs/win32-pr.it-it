---
title: fma (Corecrt \_ math.h)
description: Restituisce l'addizione di moltiplicazione fusa a precisione doppia di \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- fma HLSL
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b9a6932a1b0f0f8f1f7bc674920162def49e556c8d5b757547d4837caa60b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120205"
---
# <a name="fma"></a>fma

Restituisce la moltiplicazione a precisione doppia di b \* + c.



| *ret* fma(double *a*, *b*, *c*); |
|----------------------------------|



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="a"></span><span id="A"></span>*Un*
</dt> <dd>

\[in \] Il primo valore nell'addizione di moltiplicazione fusa.

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[in \] Il secondo valore nell'addizione di moltiplicazione fusa.

</dd> <dt>

<span id="c"></span><span id="C"></span>*C*
</dt> <dd>

\[in \] Il terzo valore nell'addizione moltiplicata fusa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Moltiplicazione a precisione doppia dei parametri *a* \* *b*  +  *c*. Il valore restituito deve essere accurato a 0,5 unità di precisione minima (ULP).

## <a name="remarks"></a>Commenti

La **funzione intrinseca fma** deve supportare NaN, INFs e Denorms.

Per usare la funzione intrinseca **fma** nel codice shader, chiamare il metodo [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) per verificare che il dispositivo Direct3D supporti l'opzione della funzionalità [**ExtendedDoublesShaderInstructions.**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) La **funzione intrinseca fma** richiede un driver video WDDM 1.2 e tutti i driver di visualizzazione WDDM 1.2 devono supportare **fma**. Se l'app crea [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) un dispositivo di rendering con livello di funzionalità 11.0 o 11.1 e la destinazione di compilazione è il modello shader 5 o versione successiva, il codice sorgente HLSL può usare la **funzione intrinseca fma.**

### <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *Un*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Doppia**](/windows/desktop/WinProg/windows-data-types)                       | any                          |
| *b*   | uguale all'input *a*                                                                                              | [**Doppia**](/windows/desktop/WinProg/windows-data-types)                       | stesse dimensioni *dell'input* |
| *c*   | uguale all'input *a*                                                                                              | [**Doppia**](/windows/desktop/WinProg/windows-data-types)                       | stesse dimensioni *dell'input* |
| *Ret* | uguale all'input *a*                                                                                              | [**Doppia**](/windows/desktop/WinProg/windows-data-types)                       | stesse dimensioni *dell'input* |



 

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                | Supportato |
|-------------------------------------------------------------|-----------|
| [Modello shader 5 o versione successiva](d3d11-graphics-reference-sm5.md) | sì       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

