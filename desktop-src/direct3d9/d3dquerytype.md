---
description: Identifica il tipo di query.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Enumerazione D3DQUERYTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 21cb3e2f2254d54caacd4217d3e0023446a0c6f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322918"
---
# <a name="d3dquerytype-enumeration"></a>Enumerazione D3DQUERYTYPE

Identifica il tipo di query. Per informazioni sulle query, vedere [query (Direct3D 9)](queries.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_ResourceManager    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**\_VCACHE D3DQUERYTYPE**
</dt> <dd>

Query per gli hint driver sul layout dei dati per la memorizzazione nella cache dei vertici.

</dd> <dt>

<span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**\_RESOURCEMANAGER D3DQUERYTYPE**
</dt> <dd>

Eseguire una query in Resource Manager. Per questa query, i flag di comportamento del dispositivo devono includere [D3DCREATE \_ Disable \_ driver \_ Management](d3dcreate.md).

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**\_VERTEXSTATS D3DQUERYTYPE**
</dt> <dd>

Eseguire query sulle statistiche del vertice.

</dd> <dt>

<span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**\_Evento D3DQUERYTYPE**
</dt> <dd>

Eseguire una query per tutti gli eventi asincroni emessi dalle chiamate API.

</dd> <dt>

<span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**\_Occlusione D3DQUERYTYPE**
</dt> <dd>

Una query di occlusione restituisce il numero di pixel che superano il test z. Questi pixel sono per le primitive tracciate tra il problema di [**D3DISSUE \_ Begin**](d3dissue-begin.md) e [**D3DISSUE \_ end**](d3dissue-end.md). Questo consente a un'applicazione di verificare il risultato dell'occlusione rispetto a 0. Zero è completamente nascosto, il che significa che i pixel non sono visibili dalla posizione corrente della fotocamera.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**\_Timestamp D3DQUERYTYPE**
</dt> <dd>

Restituisce un timestamp a 64 bit.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**\_TIMESTAMPDISJOINT D3DQUERYTYPE**
</dt> <dd>

Usare questa query per notificare a un'applicazione se la frequenza del contatore è cambiata rispetto al \_ timestamp D3DQUERYTYPE.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**\_TIMESTAMPFREQ D3DQUERYTYPE**
</dt> <dd>

Il risultato della query è **true** se \_ non è possibile garantire che i valori delle query timestamp D3DQUERYTYPE siano continui per tutta la durata della \_ query TIMESTAMPDISJOINT D3DQUERYTYPE. In caso contrario, il risultato della query è **false**.

</dd> <dt>

<span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**\_PIPELINETIMINGS D3DQUERYTYPE**
</dt> <dd>

Percentuale del tempo di elaborazione dei dati della pipeline.

</dd> <dt>

<span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**\_INTERFACETIMINGS D3DQUERYTYPE**
</dt> <dd>

Percentuale del tempo di elaborazione dei dati nel driver.

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**\_VERTEXTIMINGS D3DQUERYTYPE**
</dt> <dd>

Percentuale del tempo di elaborazione dei dati del vertex shader.

</dd> <dt>

<span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**\_PIXELTIMINGS D3DQUERYTYPE**
</dt> <dd>

Percentuale del tempo di elaborazione dei dati pixel shader.

</dd> <dt>

<span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**\_BANDWIDTHTIMINGS D3DQUERYTYPE**
</dt> <dd>

Confronti di misurazione della velocità effettiva per aiutare a comprendere le prestazioni di un'applicazione.

</dd> <dt>

<span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**\_CACHEUTILIZATION D3DQUERYTYPE**
</dt> <dd>

Misura le prestazioni della frequenza di riscontri nella cache per le trame e i vertici indicizzati.

</dd> <dt>

<span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**\_MEMORYPRESSURE D3DQUERYTYPE**
</dt> <dd>

Efficienza dell'allocazione di memoria contenuta in una struttura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .



|                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> D3DQUERYTYPE \_ MEMORYPRESSURE è disponibile solo in Direct3D9Ex in esecuzione su Windows 7 (o più sistemi operativi correnti).<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
