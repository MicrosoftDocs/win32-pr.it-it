---
title: Tipi di richiesta SNMP (SNMP. h)
description: I tipi di richiesta SNMP vengono utilizzati per descrivere l'operazione che il servizio SNMP sta richiedendo all'agente di estensione di eseguire.
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
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478430"
---
# <a name="snmp-request-types"></a>Tipi di richiesta SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

I tipi di richiesta SNMP vengono utilizzati per descrivere l'operazione che il servizio SNMP sta richiedendo all'agente di estensione di eseguire.



| Costante/valore                                                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <dt>**SNMP \_ ESTENSIONE \_ Get**</dt> <dt>SNMP \_ PDU \_ Get</dt> </dl>                       | Recuperare il valore dei valori delle variabili specificate.<br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <dt>**SNMP \_ ESTENSIONE \_ get \_ Next**</dt> <dt>SNMP \_ PDU \_ GetNext</dt> </dl>   | Recuperare il valore o i valori del successore lessicografico delle variabili specificate.<br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <dt>**SNMP \_ ESTENSIONE \_ get \_ bulk**</dt> <dt>SNMP \_ PDU \_ GetBulk</dt> </dl>   | Eseguire ricerche e recuperare più valori con una singola richiesta.<br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <dt>**\_test del \_ set di estensioni SNMP \_**</dt> </dl>                                                                           | Convalidare i valori delle variabili specificate. Questa operazione ottimizza la probabilità di un'operazione di scrittura riuscita durante la richiesta di COMMIT. Per ulteriori informazioni, vedere la funzione [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .<br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <dt>**SNMP \_ set di estensioni di \_ \_ commit**</dt> SNMP del set di estensioni <dt> \_ \_</dt> </dl> | Scrive i nuovi valori nelle variabili specificate.<br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <dt>**\_ \_ Annulla set di estensioni SNMP \_**</dt> </dl>                                                                           | Reimpostare i valori delle variabili specificate sui rispettivi valori prima della richiesta di COMMIT.<br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <dt>**\_pulizia del \_ set di estensioni SNMP \_**</dt> </dl>                                                                  | Rilascia le risorse allocate nelle richieste e nelle operazioni precedenti.<br/>                                                                                                                                                                             |



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

 

