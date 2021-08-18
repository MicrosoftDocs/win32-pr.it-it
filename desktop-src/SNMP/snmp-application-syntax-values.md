---
title: Valori della sintassi dell'applicazione SNMP (Snmp.h)
description: I valori di sintassi dell'applicazione SNMP vengono usati dalle applicazioni di gestione che utilizzano microsoft SNMP API Gestione.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787723780d5920aafc3c37c40ea995a675943d1e45873d5f30cd8cebb77b5b64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009029"
---
# <a name="snmp-application-syntax-values"></a>Valori della sintassi dell'applicazione SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

I valori di sintassi dell'applicazione SNMP vengono usati dalle applicazioni di gestione che utilizzano microsoft SNMP API Gestione.



| Costante                                                                                                                                                                                  | Descrizione                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <dt>**INDIRIZZO \_ IP ASN**</dt> </dl>                             | Indica una variabile di indirizzo IP.<br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <dt>**CONTATORE \_ ASN32**</dt> </dl>                             | Indica una variabile contatore.<br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <dt>**MISURATORE \_ ASN32**</dt> </dl>                                   | Indica una variabile del misuratore. Questa variabile descrive un tipo Unsigned32 conforme a RFC 1902.<br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <dt>**ASN \_ TIMETICKS**</dt> </dl>                             | Indica una variabile timeticks.<br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <dt>**ASN \_ OPAQUE**</dt> </dl>                                      | Indica una variabile opaca.<br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <dt>**CONTATORE \_ ASN64**</dt> </dl>                             | Indica una variabile contatore che aumenta fino a raggiungere il valore massimo (2^64) - 1.<br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <dt>**ASN \_ UINTEGER32**</dt> </dl>                          | Indica una variabile integer senza segno a 32 bit. Questa variabile descrive un tipo UInteger32 conforme a RFC 1442.<br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <dt>**ASN \_ RFC2578 \_ UNSIGNED32**</dt> </dl> | Vedere ASN \_ GAUGE32.<br/>                                                                                                     |



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

 

