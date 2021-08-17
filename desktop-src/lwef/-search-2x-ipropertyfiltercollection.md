---
title: Interfaccia IPropertyFilterCollection (WdsSharedIDL.h)
description: Espone le proprietà della raccolta restituita in base alla query inviata.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Interfaccia IPropertyFilterCollection Funzionalità dell'ambiente Windows legacy
- Interfaccia IPropertyFilterCollection Legacy Windows dell'ambiente , descritta
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69fb2f7ce6e100c74046f3402eee3385108723202fbaa6dce01e888bffef4b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349981"
---
# <a name="ipropertyfiltercollection-interface"></a>Interfaccia IPropertyFilterCollection

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Espone le proprietà della raccolta restituita in base alla query inviata.

## <a name="members"></a>Membri

**L'interfaccia IPropertyFilterCollection** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPropertyFilterCollection** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IPropertyFilterCollection** ha queste proprietà.



| Proprietà                                                                         | Tipo di accesso           | Descrizione                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [**Additem**](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | Sola lettura<br/>  | Aggiunge un nuovo filtro alla raccolta. <br/>             |
| [**Chiaro**](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | Sola scrittura<br/> | Cancella la raccolta. <br/>                           |
| [**Conteggio**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | Sola lettura<br/>  | Numero di filtri nella raccolta. <br/>             |
| [**GetITem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | Lettura/Scrittura<br/> | Restituisce un filtro specifico all'interno dell'insieme. <br/> |
| [**Removeitem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | Sola scrittura<br/> | Rimuove un filtro specifico dall'insieme. <br/>     |



 

## <a name="remarks"></a>Commenti

Queste proprietà vengono usate per filtrare la raccolta restituita dalla query.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

