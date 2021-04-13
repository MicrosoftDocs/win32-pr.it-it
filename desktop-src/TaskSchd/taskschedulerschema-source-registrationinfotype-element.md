---
title: Elemento Source (registrationInfoType)
description: Specifica la posizione da cui ha avuto origine l'attività. Ad esempio, da un componente, da un servizio, da un'applicazione o da un utente.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Elemento Source Utilità di pianificazione
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400342"
---
# <a name="source-registrationinfotype-element"></a>Elemento Source (registrationInfoType)

Specifica la posizione da cui ha avuto origine l'attività. Ad esempio, da un componente, da un servizio, da un'applicazione o da un utente.

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

L'elemento di **origine** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                           | Derivato da                                                                         | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, l'origine di un'attività viene specificata utilizzando la proprietà [**RegistrationInfo. Source**](registrationinfo-source.md) .

Per lo sviluppo in C++, l'origine di un'attività viene specificata tramite la proprietà [**IRegistrationInfo:: Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) .

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

 

 





