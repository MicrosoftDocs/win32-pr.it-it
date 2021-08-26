---
title: Oggetto RegistrationInfo
description: Oggetto di scripting che fornisce le informazioni amministrative che possono essere utilizzate per descrivere l'attività.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- informazioni di registrazione Utilità di pianificazione, oggetto
- Oggetto RegistrationInfo Utilità di pianificazione
- Oggetto RegistrationInfo Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85bb423ae27a3d0b0b15f7b04d287a749f4fe23f3a4b58f7c2462b487b8a705
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072651"
---
# <a name="registrationinfo-object"></a>Oggetto RegistrationInfo

Oggetto di scripting che fornisce le informazioni amministrative che possono essere utilizzate per descrivere l'attività. Queste informazioni includono dettagli quali una descrizione dell'attività, l'autore dell'attività, la data di registrazione dell'attività e il descrittore di sicurezza dell'attività.

## <a name="members"></a>Membri

**L'oggetto RegistrationInfo** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto RegistrationInfo** ha queste proprietà.



| Proprietà                                                                     | Tipo di accesso           | Descrizione                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autore**](registrationinfo-author.md)<br/>                         | Lettura/Scrittura<br/> | Ottiene o imposta l'autore dell'attività.<br/>                                                                                            |
| [**Data**](registrationinfo-date.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta la data e l'ora di registrazione dell'attività.<br/>                                                                     |
| [**Descrizione**](registrationinfo-description.md)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta la descrizione dell'attività.<br/>                                                                                       |
| [**Documentazione**](registrationinfo-documentation.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta qualsiasi documentazione aggiuntiva per l'attività.<br/>                                                                         |
| [**SecurityDescriptor**](registrationinfo-securitydescriptor.md)<br/> |                       | Ottiene o imposta il descrittore di sicurezza dell'attività.<br/>                                                                               |
| [**Source (Sorgente)**](registrationinfo-source.md)<br/>                         | Lettura/Scrittura<br/> | Ottiene o imposta l'origine dell'attività. Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.<br/> |
| [**URI**](registrationinfo-uri.md)<br/>                               | Lettura/Scrittura<br/> | Ottiene o imposta l'URI dell'attività.<br/>                                                                                               |
| [**Versione**](registrationinfo-version.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta il numero di versione dell'attività.<br/>                                                                                    |
| [**Xmltext**](registrationinfo-xmltext.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta una versione in formato XML delle informazioni di registrazione per l'attività.<br/>                                             |



 

## <a name="remarks"></a>Commenti

Le informazioni di registrazione possono essere usate per identificare un'attività tramite l'interfaccia utente di Utilità di pianificazione o come criteri di ricerca durante l'enumerazione delle attività registrate.

Durante la lettura o la scrittura di codice XML per un'attività, le informazioni di registrazione per l'attività vengono specificate [**nell'elemento RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) dello schema Utilità di pianificazione dati.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





