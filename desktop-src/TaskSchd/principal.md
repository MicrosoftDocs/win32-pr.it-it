---
title: Oggetto Principal
description: Oggetto di scripting che fornisce le credenziali di sicurezza per un'entità.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Utilità di pianificazione oggetto principale
- Utilità di pianificazione oggetto principale, descritto
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
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873553"
---
# <a name="principal-object"></a>Oggetto Principal

Oggetto di scripting che fornisce le credenziali di sicurezza per un'entità. Queste credenziali di sicurezza definiscono il contesto di sicurezza per le attività associate all'entità.

## <a name="members"></a>Membri

L'oggetto **Principal** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **Principal** dispone di queste proprietà.



| Proprietà                                                | Tipo di accesso           | Descrizione                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](principal-displayname.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il nome dell'entità visualizzata nell'interfaccia utente di Utilità di pianificazione.<br/>                                                                |
| [**GroupId**](principal-groupid.md)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.<br/>                           |
| [**ID**](principal-id.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore dell'entità.<br/>                                                                                                     |
| [**LogonType**](principal-logontype.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.<br/>                                  |
| [**RunLevel**](principal-runlevel.md)<br/>       | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.<br/> |
| [**UserId**](principal-userid.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore utente necessario per eseguire le attività associate all'entità.<br/>                                        |



 

## <a name="remarks"></a>Commenti

Quando si specifica un account, ricordarsi di usare correttamente la doppia barra rovesciata nel codice per specificare il dominio e il nome utente. Usare, ad esempio, DOMAIN \\ \\ username per specificare un valore per la proprietà [**userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .

Durante la lettura o la scrittura di codice XML per un'attività, le credenziali di sicurezza per un'entità vengono specificate nell'elemento [**Principal**](taskschedulerschema-principal-principaltype-element.md) dello schema utilità di pianificazione.

Se un'attività viene registrata usando lo strumento da riga di comando at.exe e questo oggetto viene usato per recuperare informazioni sull'attività, la proprietà [**LogonType**](principal-logontype.md) restituirà 0, la proprietà [**runlevel**](principal-runlevel.md) restituirà 0 e la proprietà [**userid**](principal-userid.md) non restituirà alcun valore.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





