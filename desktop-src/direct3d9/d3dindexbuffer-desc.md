---
description: Descrive un index buffer.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: D3DINDEXBUFFER_DESC struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a7a25e56ccb9877fad6b370f9ed81c6c7dcf0744a96734b1e17d6dc3abbc0535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804935"
---
# <a name="d3dindexbuffer_desc-structure"></a>Struttura DESC D3DINDEXBUFFER \_

Descrive un index buffer.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro del [tipo enumerato D3DFORMAT,](d3dformat.md) che descrive il formato della superficie index buffer dati.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DRESOURCETYPE,**](./d3dresourcetype.md) che identifica la risorsa come index buffer.

</dd> <dt>

**Utilizzo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinazione di uno o più flag seguenti, specificando l'utilizzo per questa risorsa.



| Valore                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <dt>**D3DUSAGE \_ DONOTCLIP**</dt> </dl>                            | Impostare su per indicare che il index buffer non richiederà mai il ritaglio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <dt>**D3DUSAGE \_ DYNAMIC**</dt> </dl>                                  | Impostare su per indicare che l'index buffer richiede l'uso dinamico della memoria. Ciò è utile per i driver perché consente loro di decidere dove posizionare il buffer. In generale, i buffer di indice statici vengono inseriti nella memoria video e i buffer di indice dinamici vengono inseriti nella memoria AGP. Si noti che non esiste un utilizzo statico separato. se non si specifica D3DUSAGE \_ DYNAMIC, index buffer viene reso statico. D3DUSAGE DYNAMIC viene applicato rigorosamente tramite i flag di blocco \_ \_ D3DLOCK DISCARD e D3DLOCK \_ NOOVERWRITE. Di conseguenza, D3DLOCK DISCARD e D3DLOCK NOOVERWRITE sono validi solo per i buffer di indice creati con \_ \_ D3DUSAGE DYNAMIC; non sono flag validi nei buffer dei vertici \_ statici.<br/> Per altre informazioni sull'uso dei buffer di indice dinamici, vedere [Using Dynamic Vertex and Index Buffers](performance-optimizations.md).<br/> Si noti che non è possibile specificare D3DUSAGE \_ DYNAMIC nei buffer dell'indice gestito. Per altre informazioni, vedere [Gestione delle risorse (Direct3D 9).](managing-resources.md)<br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <dt>**D3DUSAGE \_ RTPATCHES**</dt> </dl>                            | Impostare su per indicare quando index buffer deve essere usato per disegnare primitive di alto livello.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <dt>**D3DUSAGE \_ NPATCHES**</dt> </dl>                               | Impostare su per indicare quando il index buffer deve essere usato per disegnare N patch.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <dt>**PUNTI D3DUSAGE \_**</dt> </dl>                                     | Impostare su per indicare quando il index buffer deve essere usato per gli sprite dei punti di disegno o gli elenchi di punti indicizzati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt> </dl> | Impostare su per indicare che il buffer deve essere usato con l'elaborazione software.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <dt>**D3DUSAGE \_ WRITEONLY**</dt> </dl>                            | Informa il sistema che l'applicazione scrive solo nel index buffer. L'uso di questo flag consente al driver di scegliere la posizione di memoria migliore per operazioni di scrittura e rendering efficienti. I tentativi di lettura da index buffer creati con questa funzionalità possono comportare una riduzione delle prestazioni.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**Pool**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DPOOL,**](./d3dpool.md) che specifica la classe di memoria allocata per questo index buffer.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni del index buffer, in byte.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[Buffer di indice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
