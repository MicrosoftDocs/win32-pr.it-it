---
title: '\_Costanti di errore del certificato EAP (Eaphosterror. h)'
description: Definire gli errori correlati ai certificati comuni a tutte le tecnologie API EAPHost.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517517"
---
# <a name="eap_cert-error-constants"></a>\_Costanti di errore del certificato EAP

Queste costanti definiscono gli errori correlati ai certificati comuni a tutte le tecnologie API EAPHost.

<dl> <dt>

<span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_\_certificato EAP \_ prima**
</dt> <dd> <dl> <dt>

0x0
</dt> <dt>



Definisce il limite dei report di errore. si verificherà un errore di certificato tra i certificati **\_ EAP \_ \_ prima** e il certificato **\_ EAP per \_ \_ ultimo**.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_\_ultimo certificato \_ EAP**
</dt> <dd> <dl> <dt>

0xF
</dt> <dt>



Definisce il limite dei report di errore. si verificherà un errore di certificato tra i certificati **\_ EAP \_ \_ prima** e il certificato **\_ EAP per \_ \_ ultimo**.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_certificato EAP \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Non è stato trovato alcun certificato utente.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_\_certificato EAP \_ non valido**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Il certificato utente non è valido.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_\_certificato EAP \_ scaduto**
</dt> <dd> <dl> <dt>

0x3
</dt> <dt>



Il certificato utente è scaduto.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_\_certificato EAP \_ revocato**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Il certificato utente è stato revocato.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_\_ \_ altro errore del certificato EAP \_**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Errore sconosciuto relativo al certificato.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_\_certificato EAP \_ rifiutato**
</dt> <dd> <dl> <dt>

0x6
</dt> <dt>



Il certificato utente è stato rifiutato.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_il \_ nome del certificato EAP è \_ \_ obbligatorio**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



Il certificato utente richiede un nome.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_\_prima EAP generale \_**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Definisce il limite dei report di errore. qualsiasi errore EAP generale si verificherà tra il **\_ \_ \_ primo** e **\_ \_ \_ l'ultimo** generale EAP.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_\_ultimo generale \_ EAP**
</dt> <dd> <dl> <dt>

0x3F
</dt> <dt>



Definisce il limite dei report di errore. qualsiasi errore EAP generale si verificherà tra il **\_ \_ \_ primo** e **\_ \_ \_ l'ultimo** generale EAP.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Eaphosterror. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti EAPHost comuni](common-eap-host-error-constants.md)
</dt> </dl>

 

 





