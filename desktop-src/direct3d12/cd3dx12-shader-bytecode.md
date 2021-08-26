---
title: CD3DX12_SHADER_BYTECODE struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una struttura BYTECODE D3D12 \_ \_ SHADER.
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- CD3DX12_SHADER_BYTECODE struttura
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
ms.openlocfilehash: 5bd984268a8dcd083b2d42573c6fa0028d2b73e7a3daacecd3fefe41c68150db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988370"
---
# <a name="cd3dx12_shader_bytecode-structure"></a>Struttura CD3DX12 \_ SHADER \_ BYTECODE

Struttura helper per consentire una facile inizializzazione di [**una struttura \_ \_ BYTECODE D3D12 SHADER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

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

**BYTECODE() DELLO SHADER CD3DX12() \_ \_**
</dt> <dd>

Crea una nuova istanza non inizializzata di un BYTECODE SHADER CD3DX12. \_ \_

</dd> <dt>

**BYTECODE DELLO SHADER CD3DX12 \_ \_ esplicito(const D3D12 \_ SHADER \_ BYTECODE &o)**
</dt> <dd>

Crea una nuova istanza di un BYTECODE CD3DX12 SHADER, inizializzato con il contenuto di un'altra struttura \_ \_ [**\_ \_ BYTECODE D3D12 SHADER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> <dt>

**CD3DX12 \_ SHADER \_ BYTECODE(ID3DBlob \* pShaderBlob)**
</dt> <dd>

Crea una nuova istanza di un BYTECODE SHADER CD3DX12, \_ \_ inizializzando i parametri seguenti:

[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob

</dd> <dt>

**CD3DX12 \_ SHADER \_ BYTECODE(const void \* \_ pShaderBytecode, SIZE \_ T bytecodeLength)**
</dt> <dd>

Crea una nuova istanza di un BYTECODE SHADER CD3DX12, \_ \_ inizializzando i parametri seguenti:

void \* \_ pShaderBytecode

SIZE \_ T bytecodeLength

</dd> <dt>

**operator const D3D12 \_ SHADER \_ BYTECODE&() const**
</dt> <dd>

Definisce l'& operatore pass-by-reference per il tipo di struttura padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ SHADER \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

