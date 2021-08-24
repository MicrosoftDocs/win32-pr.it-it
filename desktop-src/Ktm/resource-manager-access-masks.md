---
description: KTM definisce le maschere di accesso all'integrazione seguenti da usare quando si apre un gestore di risorse.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Resource Manager di accesso alle applicazioni (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ede54d5d49533e70aa9cda2d9c4a363d61f1fdbd894108a5b83f2c5e9efc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146484"
---
# <a name="resource-manager-access-masks"></a>Resource Manager di accesso

KTM definisce le maschere di accesso all'integrazione seguenti da usare quando si apre un gestore di risorse.

<dl> <dt>

<span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**INFORMAZIONI SULLE \_ QUERY DI \_ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Il chiamante può eseguire una query per ottenere informazioni sul gestore di risorse(RM).


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**INFORMAZIONI SUI \_ SET DI \_ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Il chiamante può impostare le informazioni RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RIPRISTINO \_ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Il chiamante può recuperare l'RM specificato.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**INTEGRAZIONE \_ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Il chiamante può integrare un RM in una transazione.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**NOTIFICA GET \_ \_ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Il chiamante può ricevere una notifica per un RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**LETTURA \_ GENERICA RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Il chiamante ha i privilegi seguenti: STANDARD \_ RIGHTS \_ READ, RESOURCEMANAGER \_ QUERY INFORMATION e \_ RESOURCEMANAGER \_ RECOVER.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**SCRITTURA \_ GENERICA RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Il chiamante ha i privilegi seguenti: STANDARD \_ RIGHTS \_ WRITE, RESOURCEMANAGER \_ SET \_ INFORMATION, RESOURCEMANAGER \_ ENLIST e RESOURCEMANAGER GET \_ \_ NOTIFICATION.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**ESECUZIONE \_ GENERICA DI RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Il chiamante ha i privilegi seguenti: STANDARD \_ RIGHTS \_ EXECUTE, RESOURCEMANAGER \_ ENLIST e RESOURCEMANAGER GET \_ \_ NOTIFICATION.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER \_ ALL \_ ACCESS**
</dt> <dd> <dl> <dt>



Il chiamante ha il privilegio seguente: STANDARD \_ RIGHTS \_ REQUIRED.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                           |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




