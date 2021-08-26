---
description: KTM definisce le maschere di accesso all'integrazione seguenti da usare quando si aprono le integrazioni.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Maschere di accesso all'integrazione (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f3d774c474c27896c16bba5c7552713f248519aa86ef56da0da5b704234b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870111"
---
# <a name="enlistment-access-masks"></a>Maschere di accesso all'integrazione

KTM definisce le maschere di accesso all'integrazione seguenti da usare quando si aprono le integrazioni.

<dl> <dt>

<span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**INFORMAZIONI SULLE \_ QUERY DI \_ INTEGRAZIONE**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



Il chiamante può eseguire una query KTM per informazioni sull'integrazione.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**INFORMAZIONI SUL \_ SET DI \_ INTEGRAZIONE**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



Il chiamante può impostare informazioni sull'integrazione.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**RIPRISTINO \_ DELL'INTEGRAZIONE**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



Il chiamante può recuperare un'integrazione.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**DIRITTI \_ SUBORDINATI DI \_ INTEGRAZIONE**
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

<span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**DIRITTI SUPERIORI \_ DI \_ INTEGRAZIONE**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



Il chiamante può integrarsi nella transazione come gestore delle transazioni superiore.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**LETTURA \_ GENERICA \_ DELL'INTEGRAZIONE**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



Il chiamante ha i privilegi seguenti: **STANDARD \_ RIGHTS READ \_ e** **ENLISTMENT QUERY \_ \_ INFORMATION**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**SCRITTURA \_ GENERICA DI \_ INTEGRAZIONE**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



Il chiamante ha i privilegi seguenti: **STANDARD \_ RIGHTS \_ WRITE,** **ENLISTMENT SET \_ \_ INFORMATION** e **ENLISTMENT \_ RECOVER.**


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**ESECUZIONE \_ GENERICA \_ DELL'INTEGRAZIONE**
</dt> <dd> <dl> <dt>

0x2001C
</dt> <dt>



Il chiamante ha i privilegi seguenti: **STANDARD \_ RIGHTS \_ EXECUTE,** **ENLISTMENT \_ RECOVER** e **ENLISTMENT \_ SUBORDINATE \_ RIGHTS**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**INTEGRAZIONE DI \_ TUTTI \_ GLI ACCESSI**
</dt> <dd> <dl> <dt>

0xF001F
</dt> <dt>



Questo valore imposta tutti i bit validi per un valore di accesso all'integrazione.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                           |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




