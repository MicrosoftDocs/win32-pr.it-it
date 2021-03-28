---
title: msad4
description: Confronta un valore di riferimento di 4 byte e un valore di origine a 8 byte e accumula un vettore di 4 somme. Ogni somma corrisponde alla somma mascherata delle differenze assolute di un diverso allineamento dei byte tra il valore di riferimento e il valore di origine.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- HLSL msad4
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104976967"
---
# <a name="msad4"></a>msad4

Confronta un valore di riferimento di 4 byte e un valore di origine a 8 byte e accumula un vettore di 4 somme. Ogni somma corrisponde alla somma mascherata delle differenze assolute di un diverso allineamento dei byte tra il valore di riferimento e il valore di origine.



| risultato di uint4 = msad4 (riferimento a uint, origine uint2, uint4 di accuratezza); |
|------------------------------------------------------------------|



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="reference"></span><span id="REFERENCE"></span>*riferimento*
</dt> <dd>

\[nella \] matrice di riferimento di 4 byte in un valore **uint** .

</dd> <dt>

<span id="source"></span><span id="SOURCE"></span>*origine*
</dt> <dd>

\[nella \] matrice di origine di 8 byte in due valori **uint2** .

</dd> <dt>

<span id="accum"></span><span id="ACCUM"></span>*accum*
</dt> <dd>

\[in \] un vettore di 4 valori. **msad4** aggiunge questo vettore alla somma mascherata delle differenze assolute dei diversi allineamenti di byte tra il valore di riferimento e il valore di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Vettore di 4 somme. Ogni somma corrisponde alla somma mascherata delle differenze assolute degli allineamenti di byte diversi tra il valore di riferimento e il valore di origine. **msad4** non include una differenza nella somma se tale differenza è nascosta (ovvero, il byte di riferimento è 0).

## <a name="remarks"></a>Commenti

Per usare la funzione intrinseca **msad4** nel codice dello shader, chiamare il metodo [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con le [**\_ \_ \_ Opzioni d3d11 della funzionalità d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) per verificare che il dispositivo Direct3D supporti l'opzione della funzionalità [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) . Per la funzione intrinseca **msad4** è necessario un driver di visualizzazione WDDM 1,2 e tutti i driver di visualizzazione WDDM 1,2 devono supportare **msad4**. Se l'app crea un dispositivo di rendering con [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 o 11,1 e la destinazione di compilazione è Shader Model 5 o versione successiva, il codice sorgente di HLSL può usare il **msad4** intrinseco.

I valori restituiti sono accurati solo fino a 65535. Se si chiama la funzione intrinseca **msad4** con input che potrebbero restituire valori restituiti maggiori di 65535, **msad4** genera risultati non definiti.

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                | Supportato |
|-------------------------------------------------------------|-----------|
| [Shader Model 5 o versione successiva](d3d11-graphics-reference-sm5.md) | sì       |



 

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di calcolo dei risultati per **msad4**:


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



Di seguito è riportato un esempio di come è possibile usare **msad4** per cercare un modello di riferimento all'interno di un buffer:


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>           |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

