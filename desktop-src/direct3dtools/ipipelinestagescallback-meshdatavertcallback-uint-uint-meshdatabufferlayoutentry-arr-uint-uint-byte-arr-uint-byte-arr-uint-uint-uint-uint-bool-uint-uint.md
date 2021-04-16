---
description: Callback che notifica all'host delle fasi della pipeline le informazioni mesh restituite dalla richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesCallback:: MeshDataVertCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521386"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>Metodo IPipeLineStagesCallback:: MeshDataVertCallback

Callback che notifica all'host delle fasi della pipeline le informazioni mesh restituite dalla richiesta associata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a>Parametri

*numVertices*   
Numero di vertici nei risultati.

*numBufferLayoutEntries*   
Numero di voci del layout del buffer nei risultati.

*voci di count1 \_*   
Il layout del buffer è intero. Che descrivono la firma di output dello shader.

*stride*   
Dimensione (stride) di un intero blocco di output.

*numVBBytes*   
Dimensioni in byte del buffer del vertice.

*\_pVBData count4*   
Buffer dei vertici.

*numIBBytes*   
Dimensioni in byte del buffer dell'indice.

*\_pIBData count6*   
Buffer dell'indice.

*indexSize*   
Dimensioni in byte di ogni indice.

*IBOffset*   
Offset nel buffer di indice che specifica la posizione in cui gli indici devono iniziare a essere utilizzati.

*baseVertex*   
Offset nel buffer dei vertici che specifica la posizione in cui iniziare a usare i vertici.

*minVertex*   

*IBIndexesVB*   
true quando viene utilizzato il buffer di indice; in caso contrario, false.

*numIndices*   
Numero di indici utilizzati.

*topologia*   
Topolology dello shader. Questa operazione non è necessariamente identica alla topologia della chiamata di progetto associata.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
