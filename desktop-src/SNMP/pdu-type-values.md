---
title: Valori di tipo PDU (Snmp.h)
description: I valori del tipo PDU vengono usati nel campo tipo pdu \_ della PDU per descriverne il tipo.
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
ms.openlocfilehash: b2e9346c313efccda6d3635da51919f52fae37dd901cc73cf1f119bffdf9c22c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009209"
---
# <a name="pdu-type-values"></a>Valori di tipo PDU

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

I valori del tipo PDU vengono usati nel campo **tipo pdu \_** della PDU per descriverne il tipo.



| Costante                                                                                                                                                                   | Descrizione                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <dt>**SNMP \_ PDU \_ GET**</dt> </dl>                | Cercare e recuperare un valore da una variabile SNMP specificata.<br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <dt>**SNMP \_ PDU \_ GETNEXT**</dt> </dl>    | Cercare e recuperare il valore di una variabile SNMP senza conoscere il nome esatto della variabile.<br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <dt>**RISPOSTA \_ PDU \_ SNMP**</dt> </dl> | Rispondere a una richiesta SNMP \_ PDU \_ GET o SNMP \_ PDU \_ GETNEXT.<br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <dt>**SNMP \_ PDU \_ SET**</dt> </dl>                | Archiviare un valore in una variabile SNMP specificata.<br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <dt>**SNMP \_ PDU \_ V1TRAP**</dt> </dl>       | Indica che la trap PDU è formattata in modo da essere conforme allo standard SNMPv1.<br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <dt>**SNMP \_ PDU \_ GETBULK**</dt> </dl>    | Cercare e recuperare più valori con una singola richiesta.<br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <dt>**SNMP \_ PDU \_ INFORM**</dt> </dl>       | Indica una PDU di richiesta di informazioni.<br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <dt>**SNMP \_ PDU \_ TRAP**</dt> </dl>             | Avvisa il sistema di gestione di un evento straordinario in SNMPv2C.<br/>                             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Snmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del protocollo Simple Network Management Protocol (SNMP)](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Informazioni di riferimento su SNMP](snmp-reference.md)
</dt> <dt>

[Costanti SNMP](snmp-constants.md)
</dt> </dl>

 

