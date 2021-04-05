---
description: Descrive un buffer di indice.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: Struttura D3DINDEXBUFFER_DESC (D3D9Types. h)
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
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969384"
---
# <a name="d3dindexbuffer_desc-structure"></a>\_Struttura D3DINDEXBUFFER DESC

Descrive un buffer di indice.

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

Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato di superficie dei dati del buffer dell'indice.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membro del tipo enumerato [**D3DRESOURCETYPE**](./d3dresourcetype.md) , che identifica questa risorsa come buffer di indice.

</dd> <dt>

**Utilizzo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinazione di uno o più dei flag seguenti, che specifica l'utilizzo della risorsa.



| Valore                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <dt>**\_DONOTCLIP D3DUSAGE**</dt> </dl>                            | Impostare per indicare che il contenuto del buffer dell'indice non richiede mai il ritaglio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <dt>**D3DUSAGE \_ dinamico**</dt> </dl>                                  | Impostare per indicare che il buffer dell'indice richiede l'utilizzo della memoria dinamica. Questa operazione è utile per i driver perché consente loro di decidere dove posizionare il buffer. In generale, i buffer di indice statici vengono inseriti nella memoria video e i buffer degli indici dinamici vengono inseriti nella memoria AGP. Si noti che non esiste un utilizzo statico separato; Se non si specifica D3DUSAGE \_ Dynamic, il buffer di indice viene reso statico. \_La dinamica D3DUSAGE viene applicata rigorosamente tramite i \_ flag di blocco D3DLOCK scartit e D3DLOCK \_ nowrite. Di conseguenza, i D3DLOCK di \_ eliminazione e D3DLOCK \_ nowrite sono validi solo per i buffer di indice creati con D3DUSAGE \_ Dynamic; non sono flag validi per i buffer dei vertici statici.<br/> Per ulteriori informazioni sull'utilizzo dei buffer di indice dinamici, vedere [utilizzo dei buffer di indice e di vertex dinamici](performance-optimizations.md).<br/> Si noti che \_ non è possibile specificare D3DUSAGE Dynamic nei buffer dell'indice gestito. Per ulteriori informazioni, vedere [gestione delle risorse (Direct3D 9)](managing-resources.md).<br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <dt>**\_RTPATCHES D3DUSAGE**</dt> </dl>                            | Impostare per indicare quando il buffer dell'indice deve essere utilizzato per il disegno di primitive di ordine superiore.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <dt>**\_NPATCHES D3DUSAGE**</dt> </dl>                               | Impostare per indicare quando deve essere utilizzato il buffer di indice per disegnare N patch.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <dt>**\_Punti D3DUSAGE**</dt> </dl>                                     | Impostare per indicare quando deve essere utilizzato il buffer di indice per gli sprite del punto di disegno o gli elenchi di punti indicizzati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <dt>**\_SOFTWAREPROCESSING D3DUSAGE**</dt> </dl> | Impostare per indicare che il buffer deve essere utilizzato con l'elaborazione del software.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <dt>**\_WRITEONLY D3DUSAGE**</dt> </dl>                            | Informa il sistema che l'applicazione scrive solo nel buffer dell'indice. L'utilizzo di questo flag consente al driver di scegliere la migliore posizione di memoria per operazioni di scrittura e rendering efficienti. Il tentativo di leggere da un buffer di indice creato con questa funzionalità può comportare un peggioramento delle prestazioni.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**Pool**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che specifica la classe di memoria allocata per questo buffer di indice.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni in byte del buffer dell'indice.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Getdesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[Buffer di indice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
