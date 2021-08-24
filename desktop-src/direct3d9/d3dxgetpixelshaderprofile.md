---
description: 'Funzione D3DXGetPixelShaderProfile: restituisce il nome del profilo HLSL (High Level Shader Language) più alto supportato da un determinato dispositivo.'
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: Funzione D3DXGetPixelShaderProfile (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc609e742a4f780f3cb8c34e4dbc4cc40842ee51
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473657"
---
# <a name="d3dxgetpixelshaderprofile-function"></a>Funzione D3DXGetPixelShaderProfile

Restituisce il nome del profilo HLSL (High-Level Shader Language) più alto supportato da un determinato dispositivo.

## <a name="syntax"></a>Sintassi


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore al dispositivo. Vedere [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome del profilo HLSL.

Se il dispositivo non supporta pixel shader, la funzione restituisce **NULL.**

## <a name="remarks"></a>Commenti

Un profilo shader specifica la versione dell'assembly shader da usare e le funzionalità disponibili per il compilatore HLSL durante la compilazione di uno shader. Nella tabella seguente sono elencati pixel shader profili supportati.




| Profilo shader | Descrizione | 
|----------------|-------------|
| ps_1_1 | Compilare per ps_1_1 versione. | 
| ps_1_2 | Compilare per ps_1_2 versione. | 
| ps_1_3 | Compilare per ps_1_3 versione. | 
| ps_1_4 | Compilare per ps_1_4 versione. | 
| ps_2_0 | Compilare per ps_2_0 versione. | 
| ps_2_a | Uguale al profilo ps_2_0, con le funzionalità aggiuntive seguenti disponibili per il compilatore come destinazione:<ul><li>Il numero di registri temporanei (r#) è maggiore o uguale a 22.</li><li>Scorrimento arbitrario dell'origine.</li><li>Istruzioni sfumatura: dsx, dsy.</li><li>Predicazione.</li><li>Nessun limite di lettura trame dipendente.</li><li>Nessun limite per il numero di istruzioni di trama.</li></ul> | 
| ps_2_b | Uguale al profilo ps_2_0, con le funzionalità aggiuntive seguenti disponibili per il compilatore come destinazione:<ul><li>Il numero di registri temporanei (r#) è maggiore o uguale a 32.</li><li>Nessun limite per il numero di istruzioni di trama.</li></ul> | 
| ps_3_0 | Compilare per ps_3_0 versione. | 




 

Per altre informazioni sulle differenze tra le versioni dello shader, vedere [Differenze dei pixel shader.](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
