---
title: Valori della sintassi dell'applicazione SNMP (SNMP. h)
description: I valori della sintassi dell'applicazione SNMP vengono utilizzati dalle applicazioni di gestione che utilizzano l'API di gestione SNMP Microsoft.
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
ms.openlocfilehash: d79ab6535c97fe4124aa1cb3f7ca11ce3eb02582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119530"
---
# <a name="snmp-application-syntax-values"></a>Valori della sintassi dell'applicazione SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

I valori della sintassi dell'applicazione SNMP vengono utilizzati dalle applicazioni di gestione che utilizzano l'API di gestione SNMP Microsoft.



| Costante                                                                                                                                                                                  | Descrizione                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <dt>**\_indirizzo IP ASN**</dt> </dl>                             | Indica una variabile dell'indirizzo IP.<br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <dt>**\_COUNTER32 ASN**</dt> </dl>                             | Indica una variabile contatore.<br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <dt>**\_GAUGE32 ASN**</dt> </dl>                                   | Indica una variabile del misuratore. Questa variabile descrive un tipo Unsigned32 in conformità con RFC 1902.<br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <dt>**\_TimeTicks ASN**</dt> </dl>                             | Indica una variabile TimeTicks.<br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <dt>**ASN \_ opaco**</dt> </dl>                                      | Indica una variabile opaca.<br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <dt>**\_COUNTER64 ASN**</dt> </dl>                             | Indica una variabile contatore che aumenta fino a quando non raggiunge un valore massimo di (2 ^ 64)-1.<br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <dt>**\_UINTEGER32 ASN**</dt> </dl>                          | Indica una variabile di Unsigned Integer a 32 bit. Questa variabile descrive un tipo UInteger32 in conformità con RFC 1442.<br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <dt>**\_UNSIGNED32 RFC2578 \_ ASN**</dt> </dl> | Vedere ASN \_ GAUGE32.<br/>                                                                                                     |



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

 

