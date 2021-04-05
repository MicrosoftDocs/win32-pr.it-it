---
description: KTM definisce le maschere di accesso all'elenco seguenti da usare all'apertura di un gestore di risorse.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Maschere di accesso Gestione risorse (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131518"
---
# <a name="resource-manager-access-masks"></a>Maschere di accesso Gestione risorse

KTM definisce le maschere di accesso all'elenco seguenti da usare all'apertura di un gestore di risorse.

<dl> <dt>

<span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_ \_ informazioni sulle query RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Il chiamante può eseguire una query per le informazioni di Resource Manager (RM).


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**\_informazioni sui set di RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Il chiamante può impostare le informazioni RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**ripristino di RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Il chiamante può recuperare il RM specificato.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**integrazione di RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Il chiamante può integrare un RM in una transazione.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**\_notifica Get di RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Il chiamante può ricevere una notifica per un RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**\_lettura generica RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Il chiamante dispone dei privilegi seguenti: \_ diritti \_ di lettura standard, \_ \_ informazioni sulle query ResourceManager e \_ ripristino ResourceManager.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_scrittura generica RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Il chiamante presenta i privilegi seguenti: STANDARD \_ Rights \_ Write, ResourceManager \_ set \_ Information, RESOURCEMANAGER \_ integrate e ResourceManager \_ get \_ Notification.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**\_esecuzione generica RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Il chiamante dispone dei privilegi seguenti: \_ diritti standard \_ Execute, ResourceManager \_ integrate e ResourceManager \_ get \_ Notification.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**accesso a RESOURCEMANAGER \_ All \_**
</dt> <dd> <dl> <dt>



Il chiamante dispone del privilegio seguente: \_ diritti standard \_ richiesti.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                           |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




