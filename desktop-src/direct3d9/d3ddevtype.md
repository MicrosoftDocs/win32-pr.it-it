---
description: Definisce i tipi di dispositivo.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Enumerazione D3DDEVTYPE (D3D9Types.h)
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
ms.openlocfilehash: d311706d328a5d05668a4d1dcddb032f17fba0c69e48286f899875a8da6a650e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732991"
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

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE \_ HAL**
</dt> <dd>

Rasterizzazione dell'hardware. L'ombreggiatura viene eseguita con software, hardware o trasformazione e illuminazione miste.

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NULLREF**
</dt> <dd>

Inizializzare Direct3D in un computer in cui non sono disponibili hardware né rasterizzazione dei riferimenti e abilitare le risorse per la creazione di contenuto 3D. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ REF**
</dt> <dd>

Le funzionalità Direct3D vengono implementate nel software. Tuttavia, l'rasterizzazione dei riferimenti usa istruzioni speciali della CPU ogni volta che è possibile.

Il dispositivo di riferimento viene installato da Windows SDK 8.0 o versione successiva ed è progettato come supporto per il debug solo per lo sviluppo.

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

Un dispositivo software collegabile registrato con [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutti i metodi [**dell'interfaccia IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) che accettano un tipo di dispositivo **D3DDEVTYPE** avranno esito negativo se si specifica D3DDEVTYPE \_ NULLREF. Per usare questi metodi, sostituire D3DDEVTYPE \_ REF nella chiamata al metodo.

È necessario creare un dispositivo D3DDEVTYPE REF nella memoria \_ D3DPOOL SCRATCH, a meno che non siano necessari buffer di vertici \_ e indici. Per supportare i buffer dei vertici e degli indici, creare il dispositivo nella memoria \_ SYSTEMMEM D3DPOOL.

Se D3dref9.dll installato, Direct3D userà l'unità di rasterizzazione dei riferimenti per creare un tipo di dispositivo D3DDEVTYPE REF, anche se è specificato \_ D3DDEVTYPE \_ NULLREF. Se D3dref9.dll non è disponibile ed è specificato D3DDEVTYPE NULLREF, Direct3D non eseguirà il rendering né \_ presenterà la scena.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[**PARAMETRI DI CREAZIONE DEL DISPOSITIVO D3D \_ \_**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
