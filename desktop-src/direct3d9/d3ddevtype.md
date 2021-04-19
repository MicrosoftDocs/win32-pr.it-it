---
description: Definisce i tipi di dispositivo.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Enumerazione D3DDEVTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322395"
---
# <a name="d3ddevtype-enumeration"></a>Enumerazione D3DDEVTYPE

Definisce i tipi di dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**\_Hal D3DDEVTYPE**
</dt> <dd>

Rasterizzazione dell'hardware. L'ombreggiatura viene eseguita con software, hardware o trasformazione mista e illuminazione.

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**\_NULLREF D3DDEVTYPE**
</dt> <dd>

Inizializzare Direct3D in un computer che non ha né hardware né la rasterizzazione dei riferimenti disponibile e abilitare le risorse per la creazione di contenuto 3D. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ ref**
</dt> <dd>

Le funzionalità Direct3D sono implementate nel software; Tuttavia, l'rasterizzazione dei riferimenti usa istruzioni della CPU speciali ogni volta che è possibile.

Il dispositivo di riferimento viene installato da Windows SDK 8,0 o versione successiva ed è pensato come supporto per il debug solo a scopo di sviluppo.

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

Un dispositivo software collegabile che è stato registrato con [**IDirect3D9:: RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutti i metodi dell'interfaccia [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) che accettano un tipo di dispositivo **D3DDEVTYPE** avranno esito negativo se \_ si specifica D3DDEVTYPE NULLREF. Per usare questi metodi, sostituire D3DDEVTYPE \_ ref nella chiamata al metodo.

\_È necessario creare un dispositivo Ref D3DDEVTYPE in D3DPOOL \_ Scratch Memory, a meno che non siano necessari buffer di Vertex e index. Per supportare i buffer dei vertici e degli indici, creare il dispositivo in D3DPOOL \_ SYSTEMMEM Memory.

Se D3dref9.dll è installato, Direct3D utilizzerà l'unità di rasterizzazione dei riferimenti per creare un \_ tipo di dispositivo Ref D3DDEVTYPE, anche se \_ è specificato D3DDEVTYPE NULLREF. Se D3dref9.dll non è disponibile e \_ viene specificato D3DDEVTYPE NULLREF, Direct3D non eseguirà né il rendering né la presentazione della scena.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[**\_Parametri di creazione D3DDEVICE \_**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
