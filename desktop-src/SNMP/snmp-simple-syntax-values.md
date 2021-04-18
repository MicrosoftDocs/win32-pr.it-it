---
title: Valori di sintassi semplici SNMP (SNMP. h)
description: I valori della sintassi semplice SNMP vengono utilizzati per indicare un tipo di variabile SNMP.
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120234"
---
# <a name="snmp-simple-syntax-values"></a>Valori di sintassi semplici SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

I valori della sintassi semplice SNMP vengono utilizzati per indicare un tipo di variabile SNMP.



| Costante                                                                                                                                                                           | Descrizione                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <dt>**\_intero ASN**</dt> </dl>                            | Indica una variabile di tipo integer con segno a 32 bit.<br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <dt>**\_bit ASN**</dt> </dl>                                     | Indica una variabile che è un'enumerazione di bit denominati.<br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <dt>**\_OCTETSTRING ASN**</dt> </dl>                | Indica una variabile di stringa ottetto.<br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <dt>**ASN \_ null**</dt> </dl>                                     | Indica un valore **null** .<br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <dt>**\_OBJECTIDENTIFIER ASN**</dt> </dl> | Indica una variabile dell'identificatore di oggetto.<br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <dt>**\_INTEGER32 ASN**</dt> </dl>                      | Indica un valore intero con segno a 32 bit.<br/>                   |



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

 

