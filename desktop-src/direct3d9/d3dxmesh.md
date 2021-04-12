---
description: Flag utilizzati per specificare le opzioni di creazione per una mesh.
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Enumerazione D3DXMESH (D3dx9mesh. h)
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
ms.openlocfilehash: 602eb38f2113b54ee02477faf3bdd15a6a924abc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354184"
---
# <a name="d3dxmesh-enumeration"></a>Enumerazione D3DXMESH

Flag utilizzati per specificare le opzioni di creazione per una mesh.

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

<span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH a \_ 32 bit**
</dt> <dd>

La mesh ha indici a 32 bit invece degli indici a 16 bit. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**\_DONOTCLIP D3DXMESH**
</dt> <dd>

Usare il flag di utilizzo di [**\_ DONOTCLIP D3DUSAGE**](d3dusage.md) per i buffer di Vertex e index.

</dd> <dt>

<span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**\_Punti D3DXMESH**
</dt> <dd>

Usare il flag di utilizzo dei [**\_ punti di D3DUSAGE**](d3dusage.md) per i buffer dei vertici e degli indici.

</dd> <dt>

<span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**\_RTPATCHES D3DXMESH**
</dt> <dd>

Usare il flag di utilizzo di [**\_ RTPATCHES D3DUSAGE**](d3dusage.md) per i buffer di Vertex e index.

</dd> <dt>

<span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**\_NPATCHES D3DXMESH**
</dt> <dd>

Se si specifica questo flag, il vertice e il buffer dell'indice della mesh verranno creati con il flag [**D3DUSAGE \_ NPATCHES**](d3dusage.md) . Questa operazione è obbligatoria se è necessario eseguire il rendering dell'oggetto mesh usando la funzionalità di miglioramento della patch N con Direct3D.

</dd> <dt>

<span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**
</dt> <dd>

Usare il flag di utilizzo di [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) per i buffer dei vertici.

</dd> <dt>

<span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ gestito**
</dt> <dd>

Usare il flag di utilizzo [**\_ gestito di D3DPOOL**](./d3dpool.md) per i buffer dei vertici.

</dd> <dt>

<span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**
</dt> <dd>

Usare il flag di utilizzo di [**D3DUSAGE \_ WRITEONLY**](d3dusage.md) per i buffer dei vertici.

</dd> <dt>

<span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ dinamico**
</dt> <dd>

Usare il flag di utilizzo [**\_ dinamico D3DUSAGE**](d3dusage.md) per i buffer dei vertici.

</dd> <dt>

<span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**
</dt> <dd>

Usare il flag di utilizzo di [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) per i buffer dei vertici.

</dd> <dt>

<span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**
</dt> <dd>

Usare il flag di utilizzo di [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) per i buffer di indice.

</dd> <dt>

<span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ gestito**
</dt> <dd>

Usare il flag di utilizzo [**\_ gestito di D3DPOOL**](./d3dpool.md) per i buffer di indice.

</dd> <dt>

<span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**
</dt> <dd>

Usare il flag di utilizzo di [**D3DUSAGE \_ WRITEONLY**](d3dusage.md) per i buffer di indice.

</dd> <dt>

<span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ dinamico**
</dt> <dd>

Usare il flag di utilizzo [**\_ dinamico D3DUSAGE**](d3dusage.md) per i buffer di indice.

</dd> <dt>

<span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**
</dt> <dd>

Usare il flag di utilizzo di [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) per i buffer di indice.

</dd> <dt>

<span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**\_Condivisione VB \_ D3DXMESH**
</dt> <dd>

Forza le mesh clonate a condividere i buffer dei vertici.

</dd> <dt>

<span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**\_USEHWONLY D3DXMESH**
</dt> <dd>

Utilizzare solo l'elaborazione hardware. Per il dispositivo in modalità mista, questo flag farà sì che il sistema usi l'hardware (se supportato nell'hardware) o per impostazione predefinita l'elaborazione del software.

</dd> <dt>

<span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**\_SYSTEMMEM D3DXMESH**
</dt> <dd>

Equivale a specificare sia D3DXMESH \_ VB \_ SYSTEMMEM che D3DXMESH \_ IB \_ SYSTEMMEM.

</dd> <dt>

<span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ gestito**
</dt> <dd>

Equivale a specificare sia \_ gestito D3DXMESH VB \_ che D3DXMESH \_ IB \_ gestito.

</dd> <dt>

<span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**\_WRITEONLY D3DXMESH**
</dt> <dd>

Equivale a specificare sia D3DXMESH \_ VB \_ WRITEONLY che D3DXMESH \_ IB \_ WRITEONLY.

</dd> <dt>

<span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ dinamico**
</dt> <dd>

Equivale a specificare D3DXMESH \_ VB \_ Dynamic e D3DXMESH \_ IB \_ Dynamic.

</dd> <dt>

<span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**\_SOFTWAREPROCESSING D3DXMESH**
</dt> <dd>

Equivale a specificare sia D3DXMESH \_ VB \_ SOFTWAREPROCESSING che D3DXMESH \_ IB \_ SOFTWAREPROCESSING.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una mesh a 32 bit (D3DXMESH a 32 bit \_ ) può supportare teoricamente (2 ^ 32)-1 visi e vertici. Tuttavia, l'allocazione della memoria per una rete di grandi dimensioni in un sistema operativo a 32 bit non è praticabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
