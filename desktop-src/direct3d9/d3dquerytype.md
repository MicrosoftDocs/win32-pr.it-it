---
description: Identifica il tipo di query.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Enumerazione D3DQUERYTYPE (D3D9Types.h)
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
ms.openlocfilehash: b60f6a52f782efee8647828509e04b99a2ffd94489b9db215158090497947229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732322"
---
# <a name="d3dquerytype-enumeration"></a>Enumerazione D3DQUERYTYPE

Identifica il tipo di query. Per informazioni sulle query, vedere [Query (Direct3D 9)](queries.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_RESOURCEMANAGER    = 5,
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

<span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**
</dt> <dd>

Eseguire una query per gli hint del driver sul layout dei dati per la memorizzazione nella cache dei vertici.

</dd> <dt>

<span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**
</dt> <dd>

Eseguire una query sul gestore delle risorse. Per questa query, i flag di comportamento del dispositivo devono includere [D3DCREATE \_ DISABLE \_ DRIVER \_ MANAGEMENT](d3dcreate.md).

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**
</dt> <dd>

Eseguire query sulle statistiche dei vertici.

</dd> <dt>

<span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**EVENTO D3DQUERYTYPE \_**
</dt> <dd>

Eseguire una query per tutti gli eventi asincroni emessi dalle chiamate API.

</dd> <dt>

<span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**OCCLUSIONE D3DQUERYTYPE \_**
</dt> <dd>

Una query di occlusione restituisce il numero di pixel che superano il test z. Questi pixel sono per primitive disegnate tra il problema [**di D3DISSUE \_ BEGIN**](d3dissue-begin.md) e [**D3DISSUE \_ END**](d3dissue-end.md). Ciò consente a un'applicazione di controllare il risultato dell'occlusione rispetto a 0. Zero è completamente occluso, ovvero i pixel non sono visibili dalla posizione corrente della fotocamera.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE \_ TIMESTAMP**
</dt> <dd>

Restituisce un timestamp a 64 bit.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**TIMESTAMP \_ D3DQUERYTYPEDISJOINT**
</dt> <dd>

Usare questa query per inviare una notifica a un'applicazione se la frequenza del contatore è stata modificata rispetto a D3DQUERYTYPE \_ TIMESTAMP.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**TIMESTAMP D3DQUERYTYPEFREQ \_**
</dt> <dd>

Questo risultato della query è **TRUE** se non è possibile garantire che i valori delle query TIMESTAMP D3DQUERYTYPE siano continui per tutta la durata della \_ query D3DQUERYTYPE \_ TIMESTAMPDISJOINT. In caso contrario, il risultato della query è **FALSE.**

</dd> <dt>

<span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**\_PIPELINE D3DQUERYTYPETIMINGS**
</dt> <dd>

Percentuale di tempo di elaborazione dei dati della pipeline.

</dd> <dt>

<span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**INTERFACCIA \_ D3DQUERYTYPETIMINGS**
</dt> <dd>

Percentuale di tempo di elaborazione dei dati nel driver.

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**
</dt> <dd>

Percentuale di tempo di elaborazione dei dati vertex shader.

</dd> <dt>

<span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**PIXELTIMING D3DQUERYTYPE \_**
</dt> <dd>

Percentuale di tempo di elaborazione pixel shader dati.

</dd> <dt>

<span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**
</dt> <dd>

Confronti delle misurazioni della velocità effettiva per comprendere le prestazioni di un'applicazione.

</dd> <dt>

<span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**
</dt> <dd>

Misurare le prestazioni di hit rate della cache per trame e vertici indicizzati.

</dd> <dt>

<span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**
</dt> <dd>

Efficienza dell'allocazione di memoria contenuta in [**una struttura D3DMEMORYPRESSURE.**](d3dmemorypressure.md)

Differenze tra Direct3D 9 e Direct3D 9Ex:

- D3DQUERYTYPE MEMORYPRESSURE è disponibile solo \_ in Direct3D9Ex in esecuzione in Windows 7 (o più sistema operativo corrente).



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
