---
title: Oggetto TriggerCollection (Windows. UI. XAML. h)
description: Oggetto di scripting utilizzato per aggiungere, rimuovere e recuperare i trigger di un'attività.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- Triggers Utilità di pianificazione, trigger Collection (oggetto)
- Utilità di pianificazione oggetto TriggerCollection
- Utilità di pianificazione oggetto TriggerCollection, descritto
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
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119379"
---
# <a name="triggercollection-object"></a>TriggerCollection (oggetto)

Oggetto di scripting utilizzato per aggiungere, rimuovere e recuperare i trigger di un'attività.

## <a name="members"></a>Membri

L'oggetto **TriggerCollection** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'oggetto **TriggerCollection** .



| Metodo                                     | Descrizione                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Deselezionare**](triggercollection-clear.md)   | Cancella tutti i trigger dalla raccolta.<br/>                                        |
| [**Creare**](triggercollection-create.md) | Crea un nuovo trigger per l'attività.<br/>                                             |
| [**Rimuovi**](triggercollection-remove.md) | Rimuove il trigger specificato dalla raccolta di trigger utilizzati dall'attività.<br/> |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono impostate dall'oggetto **TriggerCollection** .



| Proprietà                                            | Tipo di accesso          | Descrizione                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Conteggio**](triggercollection-count.md)<br/> | Sola lettura<br/> | Ottiene il numero di trigger nell'insieme.<br/>  |
| [**Elemento**](triggercollection-item.md)<br/>   | Sola lettura<br/> | Ottiene il trigger specificato dalla raccolta.<br/> |



 

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, i trigger per l'attività vengono specificati nell'elemento [**trigger**](taskschedulerschema-triggers-tasktype-element.md) dello schema utilità di pianificazione.

Per informazioni su ogni tipo di trigger, vedere [tipi di trigger](trigger-types.md).

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Windows. UI. XAML. h</dt> </dl> |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trigger**](trigger.md)
</dt> </dl>

 

 





