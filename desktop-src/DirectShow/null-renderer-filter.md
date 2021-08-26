---
description: Il filtro Renderer Null è un renderer che rimuove ogni campione ricevuto, senza visualizzare o eseguire il rendering dei dati di esempio.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtro renderer Null (Qedit.h)
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
ms.openlocfilehash: 2686c64b3251616ac8cefbe81a77282e5b1a7c6847ef965b6361759118b74756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050881"
---
# <a name="null-renderer-filter"></a>Filtro renderer Null

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il filtro Renderer Null è un renderer che rimuove ogni campione ricevuto, senza visualizzare o eseguire il rendering dei dati di esempio.



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) |
| Tipi di supporti pin di input                    | Qualsiasi tipo di supporto                                                                                                       |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)               |
| Tipi di supporti pin di output                   | Non applicabile.                                                                                                      |
| Interfacce pin di output                    | Non applicabile.                                                                                                      |
| Filtro CLSID                             | CLSID \_ NullRenderer                                                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                    |
| File eseguibile                               | Qedit.dll                                                                                                            |
| [Merito](merit.md)                       | MERITO \_ NON \_ \_ USARE                                                                                                  |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                        |



 

## <a name="remarks"></a>Commenti

Usare questo filtro quando un segnaposto di output nel grafico richiede una connessione downstream, ma non si vuole eseguire il rendering dei dati da tale pin. Connettendo il pin di output al renderer Null, si completa la connessione senza eseguire il rendering dei dati.

Anche se questo filtro non esegue il rendering di alcun esempio, attende il tempo di presentazione di ogni campione prima di eliminare l'esempio. Di conseguenza, il grafico verrà eseguito alla velocità normale. Se si desidera che l'esecuzione del grafico sia eseguita il più rapidamente possibile, impostare l'orologio di riferimento su **NULL.** Per altre informazioni, vedere [Impostazione dell'Graph clock](setting-the-graph-clock.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Modifica di oggetti di Servizi](directshow-editing-services-objects.md)
</dt> </dl>

 

 




