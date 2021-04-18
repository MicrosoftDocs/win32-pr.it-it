---
title: Struttura CD3DX12_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura desc della firma radice D3D12 \_ .
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- Struttura CD3DX12_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323554"
---
# <a name="cd3dx12_root_signature_desc-structure"></a>\_ \_ Struttura desc della firma radice CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ \_ desc della firma radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ della \_ firma radice \_ DESC ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ firma radice CD3DX12 \_ \_ desc.

</dd> <dt>

**Descrizione della \_ firma radice CD3DX12 esplicita \_ \_ (const D3D12 \_ root \_ Signature \_ desc &o)**
</dt> <dd>

Crea una nuova istanza di una \_ firma radice \_ CD3DX12 \_ DESC, inizializzata con il contenuto di un'altra struttura [**\_ \_ \_ desc della firma radice di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

</dd> <dt>

**CD3DX12 \_ root \_ Signature \_ DESC (uint numParameters, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ PSTATICSAMPLERS = null, D3D12 root Signature Flags Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione della \_ firma radice CD3DX12 \_ , inizializzando i parametri seguenti:

NumParameters UINT

[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

consenso esplicito UINT numStaticSamplers = 0

consenso esplicito [**D3D12 \_ \_Campionatore statico \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

consenso esplicito [**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None

</dd> <dt>

**\_Firma radice \_ CD3DX12 \_ DESC ( \_ impostazione predefinita CD3DX12)**
</dt> <dd>

Crea una nuova istanza di una \_ firma radice \_ CD3DX12 \_ DESC, inizializzata con parametri predefiniti.

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

**inline init (UINT numParameters, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 \_ root Signature Flags \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

NumParameters UINT

[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

consenso esplicito UINT numStaticSamplers = 0

consenso esplicito [**D3D12 \_ \_Campionatore statico \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

consenso esplicito [**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None

</dd> <dt>

**static inline init (D3D12 \_ root \_ signature \_ desc &DESC, uint numParameters, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 \_ flag firma radice Flags \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ Descrizione \_ della \_ firma radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &DESC

NumParameters UINT

[**D3D12 \_ \_Parametro radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

consenso esplicito UINT numStaticSamplers = 0

consenso esplicito [**D3D12 \_ \_Campionatore statico \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

consenso esplicito [**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Descrizione della \_ firma \_ radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





