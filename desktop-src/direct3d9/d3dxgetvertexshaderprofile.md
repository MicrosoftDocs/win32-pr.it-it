---
description: 'Funzione D3DXGetVertexShaderProfile: restituisce il nome del profilo HLSL (High Level Language) di alto livello supportato da un determinato dispositivo.'
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Funzione D3DXGetVertexShaderProfile (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5c646fb9779ca923480487cb96f184c76eff9ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473627"
---
# <a name="d3dxgetvertexshaderprofile-function"></a>Funzione D3DXGetVertexShaderProfile

Restituisce il nome del profilo HLSL (High-Level Shader Language) più alto supportato da un determinato dispositivo.

## <a name="syntax"></a>Sintassi


```C++
LPCSTR D3DXGetVertexShaderProfile(
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

Se il dispositivo non supporta i vertex shader, la funzione restituisce **NULL.**

## <a name="remarks"></a>Commenti

Un profilo shader specifica la versione dello shader dell'assembly da usare e le funzionalità disponibili per il compilatore HLSL durante la compilazione di uno shader. La tabella seguente elenca i profili di vertex shader supportati.




| Profilo shader | Descrizione | 
|----------------|-------------|
| vs_1_1 | Compilare per vs_1_1 versione. | 
| vs_2_0 | Eseguire la compilazione vs_2_0 versione. | 
| vs_2_a | Uguale al profilo vs_2_0, con le funzionalità aggiuntive seguenti disponibili per il compilatore come destinazione:<ul><li>Il numero di registri temporanei (r#) è maggiore o uguale a 13.</li><li>Istruzione di controllo dinamico del flusso.</li><li>Predicazione.</li></ul> | 
| vs_3_0 | Eseguire la compilazione vs_3_0 versione. | 




 

Per altre informazioni sulle differenze tra le versioni dello shader, vedere [Differenze tra vertex shader.](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
