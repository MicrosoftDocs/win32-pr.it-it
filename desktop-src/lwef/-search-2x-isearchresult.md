---
title: Interfaccia ISearchResult (WdsSharedIDL. h)
description: Espone informazioni e proprietà relative al set di risultati.
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia ISearchResult
- Funzionalità dell'ambiente Windows legacy dell'interfaccia ISearchResult, descritte
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89387ebe02c87ca6a5c5ac663a67ea060bd78948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742311"
---
# <a name="isearchresult-interface"></a>Interfaccia ISearchResult

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Espone informazioni e proprietà relative al set di risultati.

## <a name="members"></a>Membri

L'interfaccia **ISearchResult** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ISearchResult** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISearchResult** dispone di questi metodi.



| Metodo                                                            | Descrizione                 |
|:------------------------------------------------------------------|:----------------------------|
| [**Disponibilità**](-search-2x-isearchresult-availability.md)     | Non implementato.<br/> |
| [**DoVerb**](-search-2x-isearchresult-doverb.md)                 | Non implementato.<br/> |
| [**GetIcon**](-search-2x-isearchresult-geticon.md)               | Non implementato.<br/> |
| [**GetThumbnail**](-search-2x-isearchresult-getthumbnail.md)     | Non implementato.<br/> |
| [**GetValue**](-search-2x-isearchresult-getvalue.md)             | Non implementato.<br/> |
| [**Getverbi**](-search-2x-isearchresult-getverb.md)               | Non implementato.<br/> |
| [**IconCount**](-search-2x-isearchresult-iconcount.md)           | Non implementato.<br/> |
| [**Index**](-search-2x-isearchresult-index.md)                   | Non implementato.<br/> |
| [**LoadState**](-search-2x-isearchresult-loadstate.md)           | Non implementato.<br/> |
| [**Visualizzatore anteprima**](-search-2x-isearchresult-previewer.md)           | Non implementato.<br/> |
| [**PutValue**](-search-2x-isearchresult-putvalue.md)             | Non implementato.<br/> |
| [**ThumbnailState**](-search-2x-isearchresult-thumbnailstate.md) | Non implementato.<br/> |
| [**Tipo**](-search-2x-isearchresult-type.md)                     | Non implementato.<br/> |
| [**VerbCount**](-search-2x-isearchresult-verbcount.md)           | Non implementato.<br/> |



 

## <a name="remarks"></a>Commenti

Questi metodi espongono proprietà e azioni applicabili al set di risultati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

