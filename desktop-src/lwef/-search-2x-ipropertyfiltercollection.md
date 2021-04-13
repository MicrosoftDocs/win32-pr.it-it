---
title: Interfaccia IPropertyFilterCollection (WdsSharedIDL. h)
description: Espone le proprietà della raccolta restituita in base alla query inviata.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection, descritte
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
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340853"
---
# <a name="ipropertyfiltercollection-interface"></a>Interfaccia IPropertyFilterCollection

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Espone le proprietà della raccolta restituita in base alla query inviata.

## <a name="members"></a>Membri

L'interfaccia **IPropertyFilterCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPropertyFilterCollection** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IPropertyFilterCollection** ha queste proprietà.



| Proprietà                                                                         | Tipo di accesso           | Descrizione                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [**AddItem**](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | Sola lettura<br/>  | Aggiunge un nuovo filtro alla raccolta. <br/>             |
| [**deselezionare**](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | Sola scrittura<br/> | Cancella la raccolta. <br/>                           |
| [**Conteggio**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | Sola lettura<br/>  | Numero di filtri nella raccolta. <br/>             |
| [**GetITem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | Lettura/Scrittura<br/> | Restituisce un filtro specifico all'interno della raccolta. <br/> |
| [**RemoveItem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | Sola scrittura<br/> | Rimuove un filtro specifico per la raccolta. <br/>     |



 

## <a name="remarks"></a>Commenti

Queste proprietà vengono utilizzate per filtrare la raccolta restituita dalla query.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

