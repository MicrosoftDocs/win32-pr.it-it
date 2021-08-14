---
title: Elemento URI (registrationInfoType)
description: Specifica l'URI dell'attività.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- Elemento URI Utilità di pianificazione
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b9a2d9b8faf327f7b64be2cdd4273f2252405767004dc6e0d58b0c95b5f1910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355604"
---
# <a name="uri-registrationinfotype-element"></a>Elemento URI (registrationInfoType)

Specifica l'URI dell'attività. Questo elemento viene utilizzato per specificare la posizione dell'attività registrata nella gerarchia di cartelle delle attività.

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

**L'elemento URI** è definito dal [**tipo complesso registrationInfoType.**](taskschedulerschema-registrationinfotype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                           | Derivato da                                                                         | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, l'URI dell'attività viene specificato usando la [**proprietà RegistrationInfo.URI.**](registrationinfo-uri.md)

Per lo sviluppo in C++, l'URI dell'attività viene specificato usando la [**proprietà IRegistrationInfo::URI.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





