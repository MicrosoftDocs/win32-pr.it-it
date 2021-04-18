---
title: Struttura CD3DX12_SHADER_BYTECODE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura BYTECODE dello shader D3D12 \_ .
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- Struttura CD3DX12_SHADER_BYTECODE
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322203"
---
# <a name="cd3dx12_shader_bytecode-structure"></a>\_ \_ Struttura BYTECODE shader CD3DX12

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ BYTECODE dello shader D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**\_BYTECODE shader CD3DX12 \_ ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un \_ BYTECODE dello shader CD3DX12 \_ .

</dd> <dt>

**bytecode CD3DX12 \_ shader esplicito \_ (const D3D12 \_ shader \_ bytecode &o)**
</dt> <dd>

Crea una nuova istanza di un \_ bytecode dello shader CD3DX12 \_ , inizializzato con il contenuto di un'altra struttura [**\_ \_ bytecode dello shader D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**\_BYTECODE shader CD3DX12 \_ (ID3DBlob \* pShaderBlob)**
</dt> <dd>

Crea una nuova istanza di un \_ BYTECODE dello shader CD3DX12 \_ , inizializzando i parametri seguenti:

[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob

</dd> <dt>

**\_BYTECODE shader CD3DX12 \_ (const void \* \_ PShaderBytecode, Size \_ T bytecodeLength)**
</dt> <dd>

Crea una nuova istanza di un \_ BYTECODE dello shader CD3DX12 \_ , inizializzando i parametri seguenti:

void \* \_ pShaderBytecode

DIMENSIONI \_ T bytecodeLength

</dd> <dt>

**operator const D3D12 \_ BYTECODE dello shader \_& () const**
</dt> <dd>

Definisce il & operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_BYTECODE shader D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

