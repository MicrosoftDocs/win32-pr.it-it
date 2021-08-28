---
description: Filtro renderer del flusso di file
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtro renderer del flusso di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d438d77b4f402cefed2e80f2c32d061d1652710f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987864"
---
# <a name="file-stream-renderer-filter"></a>Filtro renderer del flusso di file

Il filtro Renderer del flusso di file esegue il rendering dei nomi di file analizzati dal filtro [del parser multi-file.](multi-file-parser-filter.md) Per altre informazioni, vedere la documentazione relativa a tale filtro.

L'uso di questo filtro è deprecato. Per eseguire il rendering di più file all'interno dello stesso grafo di filtro, l'applicazione deve semplicemente chiamare **RenderFile** o **AddSourceFilter** più volte.




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Tipi di supporti pin di input | <ul><li>Tipo principale: MEDIATYPE_File</li><li>Sottotipo: GUID_NULL</li><li>Tipo di formato: MEDIATYPE_File</li></ul> | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | Nessuno | 
| Interfacce pin di output | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a> | 
| Filtro CLSID | CLSID_FileRend | 
| File eseguibile | Quartz.dll | 
| <a href="merit.md">Merito</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Commenti

Il CLSID del filtro non è definito in Uuids.h. Usare questa macro nel proprio file di intestazione:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



