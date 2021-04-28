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
ms.openlocfilehash: 7d24e19d49a8a96f91847892f519ef6c06d25ef5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114438"
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

Puntatore al dispositivo. Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome del profilo HLSL.

Se il dispositivo non supporta pixel shader, la funzione restituisce **NULL.**

## <a name="remarks"></a>Commenti

Un profilo shader specifica la versione dell'assembly shader da usare e le funzionalità disponibili per il compilatore HLSL durante la compilazione di uno shader. Nella tabella seguente sono elencati pixel shader profili supportati.



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
<td>ps_1_1</td>
<td>Eseguire la compilazione ps_1_1 versione.</td>
</tr>
<tr class="even">
<td>ps_1_2</td>
<td>Compilare per ps_1_2 versione.</td>
</tr>
<tr class="odd">
<td>ps_1_3</td>
<td>Compilare per ps_1_3 versione.</td>
</tr>
<tr class="even">
<td>ps_1_4</td>
<td>Eseguire la compilazione ps_1_4 versione.</td>
</tr>
<tr class="odd">
<td>ps_2_0</td>
<td>Eseguire la compilazione ps_2_0 versione.</td>
</tr>
<tr class="even">
<td>ps_2_a</td>
<td>Uguale al profilo ps_2_0, con le funzionalità aggiuntive seguenti disponibili per il compilatore come destinazione:
<ul>
<li>Il numero di registri temporanei (r#) è maggiore o uguale a 22.</li>
<li>Swizzle di origine arbitrario.</li>
<li>Istruzioni per la sfumatura: dsx, dsy.</li>
<li>Predicazione.</li>
<li>Nessun limite di lettura della trama dipendente.</li>
<li>Nessun limite per il numero di istruzioni di trama.</li>
</ul></td>
</tr>
<tr class="odd">
<td>ps_2_b</td>
<td>Uguale al profilo ps_2_0, con le funzionalità aggiuntive seguenti disponibili per il compilatore come destinazione:
<ul>
<li>Il numero di registri temporanei (r#) è maggiore o uguale a 32.</li>
<li>Nessun limite per il numero di istruzioni di trama.</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_3_0</td>
<td>Compilare per ps_3_0 versione.</td>
</tr>
</tbody>
</table>



 

Per altre informazioni sulle differenze tra le versioni dello shader, vedere [Differenze di pixel shader.](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
