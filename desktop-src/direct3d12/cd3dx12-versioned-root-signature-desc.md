---
title: Struttura CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura desc della firma radice con versione D3D12 \_ \_ .
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- Struttura CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322184"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a>\_ \_ \_ Struttura desc della firma radice con versione CD3DX12 \_

Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ desc della \_ firma \_ radice con versione D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

## <a name="syntax"></a>Sintassi


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 della \_ \_ firma radice con versione \_ \_ DESC ()**
</dt> <dd>

Crea una nuova istanza non inizializzata di una \_ Descrizione della firma radice con versione CD3DX12 \_ \_ \_ .

</dd> <dt>

**firma radice con versione CD3DX12 esplicita \_ \_ \_ \_ DESC (const D3D12 \_ versione \_ radice \_ \_ desc &o)**
</dt> <dd>

Crea una nuova istanza di una \_ \_ firma radice CD3DX12 con \_ versione \_ DESC, inizializzata con il contenuto di una struttura della [**\_ \_ \_ firma radice \_ con versione D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

</dd> <dt>

**firma radice con versione CD3DX12 esplicita \_ \_ \_ \_ DESC (const D3D12 \_ root \_ Signature \_ desc &o)**
</dt> <dd>

Crea una nuova istanza di una \_ \_ firma radice CD3DX12 con \_ versione \_ DESC, inizializzata con il contenuto di una struttura [**D3D12 della \_ \_ firma \_ radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

</dd> <dt>

**firma radice con versione CD3DX12 esplicita \_ \_ \_ \_ DESC (const D3D12 \_ root \_ Signature \_ DESC1 &o)**
</dt> <dd>

Crea una nuova istanza di una \_ \_ firma radice CD3DX12 con \_ versione \_ DESC, inizializzata con il contenuto di una struttura [**\_ \_ \_ DESC1 della firma radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) .

</dd> <dt>

**CD3DX12 della \_ \_ firma radice con versione \_ \_ DESC (uint NUMPARAMETERS, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 firma radice flag Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione della firma radice con versione CD3DX12 \_ \_ \_ , inizializzando i parametri seguenti:

NumParameters UINT

[**\_ \_ parametro radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) const \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None

</dd> <dt>

**CD3DX12 della \_ \_ firma radice con versione \_ \_ DESC (uint NUMPARAMETERS, const D3D12 \_ root \_ parametro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 firma radice flag Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**
</dt> <dd>

Crea una nuova istanza di una \_ Descrizione della firma radice con versione CD3DX12 \_ \_ \_ , inizializzando i parametri seguenti:

NumParameters UINT

const [**D3D12 \_ radice \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None

</dd> <dt>

**\_Firma radice con versione CD3DX12 \_ \_ \_ DESC ( \_ impostazione predefinita CD3DX12)**
</dt> <dd>

Crea una nuova istanza di una \_ \_ firma radice CD3DX12 con \_ versione \_ DESC, inizializzata con i parametri predefiniti:

UINT numParameters = 0

const [**D3D12 \_ root \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = null

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None

</dd> <dt>

**inline init \_ 1 \_ 0 (uint numParameters, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint NUMSTATICSAMPLERS = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 root Signature Flags Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

NumParameters UINT

[**\_ \_ parametro radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) const \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None

</dd> <dt>

**static inline init \_ 1 \_ 0 (D3D12 con \_ versione \_ radice \_ \_ desc &DESC, uint numParameters, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 root Signature flag Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ Descrizione della \_ firma radice con versione \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC

NumParameters UINT

[**\_ \_ parametro radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) const \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None

</dd> <dt>

**inline init \_ 1 \_ 1 (uint numParameters, const D3D12 \_ root \_ parametro1 \* \_ pParameters, uint NUMSTATICSAMPLERS = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ PSTATICSAMPLERS = null, D3D12 firma radice flag Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

NumParameters UINT

const [**D3D12 \_ radice \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None

</dd> <dt>

**static inline init \_ 1 \_ 1 (D3D12 della \_ \_ firma radice con versione \_ \_ desc &DESC, uint numParameters, const D3D12 \_ root \_ parametro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 \_ flag di firma radice Flags \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**
</dt> <dd>

Specifica una funzione che Inizializza i parametri seguenti:

[**D3D12 \_ Descrizione della \_ firma radice con versione \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC

NumParameters UINT

const [**D3D12 \_ radice \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ Descrizione della firma radice \_ con versione D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





