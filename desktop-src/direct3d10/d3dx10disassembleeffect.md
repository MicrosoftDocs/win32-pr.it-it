---
description: Nota invece di usare questa funzione legacy, è consigliabile usare l'API D3DDisassemble. Questa funzione, che disassembla un effetto compilato in una stringa di testo che contiene istruzioni di assembly e assegnazioni di registro, è stata deprecata.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: Funzione D3DX10DisassembleEffect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 67fe19365616e779bd17ab689550b34737288317
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969426"
---
# <a name="d3dx10disassembleeffect-function"></a>D3DX10DisassembleEffect (funzione)

> [!Note]  
> Invece di usare questa funzione legacy, è consigliabile usare l'API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .

 

Questa funzione, che disassembla un effetto compilato in una stringa di testo che contiene istruzioni di assembly e assegnazioni di registro, è stata deprecata. Usare invece [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pEffect* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***

Un puntatore all'interfaccia effetto (vedere [**interfaccia ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).

</dd> <dt>

*EnableColorCode* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Includere i tag HTML nell'output per codificare il risultato.

</dd> <dt>

*ppDisassembly* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Indirizzo di un buffer (vedere [**interfaccia ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene l'effetto disassemblato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
