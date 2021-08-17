---
title: Tipi di richiesta SNMP (Snmp.h)
description: I tipi di richiesta SNMP vengono usati per descrivere l'operazione che il servizio SNMP richiede all'agente di estensione di eseguire.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c4dfdfc6d65e63b8cd00956627eef9e831c46c6979e44634067b1e29defc4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142994"
---
# <a name="snmp-request-types"></a>Tipi di richiesta SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

I tipi di richiesta SNMP vengono usati per descrivere l'operazione che il servizio SNMP richiede all'agente di estensione di eseguire.



| Costante/valore                                                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <dt>**SNMP \_ ESTENSIONE \_ GET**</dt> <dt>SNMP \_ PDU \_ GET</dt> </dl>                       | Recupera il valore dei valori delle variabili specificate.<br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <dt>**SNMP \_ ESTENSIONE \_ GET \_ NEXT**</dt> <dt>SNMP \_ PDU \_ GETNEXT</dt> </dl>   | Recuperare il valore o i valori del successore lessicografico delle variabili specificate.<br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <dt>**SNMP \_ ESTENSIONE \_ GET \_ BULK**</dt> <dt>SNMP \_ PDU \_ GETBULK</dt> </dl>   | Cercare e recuperare più valori con una singola richiesta.<br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <dt>**TEST DEL \_ SET DI \_ ESTENSIONI SNMP \_**</dt> </dl>                                                                           | Convalidare i valori delle variabili specificate. Questa operazione ottimizza la probabilità che un'operazione di scrittura sia riuscita durante la richiesta COMMIT. Per altre informazioni, vedere la [**funzione SnmpExtensionQueryEx.**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex)<br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <dt>**SNMP \_ SET \_ \_ DI**</dt> PDU SNMP COMMIT DEL <dt>SET DI COMMIT \_ \_ DELL'ESTENSIONE</dt> </dl> | Scrivere i nuovi valori nelle variabili specificate.<br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <dt>**ANNULLAMENTO SET \_ DI \_ ESTENSIONI SNMP \_**</dt> </dl>                                                                           | Reimpostare i valori delle variabili specificate sui relativi valori prima della richiesta COMMIT.<br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <dt>**PULIZIA SET \_ DI \_ ESTENSIONI SNMP \_**</dt> </dl>                                                                  | Rilasciare le risorse allocate nelle richieste e nelle operazioni precedenti.<br/>                                                                                                                                                                             |



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

 

