---
description: Il filtro renderer null è un renderer che elimina tutti i campioni ricevuti, senza visualizzare o eseguire il rendering dei dati di esempio.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtro renderer null (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 7ff6c728276ca3fd69c14e304780b1d70c563265
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330170"
---
# <a name="null-renderer-filter"></a>Filtro renderer null

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il filtro renderer null è un renderer che elimina tutti i campioni ricevuti, senza visualizzare o eseguire il rendering dei dati di esempio.



|                                          |                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) |
| Tipi di supporti pin di input                    | Qualsiasi tipo di supporto                                                                                                       |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)               |
| Tipi di supporti pin di output                   | Non applicabile.                                                                                                      |
| Interfacce del PIN di output                    | Non applicabile.                                                                                                      |
| CLSID filtro                             | \_NULLRENDERER CLSID                                                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                    |
| File eseguibile                               | Qedit.dll                                                                                                            |
| [Merito](merit.md)                       | il merito non viene \_ \_ \_ utilizzato                                                                                                  |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                        |



 

## <a name="remarks"></a>Commenti

Usare questo filtro quando un pin di output nel grafico richiede una connessione downstream, ma non si vuole eseguire il rendering dei dati dal pin. Connettendo il pin di output al renderer null, si completa la connessione senza eseguire il rendering dei dati.

Anche se questo filtro non esegue il rendering di alcun campione, attende il tempo di presentazione di ogni campione prima di rimuovere l'esempio. Il grafico viene pertanto eseguito alla tariffa normale. Se si desidera che il grafico venga eseguito il più rapidamente possibile, impostare l'orologio di riferimento su **null**. Per altre informazioni, vedere [Setting the Graph Clock](setting-the-graph-clock.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti dei servizi di modifica DirectShow](directshow-editing-services-objects.md)
</dt> </dl>

 

 




