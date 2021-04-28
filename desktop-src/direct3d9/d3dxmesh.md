---
description: 'Enumerazione D3DXMESH: flag usati per specificare le opzioni di creazione per una mesh.'
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Enumerazione D3DXMESH (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a312c2618960691184182039afe38acc8947eb6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098099"
---
# <a name="d3dxmesh-enumeration"></a>Enumerazione D3DXMESH

Flag usati per specificare le opzioni di creazione per una mesh.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32 BIT**
</dt> <dd>

La mesh ha indici a 32 bit anziché indici a 16 bit. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**
</dt> <dd>

Usare il flag [**di utilizzo D3DUSAGE \_ DONOTCLIP**](d3dusage.md) per i buffer dei vertici e degli indici.

</dd> <dt>

<span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**PUNTI D3DXMESH \_**
</dt> <dd>

Usare il flag [**di utilizzo D3DUSAGE \_ POINTS**](d3dusage.md) per i buffer dei vertici e degli indici.

</dd> <dt>

<span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**
</dt> <dd>

Usare il flag [**di utilizzo D3DUSAGE \_ RTPATCHES**](d3dusage.md) per i buffer dei vertici e degli indici.

</dd> <dt>

<span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**
</dt> <dd>

Se si specifica questo flag, il vertice e index buffer della mesh vengono creati con il flag [**D3DUSAGE \_ NPATCHES.**](d3dusage.md) Questa operazione è necessaria se è necessario eseguire il rendering dell'oggetto mesh usando il miglioramento della patch N tramite Direct3D.

</dd> <dt>

<span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**
</dt> <dd>

Usare il flag [**di utilizzo D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) per i vertex buffer.

</dd> <dt>

<span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ MANAGED**
</dt> <dd>

Usare il flag [**di utilizzo D3DPOOL \_ MANAGED**](./d3dpool.md) per i vertex buffer.

</dd> <dt>

<span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**
</dt> <dd>

Usare il flag [**di utilizzo D3DUSAGE \_ WRITEONLY**](d3dusage.md) per i vertex buffer.

</dd> <dt>

<span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ DYNAMIC**
</dt> <dd>

Usare il flag [**D3DUSAGE \_ DYNAMIC**](d3dusage.md) usage per i vertex buffer.

</dd> <dt>

<span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**
</dt> <dd>

Usare il flag [**di utilizzo D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) per i vertex buffer.

</dd> <dt>

<span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**
</dt> <dd>

Usare il flag [**di utilizzo D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) per i buffer di indice.

</dd> <dt>

<span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ MANAGED**
</dt> <dd>

Usare il flag [**di utilizzo gestito D3DPOOL \_**](./d3dpool.md) per i buffer di indice.

</dd> <dt>

<span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**
</dt> <dd>

Usare il flag [**di utilizzo D3DUSAGE \_ WRITEONLY**](d3dusage.md) per i buffer di indice.

</dd> <dt>

<span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ DYNAMIC**
</dt> <dd>

Usare il flag [**D3DUSAGE \_ DYNAMIC**](d3dusage.md) usage per i buffer di indice.

</dd> <dt>

<span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**SOFTWARE IB D3DXMESHPROCESSING \_ \_**
</dt> <dd>

Usare il flag [**di utilizzo D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) per i buffer di indice.

</dd> <dt>

<span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH \_ VB \_ SHARE**
</dt> <dd>

Forza le mesh clonate a condividere i vertex buffer.

</dd> <dt>

<span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**
</dt> <dd>

Usare solo l'elaborazione hardware. Per il dispositivo in modalità mista, questo flag fa sì che il sistema usi l'hardware (se supportato nell'hardware) o per impostazione predefinita l'elaborazione software.

</dd> <dt>

<span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**
</dt> <dd>

Equivale a specificare sia D3DXMESH \_ VB \_ SYSTEMMEM che D3DXMESH \_ IB \_ SYSTEMMEM.

</dd> <dt>

<span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ GESTITO**
</dt> <dd>

Equivale a specificare sia D3DXMESH \_ VB \_ MANAGED che D3DXMESH \_ IB \_ MANAGED.

</dd> <dt>

<span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**
</dt> <dd>

Equivale a specificare sia D3DXMESH \_ VB \_ WRITEONLY che D3DXMESH \_ IB \_ WRITEONLY.

</dd> <dt>

<span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ DYNAMIC**
</dt> <dd>

Equivale a specificare sia D3DXMESH \_ VB \_ DYNAMIC che D3DXMESH \_ IB \_ DYNAMIC.

</dd> <dt>

<span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**SOFTWARE D3DXMESHPROCESSING \_**
</dt> <dd>

Equivale a specificare sia D3DXMESH \_ VB \_ SOFTWAREPROCESSING che D3DXMESH \_ IB \_ SOFTWAREPROCESSING.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una mesh a 32 bit (D3DXMESH 32BIT) può teoricamente \_ supportare (2^32)-1 visi e vertici. Tuttavia, l'allocazione di memoria per una mesh di grandi dimensioni in un sistema operativo a 32 bit non è pratica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
