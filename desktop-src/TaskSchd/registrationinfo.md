---
title: Oggetto RegistrationInfo
description: Oggetto di scripting che fornisce le informazioni amministrative che possono essere utilizzate per descrivere l'attività.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- informazioni di registrazione Utilità di pianificazione, oggetto
- Utilità di pianificazione oggetto RegistrationInfo
- Oggetto RegistrationInfo Utilità di pianificazione, descritto
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
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048094"
---
# <a name="registrationinfo-object"></a>Oggetto RegistrationInfo

Oggetto di scripting che fornisce le informazioni amministrative che possono essere utilizzate per descrivere l'attività. Queste informazioni includono dettagli quali una descrizione dell'attività, l'autore dell'attività, la data di registrazione dell'attività e il descrittore di sicurezza dell'attività.

## <a name="members"></a>Membri

L'oggetto **RegistrationInfo** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **RegistrationInfo** dispone di queste proprietà.



| Proprietà                                                                     | Tipo di accesso           | Descrizione                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autore**](registrationinfo-author.md)<br/>                         | Lettura/Scrittura<br/> | Ottiene o imposta l'autore dell'attività.<br/>                                                                                            |
| [**Data**](registrationinfo-date.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta la data e l'ora di registrazione dell'attività.<br/>                                                                     |
| [**Descrizione**](registrationinfo-description.md)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta la descrizione dell'attività.<br/>                                                                                       |
| [**Documentazione**](registrationinfo-documentation.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta qualsiasi documentazione aggiuntiva per l'attività.<br/>                                                                         |
| [**SecurityDescriptor**](registrationinfo-securitydescriptor.md)<br/> |                       | Ottiene o imposta il descrittore di sicurezza dell'attività.<br/>                                                                               |
| [**Source (Sorgente)**](registrationinfo-source.md)<br/>                         | Lettura/Scrittura<br/> | Ottiene o imposta il punto da cui ha origine l'attività. Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.<br/> |
| [**URI**](registrationinfo-uri.md)<br/>                               | Lettura/Scrittura<br/> | Ottiene o imposta l'URI dell'attività.<br/>                                                                                               |
| [**Versione**](registrationinfo-version.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta il numero di versione dell'attività.<br/>                                                                                    |
| [**XmlText**](registrationinfo-xmltext.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta una versione in formato XML delle informazioni di registrazione per l'attività.<br/>                                             |



 

## <a name="remarks"></a>Commenti

È possibile utilizzare le informazioni di registrazione per identificare un'attività tramite l'interfaccia utente di Utilità di pianificazione o come criterio di ricerca durante l'enumerazione delle attività registrate.

Durante la lettura o la scrittura di codice XML per un'attività, le informazioni di registrazione per l'attività vengono specificate nell'elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





