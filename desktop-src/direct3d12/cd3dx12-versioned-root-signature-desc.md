---
title: CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC (D3dx12.h)
description: Struttura helper per consentire un'inizializzazione semplice di una struttura DESC D3D12 \_ \_ VERSIONED ROOT \_ \_ SIGNATURE.
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC struttura
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
ms.openlocfilehash: 4b35c546dcfe5ed7c181dae3a9ae8baaa70aa05369ccb15e4cbd123ae92d75b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118808531"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a>Struttura \_ \_ \_ \_ DESC DELLA FIRMA RADICE CON CONTROLLO DELLE VERSIONI DI CD3DX12

Struttura helper per consentire un'inizializzazione semplice di [**una struttura DESC D3D12 \_ \_ VERSIONED ROOT \_ SIGNATURE. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)

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

**CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC()**
</dt> <dd>

Crea una nuova istanza non inizializzata di un file CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC.

</dd> <dt>

**explicit CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC(const D3D12 \_ VERSIONED ROOT SIGNATURE \_ \_ \_ DESC &o)**
</dt> <dd>

Crea una nuova istanza di cd3DX12 VERSIONED ROOT SIGNATURE DESC, inizializzata con il contenuto di una \_ \_ struttura \_ \_ [**D3D12 \_ VERSIONED ROOT SIGNATURE \_ \_ \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)

</dd> <dt>

**explicit CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC(const D3D12 \_ ROOT SIGNATURE \_ \_ DESC &o)**
</dt> <dd>

Crea una nuova istanza di una struttura DESC CD3DX12 VERSIONED ROOT SIGNATURE, inizializzata con il contenuto di una \_ \_ struttura \_ \_ [**D3D12 \_ ROOT SIGNATURE \_ \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)

</dd> <dt>

**explicit CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC(const D3D12 \_ ROOT SIGNATURE \_ \_ DESC1 &o)**
</dt> <dd>

Crea una nuova istanza di una struttura CD3DX12 VERSIONED ROOT SIGNATURE DESC, inizializzata con il contenuto di una \_ \_ struttura \_ \_ [**D3D12 \_ ROOT SIGNATURE \_ \_ DESC1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)

</dd> <dt>

**CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nuova istanza di CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC, inizializzando i parametri seguenti:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ FLAG \_ DI \_ FIRMA RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 ROOT SIGNATURE FLAG \_ \_ \_ \_ NONE

</dd> <dt>

**CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nuova istanza di CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC, inizializzando i parametri seguenti:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ FLAG \_ DI \_ FIRMA RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 ROOT SIGNATURE FLAG \_ \_ \_ \_ NONE

</dd> <dt>

**CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC (CD3DX12 \_ DEFAULT)**
</dt> <dd>

Crea una nuova istanza di CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC, inizializzata con i parametri predefiniti:

UINT numParameters = 0

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = NULL

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ FLAG \_ DI \_ FIRMA RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 ROOT SIGNATURE FLAG \_ \_ \_ \_ NONE

</dd> <dt>

**inline Init \_ 1 \_ 0(UINT numParameters, const D3D12 \_ ROOT PARAMETER \_ \* \_ pParameters, UINT numStaticSamplers = 0, const \_ \_ D3D12 STATIC SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE FLAGS flags = \_ \_ D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ FLAG \_ DI \_ FIRMA RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 ROOT SIGNATURE FLAG \_ \_ \_ \_ NONE

</dd> <dt>

**static inline Init \_ 1 \_ 0(D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC &desc, UINT numParameters, const D3D12 \_ ROOT PARAMETER \_ \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 STATIC \_ \_ \_ SAMPLER DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE FLAGS flags = \_ \_ D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ FLAG \_ DI \_ FIRMA RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 ROOT SIGNATURE FLAG \_ \_ \_ \_ NONE

</dd> <dt>

**inline Init \_ \_ 1 1(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters, UINT numStaticSamplers = 0, const \_ \_ D3D12 STATIC SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE FLAGS flags = \_ \_ D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ FLAG \_ DI \_ FIRMA RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 ROOT SIGNATURE FLAG \_ \_ \_ \_ NONE

</dd> <dt>

**static inline Init \_ \_ 1 1(D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC &desc, UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ \_ SAMPLER DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE FLAGS = \_ \_ D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Specifica una funzione che inizializza i parametri seguenti:

[**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ FLAG \_ DI \_ FIRMA RADICE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 ROOT SIGNATURE FLAG \_ \_ \_ \_ NONE

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[Strutture helper per D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





