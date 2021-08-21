---
title: Interfaccia IResultProperty (WdsSharedIDL.h)
description: Espone le proprietà dei risultati.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Interfaccia IResultProperty Legacy Windows'ambiente
- Interfaccia IResultProperty Legacy Windows dell'ambiente , descritta
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efba214aaaadec2cfad52db02f9f4f18d289b0b3ee9df37ee60295d5499241e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754584"
---
# <a name="iresultproperty-interface"></a>Interfaccia IResultProperty

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Espone le proprietà dei risultati.

## <a name="members"></a>Membri

**L'interfaccia IResultProperty** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IResultProperty** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IResultProperty** include questi metodi.



| Metodo                                                    | Descrizione                 |
|:----------------------------------------------------------|:----------------------------|
| [**GoBack**](-search-2x-iresultproperty-goback.md)       | Non implementato.<br/> |
| [**Goforward**](-search-2x-iresultproperty-goforward.md) | Non implementato.<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IResultProperty** ha queste proprietà.



| Proprietà                                                                   | Tipo di accesso          | Descrizione                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**Datatype**](-search-2x-iresultproperty-datatype.md)<br/>         | Sola lettura<br/> | Tipo di dati properties. <br/>                   |
| [**Displayname**](-search-2x-iresultproperty-displayname.md)<br/>   | Sola lettura<br/> | Nome visualizzato localizzato della proprietà. <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | Sola lettura<br/> | Fattibilità della proprietà. <br/>               |
| [**Suggerimento**](-search-2x-iresultproperty-hint.md)<br/>                 | Sola lettura<br/> | Valore speciale utilizzato per facilitare il recupero dei dati. <br/> |
| [**IndexColumn**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | Sola lettura<br/> | Nome della colonna Properties nell'indice. <br/>      |
| [**UID**](-search-2x-iresultproperty-uid.md)<br/>                   | Sola lettura<br/> | Identificatore univoco della proprietà. <br/>       |



 

## <a name="remarks"></a>Commenti

Questi sono gli elementi che restituiscono proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

