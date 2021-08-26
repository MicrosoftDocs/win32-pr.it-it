---
title: Oggetto Principal
description: Oggetto di scripting che fornisce le credenziali di sicurezza per un'entità.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Oggetto Principal Utilità di pianificazione
- Oggetto Principal Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cf4187875f3b02dfbdc8ef5bd9fd8bd43ed99c37134b2c899215decacfb605
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126081"
---
# <a name="principal-object"></a>Oggetto Principal

Oggetto di scripting che fornisce le credenziali di sicurezza per un'entità. Queste credenziali di sicurezza definiscono il contesto di sicurezza per le attività associate all'entità.

## <a name="members"></a>Membri

**L'oggetto Principal** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Principal** ha queste proprietà.



| Proprietà                                                | Tipo di accesso           | Descrizione                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](principal-displayname.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il nome dell'entità visualizzata nell'interfaccia Utilità di pianificazione interfaccia utente.<br/>                                                                |
| [**GroupId**](principal-groupid.md)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.<br/>                           |
| [**Id**](principal-id.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore dell'entità.<br/>                                                                                                     |
| [**LogonType**](principal-logontype.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta il metodo di accesso alla sicurezza necessario per eseguire le attività associate all'entità.<br/>                                  |
| [**Runlevel**](principal-runlevel.md)<br/>       | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.<br/> |
| [**Userid**](principal-userid.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore utente necessario per eseguire le attività associate all'entità.<br/>                                        |



 

## <a name="remarks"></a>Commenti

Quando si specifica un account, ricordarsi di usare correttamente la doppia barra rovesciata nel codice per specificare il dominio e il nome utente. Ad esempio, usare DOMAIN \\ \\ UserName per specificare un valore per la [**proprietà UserId.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid)

Quando si legge o si scrive codice XML per un'attività, le credenziali di sicurezza per un'entità vengono specificate nell'elemento [**Principal**](taskschedulerschema-principal-principaltype-element.md) dello schema Utilità di pianificazione.

Se un'attività viene registrata usando lo strumento da riga di comando at.exe e questo oggetto viene usato per recuperare informazioni sull'attività, la proprietà [**LogonType**](principal-logontype.md) restituirà 0, la proprietà [**RunLevel**](principal-runlevel.md) restituirà 0 e la [**proprietà UserId**](principal-userid.md) restituirà Nothing.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





