---
title: Interfaccia IResultProperty (WdsSharedIDL. h)
description: Espone le proprietà del risultato.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultProperty
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultProperty, descritte
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
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302069"
---
# <a name="iresultproperty-interface"></a>Interfaccia IResultProperty

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Espone le proprietà del risultato.

## <a name="members"></a>Membri

L'interfaccia **IResultProperty** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultProperty** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IResultProperty** dispone di questi metodi.



| Metodo                                                    | Descrizione                 |
|:----------------------------------------------------------|:----------------------------|
| [**GoBack**](-search-2x-iresultproperty-goback.md)       | Non implementato.<br/> |
| [**GoForward**](-search-2x-iresultproperty-goforward.md) | Non implementato.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IResultProperty** ha queste proprietà.



| Proprietà                                                                   | Tipo di accesso          | Descrizione                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**Tipo**](-search-2x-iresultproperty-datatype.md)<br/>         | Sola lettura<br/> | Tipo di dati Properties. <br/>                   |
| [**DisplayName**](-search-2x-iresultproperty-displayname.md)<br/>   | Sola lettura<br/> | Nome visualizzato localizzato della proprietà. <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | Sola lettura<br/> | Visibilità della proprietà. <br/>               |
| [**Suggerimento**](-search-2x-iresultproperty-hint.md)<br/>                 | Sola lettura<br/> | Valore speciale usato per facilitare il recupero dei dati. <br/> |
| [**IndexColumn**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | Sola lettura<br/> | Nome della colonna proprietà nell'indice. <br/>      |
| [**UID**](-search-2x-iresultproperty-uid.md)<br/>                   | Sola lettura<br/> | Identificatore univoco per la proprietà. <br/>       |



 

## <a name="remarks"></a>Commenti

Si tratta degli elementi che restituiscono proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

