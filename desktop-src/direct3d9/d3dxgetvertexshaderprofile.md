---
description: Restituisce il nome del profilo HLSL (High-Level Shader Language) più alto supportato da un determinato dispositivo.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Funzione D3DXGetVertexShaderProfile (D3DX9Shader. h)
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
ms.openlocfilehash: 34f7ccaeba60bdd1d7c512cee3fb4da29289408a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322653"
---
# <a name="d3dxgetvertexshaderprofile-function"></a>D3DXGetVertexShaderProfile (funzione)

Restituisce il nome del profilo HLSL (High-Level Shader Language) più alto supportato da un determinato dispositivo.

## <a name="syntax"></a>Sintassi


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore al dispositivo. Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome del profilo HLSL.

Se il dispositivo non supporta vertex shader, la funzione restituisce **null**.

## <a name="remarks"></a>Commenti

Un profilo shader specifica la versione dell'assembly shader da usare e le funzionalità disponibili per il compilatore HLSL durante la compilazione di uno shader. La tabella seguente elenca i profili vertex shader supportati.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Profilo shader</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vs_1_1</td>
<td>Compilare per vs_1_1 versione.</td>
</tr>
<tr class="even">
<td>vs_2_0</td>
<td>Compilare per vs_2_0 versione.</td>
</tr>
<tr class="odd">
<td>vs_2_a</td>
<td>Uguale al profilo vs_2_0, con le seguenti funzionalità aggiuntive disponibili per il compilatore come destinazione:
<ul>
<li>Il numero di registri temporanei (r #) è maggiore o uguale a 13.</li>
<li>Istruzione di controllo dinamico del flusso.</li>
<li>Predicazione.</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_3_0</td>
<td>Compilare per vs_3_0 versione.</td>
</tr>
</tbody>
</table>



 

Per altre informazioni sulle differenze tra le versioni dello shader, vedere [differenze di vertex shader](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
