---
description: Gli Stati del campionatore definiscono le operazioni di campionamento della trama, ad esempio l'indirizzamento della trama e
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Enumerazione D3DSAMPLERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322440"
---
# <a name="d3dsamplerstatetype-enumeration"></a>Enumerazione D3DSAMPLERSTATETYPE

Gli Stati del campionatore definiscono le operazioni di campionamento della trama, ad esempio l'indirizzamento della trama e Alcuni Stati del campionatore configurano l'elaborazione dei vertici e alcune impostazioni di elaborazione dei pixel. Gli Stati del campionatore possono essere salvati e ripristinati usando stateblocks (vedere lo stato [di salvataggio e ripristino del blocco di stato (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**\_Indirizzo D3DSAMP**
</dt> <dd>

Modalità di indirizzamento della trama per la coordinata u. Il valore predefinito è D3DTADDRESS \_ wrap. Per ulteriori informazioni, vedere [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**\_ADDRESSV D3DSAMP**
</dt> <dd>

Modalità di indirizzo della trama per la coordinata v. Il valore predefinito è D3DTADDRESS \_ wrap. Per ulteriori informazioni, vedere [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**\_ADDRESSW D3DSAMP**
</dt> <dd>

Modalità di indirizzamento della trama per la coordinata w. Il valore predefinito è D3DTADDRESS \_ wrap. Per ulteriori informazioni, vedere [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**\_BorderColor D3DSAMP**
</dt> <dd>

Colore del bordo o tipo [**D3DCOLOR**](d3dcolor.md). Il colore predefinito è 0x00000000.

</dd> <dt>

<span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**\_MAGFILTER D3DSAMP**
</dt> <dd>

Filtro di ingrandimento di tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). Il valore predefinito è D3DTEXF \_ Point.

</dd> <dt>

<span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**\_MINFILTER D3DSAMP**
</dt> <dd>

Filtro minification di tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). Il valore predefinito è D3DTEXF \_ Point.

</dd> <dt>

<span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**\_MIPFILTER D3DSAMP**
</dt> <dd>

Filtro mipmap da utilizzare durante minification. Vedere [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). Il valore predefinito è D3DTEXF \_ None.

</dd> <dt>

<span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**\_MIPMAPLODBIAS D3DSAMP**
</dt> <dd>

Distorsione del livello di dettaglio del mipmap. Il valore predefinito è zero.

</dd> <dt>

<span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**\_MAXMIPLEVEL D3DSAMP**
</dt> <dd>

Indice del livello di dettaglio della mappa più grande da usare. I valori sono compresi tra 0 e (n-1), dove 0 è il più grande. Il valore predefinito è zero.

</dd> <dt>

<span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**\_MAXANISOTROPY D3DSAMP**
</dt> <dd>

Anisotropia massima DWORD. I valori sono compresi tra 1 e il valore specificato nel membro **MaxAnisotropy** della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . Il valore predefinito è 1.

</dd> <dt>

<span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**\_SRGBTEXTURE D3DSAMP**
</dt> <dd>

Valore di correzione gamma. Il valore predefinito è 0, che indica che la gamma è 1,0 e non è richiesta alcuna correzione. In caso contrario, questo valore indica che il campionatore deve presupporre gamma di 2,2 sul contenuto e convertirlo in lineare (gamma 1,0) prima di presentarlo alla pixel shader.

</dd> <dt>

<span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**\_ELEMENTINDEX D3DSAMP**
</dt> <dd>

Quando una trama a più elementi viene assegnata al campionatore, indica l'indice dell'elemento da usare. Il valore predefinito è 0.

</dd> <dt>

<span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**\_DMAPOFFSET D3DSAMP**
</dt> <dd>

Offset del vertice nella mappa di spostamento precampionata. Si tratta di una costante utilizzata da mosaico, il cui valore predefinito è 0.

</dd> <dt>

<span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
