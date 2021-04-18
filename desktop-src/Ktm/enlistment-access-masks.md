---
description: KTM definisce le maschere di accesso all'elenco seguenti da usare per l'apertura delle integrazioni.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Maschere di accesso all'integrazione (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e4ebd67f93368215ebcdcd362595d0341adb52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318298"
---
# <a name="enlistment-access-masks"></a>Maschere di accesso all'elenco

KTM definisce le maschere di accesso all'elenco seguenti da usare per l'apertura delle integrazioni.

<dl> <dt>

<span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**\_informazioni sulle query di integrazione \_**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



Il chiamante può eseguire una query su KTM per ottenere informazioni sull'integrazione.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**\_informazioni sui set di integrazione \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



Il chiamante può impostare informazioni sull'integrazione.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**ripristino dell'elenco \_**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



Il chiamante può recuperare un'integrazione.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**\_diritti subordinati di integrazione \_**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



Il chiamante può completare le azioni eseguite da un gestore di risorse per conto della transazione. Di seguito è riportato un elenco di azioni:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**diritti di integrazione \_ superiore \_**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



Il chiamante può integrarsi nella transazione come gestione transazioni superiore.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**\_lettura generale dell'elenco \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



Il chiamante dispone dei privilegi seguenti: **\_ \_ informazioni sulle query** di lettura e integrazione **\_ dei diritti \_ standard** .


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_scrittura generica di integrazione \_**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



Il chiamante dispone dei privilegi seguenti: **\_ \_ scrittura dei diritti standard**, **\_ \_ informazioni sui set di integrazione** e **\_ ripristino dell'integrazione**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_esecuzione generica dell'elenco \_**
</dt> <dd> <dl> <dt>

0x2001C
</dt> <dt>



Il chiamante dispone dei privilegi seguenti: **diritti \_ standard \_ esecuzione**, **\_ ripristino dell'integrazione** e **\_ \_ diritti subordinati di integrazione**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**ELENCO \_ tutti gli \_ accessi**
</dt> <dd> <dl> <dt>

0xF001F
</dt> <dt>



Questo valore imposta tutti i bit validi per un valore di accesso all'elenco.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                           |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




