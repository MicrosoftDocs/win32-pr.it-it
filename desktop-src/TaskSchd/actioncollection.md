---
title: Oggetto ActionCollection
description: Oggetto di scripting che contiene le azioni eseguite dall'attività.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- Utilità di pianificazione azioni, oggetto Collection
- Utilità di pianificazione oggetto ActionCollection
- Utilità di pianificazione oggetto ActionCollection, descritto
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
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519142"
---
# <a name="actioncollection-object"></a>Oggetto ActionCollection

Oggetto di scripting che contiene le azioni eseguite dall'attività.

## <a name="members"></a>Membri

L'oggetto **ActionCollection** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'oggetto **ActionCollection** .



| Metodo                                    | Descrizione                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [**Deselezionare**](actioncollection-clear.md)   | Cancella tutte le azioni dalla raccolta.<br/>      |
| [**Creare**](actioncollection-create.md) | Crea e aggiunge una nuova azione alla raccolta.<br/> |
| [**Rimuovi**](actioncollection-remove.md) | Rimuove un'azione specificata dalla raccolta.<br/>  |



 

### <a name="properties"></a>Proprietà

L'oggetto **ActionCollection** dispone di queste proprietà.



| Proprietà                                               | Tipo di accesso           | Descrizione                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Context**](actioncollection-context.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore dell'entità per l'attività.<br/> |
| [**Conteggio**](actioncollection-count.md)<br/>     | Sola lettura<br/>  | Ottiene il numero di azioni nella raccolta.<br/>              |
| [**Elemento**](actioncollection-item.md)<br/>       | Sola lettura<br/>  | Ottiene un'azione specificata dalla raccolta.<br/>               |
| [**XmlText**](actioncollection-xmltext.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta una versione in formato XML della raccolta.<br/>   |



 

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML, le azioni di un'attività vengono specificate nell'elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere esempio di [trigger di ora (script)](time-trigger-example--scripting-.md), esempio di [trigger di evento (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), [esempio di trigger giornaliero (scripting)](daily-trigger-example--scripting-.md), [esempio di trigger di registrazione (scripting)](registration-trigger-example--scripting-.md), [esempio di trigger settimanale (scripting)](weekly-trigger-example--scripting-.md), esempio di trigger [Logon (](logon-trigger-example--scripting-.md)scripting) o [esempio di trigger di avvio (script](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





