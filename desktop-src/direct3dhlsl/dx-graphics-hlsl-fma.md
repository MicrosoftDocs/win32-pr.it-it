---
title: FMA (Corecrt \_ Math. h)
description: Restituisce l'aggiunta a due volte con doppia precisione di un oggetto \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- HLSL FMA
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
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400599"
---
# <a name="fma"></a>fma

Restituisce l'aggiunta di un oggetto \* b + c a precisione doppia.



| *ret* FMA (Double *a*, *b*, *c*); |
|----------------------------------|



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="a"></span><span id="A"></span>*un*
</dt> <dd>

\[nel \] primo valore dell'aggiunta di moltiplicazione fusa.

</dd> <dt>

<span id="b"></span><span id="B"></span>*b*
</dt> <dd>

\[nel \] secondo valore nell'addizione di moltiplicazione fusa.

</dd> <dt>

<span id="c"></span><span id="C"></span>*c*
</dt> <dd>

\[nel \] terzo valore nell'addizione di moltiplicazione fusa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'aggiunta di *un parametro a* \* *b*  +  *c* da parte della doppia precisione. Il valore restituito deve essere accurato per 0,5 unità di precisione minima (ULP rispetto).

## <a name="remarks"></a>Commenti

La funzione intrinseca **FMA** deve supportare Nans, infs e denorms.

Per usare la funzione intrinseca **FMA** nel codice dello shader, chiamare il metodo [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con le [**\_ \_ \_ Opzioni d3d11 della funzionalità d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) per verificare che il dispositivo Direct3D supporti l'opzione della funzionalità [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) . La funzione intrinseca **FMA** richiede un driver di visualizzazione WDDM 1,2 e tutti i driver di visualizzazione WDDM 1,2 devono supportare **FMA**. Se l'app crea un dispositivo di rendering con [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 o 11,1 e la destinazione di compilazione è il modello di shader 5 o versione successiva, il codice sorgente di HLSL può usare l'intrinseco **FMA** .

### <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *un*   | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**doppio**](/windows/desktop/WinProg/windows-data-types)                       | any                          |
| *b*   | uguale all'input *a*                                                                                              | [**doppio**](/windows/desktop/WinProg/windows-data-types)                       | stesse dimensioni dell'input *a* |
| *c*   | uguale all'input *a*                                                                                              | [**doppio**](/windows/desktop/WinProg/windows-data-types)                       | stesse dimensioni dell'input *a* |
| *RET* | uguale all'input *a*                                                                                              | [**doppio**](/windows/desktop/WinProg/windows-data-types)                       | stesse dimensioni dell'input *a* |



 

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                | Supportato |
|-------------------------------------------------------------|-----------|
| [Shader Model 5 o versione successiva](d3d11-graphics-reference-sm5.md) | sì       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                          |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

