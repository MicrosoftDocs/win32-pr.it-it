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
ms.openlocfilehash: 64647cbcbcc836c400890fb173a29c76f8723029
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908809"
---
# <a name="null-renderer-filter"></a>Filtro renderer Null

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il filtro Renderer Null è un renderer che rimuove ogni campione ricevuto, senza visualizzare o eseguire il rendering dei dati di esempio.



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) |
| Tipi di supporti pin di input                    | Qualsiasi tipo di supporto                                                                                                       |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)               |
| Tipi di supporti pin di output                   | Non applicabile.                                                                                                      |
| Interfacce pin di output                    | Non applicabile.                                                                                                      |
| Filtro CLSID                             | CLSID \_ NullRenderer                                                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                    |
| File eseguibile                               | Qedit.dll                                                                                                            |
| [Merito](merit.md)                       | NON \_ \_ USARE \_                                                                                                  |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                        |



 

## <a name="remarks"></a>Commenti

Usare questo filtro quando un segnaposto di output nel grafico richiede una connessione downstream, ma non si vuole eseguire il rendering dei dati da tale pin. Connettendo il pin di output al renderer Null, si completa la connessione senza eseguire il rendering dei dati.

Anche se questo filtro non esegue il rendering di alcun esempio, attende l'ora di presentazione di ogni campione prima di eliminarlo. Di conseguenza, il grafico verrà eseguito alla velocità normale. Se si vuole eseguire il grafico il più rapidamente possibile, impostare l'orologio di riferimento su **NULL.** Per altre informazioni, vedere [Impostazione dell'orologio del grafo.](setting-the-graph-clock.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Editing Services Objects](directshow-editing-services-objects.md)
</dt> </dl>

 

 




