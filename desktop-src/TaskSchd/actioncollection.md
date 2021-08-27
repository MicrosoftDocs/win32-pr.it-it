---
title: Oggetto ActionCollection
description: Oggetto di scripting che contiene le azioni eseguite dall'attività.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- azioni Utilità di pianificazione , oggetto raccolta
- Oggetto ActionCollection Utilità di pianificazione
- Oggetto ActionCollection Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5356757d232570a31f5c8d05e01b695f130a33e34c1c0e98689b1c74feba40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011721"
---
# <a name="actioncollection-object"></a>Oggetto ActionCollection

Oggetto di scripting che contiene le azioni eseguite dall'attività.

## <a name="members"></a>Membri

**L'oggetto ActionCollection** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto ActionCollection** dispone di questi metodi.



| Metodo                                    | Descrizione                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [**Cancella**](actioncollection-clear.md)   | Cancella tutte le azioni dalla raccolta.<br/>      |
| [**Crea**](actioncollection-create.md) | Crea e aggiunge una nuova azione alla raccolta.<br/> |
| [**Rimuovi**](actioncollection-remove.md) | Rimuove un'azione specificata dalla raccolta.<br/>  |



 

### <a name="properties"></a>Proprietà

**L'oggetto ActionCollection** ha queste proprietà.



| Proprietà                                               | Tipo di accesso           | Descrizione                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Context**](actioncollection-context.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore dell'entità per l'attività.<br/> |
| [**Conteggio**](actioncollection-count.md)<br/>     | Sola lettura<br/>  | Ottiene il numero di azioni nella raccolta.<br/>              |
| [**Elemento**](actioncollection-item.md)<br/>       | Sola lettura<br/>  | Ottiene un'azione specificata dalla raccolta.<br/>               |
| [**Xmltext**](actioncollection-xmltext.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta una versione in formato XML dell'insieme.<br/>   |



 

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML, le azioni di un'attività vengono specificate [**nell'elemento Actions**](taskschedulerschema-actions-tasktype-element.md) dello schema Utilità di pianificazione dati.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere Time [Trigger Example (Scripting) (Esempio](time-trigger-example--scripting-.md)di trigger di ora (scripting), Event [Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))(Esempio di trigger di evento (scripting), [Daily Trigger Example (Scripting) (Esempio](daily-trigger-example--scripting-.md)di trigger giornaliero (scripting), Registration [Trigger Example (Scripting) (Esempio](registration-trigger-example--scripting-.md)di trigger di registrazione -Scripting), Weekly [Trigger Example (Scripting) (Esempio](weekly-trigger-example--scripting-.md)di trigger settimanale -Scripting), [Logon Trigger Example (Scripting) (Esempio](logon-trigger-example--scripting-.md)di trigger di accesso (scripting) ) o Boot [Trigger Example (Scripting) (Esempio](boot-trigger-example--scripting-.md)di trigger di avvio (scripting) ).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





