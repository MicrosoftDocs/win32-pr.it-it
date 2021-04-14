---
title: Valori di tipo PDU (SNMP. h)
description: I valori di tipo PDU vengono usati nel \_ campo tipo PDU della PDU per descrivere il tipo.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478431"
---
# <a name="pdu-type-values"></a>Valori di tipo PDU

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

I valori di tipo PDU vengono usati nel **campo \_ tipo PDU** della PDU per descrivere il tipo.



| Costante                                                                                                                                                                   | Descrizione                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <dt>**\_Get SNMP PDU \_**</dt> </dl>                | Ricerca e recupero di un valore da una variabile SNMP specificata.<br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <dt>**datanext di SNMP \_ PDU \_**</dt> </dl>    | Cercare e recuperare il valore di una variabile SNMP senza conoscere il nome esatto della variabile.<br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <dt>**\_risposta PDU \_ SNMP**</dt> </dl> | Rispondere a una \_ richiesta SNMP PDU \_ Get o a un'istanza di SNMP \_ PDU \_ GetNext.<br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <dt>**\_set PDU \_ SNMP**</dt> </dl>                | Archivia un valore in una variabile SNMP specificata.<br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <dt>**\_V1TRAP PDU \_ SNMP**</dt> </dl>       | Indica che il Trap PDU è formattato in modo da essere conforme allo standard SNMPv1.<br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <dt>**SNMP \_ PDU \_ GetBulk**</dt> </dl>    | Eseguire ricerche e recuperare più valori con una singola richiesta.<br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <dt>**informazioni su SNMP \_ PDU \_**</dt> </dl>       | Indica una PDU di richiesta di informazioni.<br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <dt>**\_trap SNMP PDU \_**</dt> </dl>             | Segnala al sistema di gestione un evento straordinario in SNMPv2C.<br/>                             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>SNMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del protocollo Simple Network Management Protocol (SNMP)](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Riferimento SNMP](snmp-reference.md)
</dt> <dt>

[Costanti SNMP](snmp-constants.md)
</dt> </dl>

 

