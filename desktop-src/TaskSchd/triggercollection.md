---
title: Oggetto TriggerCollection (Windows.ui.xaml.h)
description: Oggetto di scripting utilizzato per aggiungere, rimuovere e recuperare i trigger di un'attività.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- trigger Utilità di pianificazione , oggetto raccolta trigger
- Oggetto TriggerCollection Utilità di pianificazione
- Oggetto TriggerCollection Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fd103918bc3898e56a3041221c9c70c9ede9aea5df4843cd984f2502279014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001939"
---
# <a name="triggercollection-object"></a>Oggetto TriggerCollection

Oggetto di scripting utilizzato per aggiungere, rimuovere e recuperare i trigger di un'attività.

## <a name="members"></a>Membri

**L'oggetto TriggerCollection** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto TriggerCollection** dispone di questi metodi.



| Metodo                                     | Descrizione                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Cancella**](triggercollection-clear.md)   | Cancella tutti i trigger dalla raccolta.<br/>                                        |
| [**Crea**](triggercollection-create.md) | Crea un nuovo trigger per l'attività.<br/>                                             |
| [**Rimuovi**](triggercollection-remove.md) | Rimuove il trigger specificato dalla raccolta di trigger utilizzati dall'attività.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto TriggerCollection** ha queste proprietà.



| Proprietà                                            | Tipo di accesso          | Descrizione                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Conteggio**](triggercollection-count.md)<br/> | Sola lettura<br/> | Ottiene il numero di trigger nella raccolta.<br/>  |
| [**Elemento**](triggercollection-item.md)<br/>   | Sola lettura<br/> | Ottiene il trigger specificato dalla raccolta.<br/> |



 

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, i trigger per l'attività vengono specificati nell'elemento [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) dello schema Utilità di pianificazione dati.

Per informazioni su ogni tipo di trigger, vedere [Tipi di trigger.](trigger-types.md)

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Windows.ui.xaml.h</dt> </dl> |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trigger**](trigger.md)
</dt> </dl>

 

 





