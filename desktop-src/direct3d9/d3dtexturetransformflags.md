---
description: Definisce i valori della trasformazione delle coordinate di trama.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Enumerazione D3DTEXTURETRANSFORMFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234959"
---
# <a name="d3dtexturetransformflags-enumeration"></a>Enumerazione D3DTEXTURETRANSFORMFLAGS

Definisce i valori della trasformazione delle coordinate di trama.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**\_Disabilitazione D3DTTFF**
</dt> <dd>

Le coordinate di trama vengono passate direttamente al rasterizzatore.

</dd> <dt>

<span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**\_COUNT1 D3DTTFF**
</dt> <dd>

Il rasterizzatore dovrebbe prevedere le coordinate di trama 1D. Questo valore viene usato dall'elaborazione del vertice della funzione fissa; deve essere impostato su 0 quando si utilizza un vertex shader programmabile.

</dd> <dt>

<span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**\_COUNT2 D3DTTFF**
</dt> <dd>

Il rasterizzatore dovrebbe prevedere le coordinate di trama 2D. Questo valore viene usato dall'elaborazione del vertice della funzione fissa; deve essere impostato su 0 quando si utilizza un vertex shader programmabile.

</dd> <dt>

<span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**\_COUNT3 D3DTTFF**
</dt> <dd>

Il rasterizzatore dovrebbe prevedere le coordinate di trama 3D. Questo valore viene usato dall'elaborazione del vertice della funzione fissa; deve essere impostato su 0 quando si utilizza un vertex shader programmabile.

</dd> <dt>

<span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**\_COUNT4 D3DTTFF**
</dt> <dd>

Il rasterizzatore dovrebbe prevedere le coordinate di trama 4D. Questo valore viene usato dall'elaborazione del vertice della funzione fissa; deve essere impostato su 0 quando si utilizza un vertex shader programmabile.

</dd> <dt>

<span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ proiettato**
</dt> <dd>

Questo flag viene rispettato dalla pipeline di pixel della funzione fissa, nonché dalla pipeline di pixel programmabile nelle versioni PS \_ 1 \_ 1 a PS \_ 1 \_ 3. Quando è abilitata la proiezione di trama per una fase di trama, è necessario scrivere tutti i quattro valori a virgola mobile nel registro di trama corrispondente. Ogni coordinata di trama è divisa per l'ultimo elemento prima del passaggio al rasterizzatore. Se, ad esempio, questo flag viene specificato con il \_ flag D3DTTFF COUNT3, le coordinate della prima e della seconda trama vengono divise per la terza coordinata prima di essere passate al rasterizzatore.

</dd> <dt>

<span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile trasformare le coordinate di trama usando una matrice 4 x 4 prima che i risultati vengano passati al rasterizzatore. Le trasformazioni delle coordinate di trama vengono impostate chiamando [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api)e passando lo \_ stato della fase della trama D3DTSS TEXTURETRANSFORMFLAGS e uno dei valori da **D3DTEXTURETRANSFORMFLAGS**. Per altre informazioni sulle trasformazioni di trama, vedere [trasformazioni di coordinate di trama (Direct3D 9)](texture-coordinate-transformations.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
