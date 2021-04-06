---
title: Elemento URI (registrationInfoType)
description: Specifica l'URI dell'attività.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- Utilità di pianificazione elemento URI
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be3f5782ba5fc02bc3309abfe337c029d0341667
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743751"
---
# <a name="uri-registrationinfotype-element"></a>Elemento URI (registrationInfoType)

Specifica l'URI dell'attività. Questo elemento viene utilizzato per specificare il percorso in cui l'attività registrata viene posizionata nella gerarchia delle cartelle delle attività.

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

L'elemento **URI** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                           | Derivato da                                                                         | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, l'URI dell'attività viene specificato mediante la proprietà [**RegistrationInfo. Uri**](registrationinfo-uri.md) .

Per lo sviluppo in C++, l'URI dell'attività viene specificato mediante la proprietà [**IRegistrationInfo:: URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





