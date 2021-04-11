---
description: Di seguito vengono illustrate le costanti di sicurezza WMI utilizzate per gli eventi. Vengono usati per impostare le voci di controllo di accesso (ACE) nei descrittori di sicurezza usati per eventi o sink.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Costanti di sicurezza degli eventi (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3009b16e468a647ee96b9be365286caba2c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131155"
---
# <a name="event-security-constants"></a>Costanti di sicurezza degli eventi

Di seguito vengono illustrate le costanti di sicurezza WMI utilizzate per gli eventi. Vengono usati per impostare le voci di controllo di accesso (ACE) nei descrittori di sicurezza usati per eventi o sink.

<dl> <dt>

<span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**\_pubblicazione con diritto WBEM \_**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Specifica che l'account può pubblicare eventi nell'istanza di [**\_ \_ EventFilter**](--eventfilter.md) che definisce il filtro eventi per un consumer permanente. Disponibile in wbemcli. h.


</dt> </dl> </dd> <dt>

<span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**\_sottoscrizione a destra di WBEM \_**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Specifica che un consumer può sottoscrivere gli eventi recapitati a un sink. Usato in [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity). Disponibile in wbemcli. h.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ S \_ soggetto \_ a \_ SDS**
</dt> <dd> <dl> <dt>

274435 (0x43003)
</dt> <dt>



Il provider di eventi indica che WMI controlla la proprietà del **\_ descrittore di sicurezza** in ogni evento (ereditato dall' [**\_ \_ evento**](--event.md)) e invia solo gli eventi agli utenti con le autorizzazioni di accesso appropriate. Disponibile in wbemprov. h.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                         |
| Intestazione<br/>                   | <dl> <dt>Wbemcli. h; </dt> <dt>Wbemprov. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> <dt>

[Protezione degli eventi WMI](securing-wmi-events.md)
</dt> </dl>

 

 




