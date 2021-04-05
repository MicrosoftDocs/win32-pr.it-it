---
title: Tipi trap SNMPv1 (SNMP. h)
description: I tipi trap SNMPv1 descrivono un set predefinito di tipi trap generici formattati in modo da essere conformi allo standard SNMPv1 Trap PDU.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874554"
---
# <a name="snmpv1-trap-types"></a>Tipi trap SNMPv1

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

I tipi trap SNMPv1 descrivono un set predefinito di tipi trap generici formattati in modo da essere conformi allo standard SNMPv1 Trap PDU.



| Costante                                                                                                                                                                                                          | Descrizione                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ COLDSTART**</dt> </dl>             | Indica una trap di avvio a freddo. L'agente sta inizializzando le entità di protocollo in modalità gestita. Potrebbe modificare gli oggetti nella relativa visualizzazione.<br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ WARMSTART**</dt> </dl>             | Indica una trap di avvio a caldo. L'agente viene reinizializzato, ma non modifica gli oggetti nella visualizzazione.<br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ LINKDOWN**</dt> </dl>                | Indica un trap di collegamento. Un'interfaccia collegata è cambiata dallo stato attivo allo stato di inattività. La prima variabile nell'elenco delle associazioni variabili identifica l'interfaccia.<br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ LINKUP**</dt> </dl>                      | Indica una trap di collegamento. Un'interfaccia collegata è cambiata dall'inizio fino allo stato attivo. La prima variabile nell'elenco delle associazioni variabili identifica l'interfaccia.<br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ AUTHFAILURE**</dt> </dl>       | Indica una trap di errore di autenticazione. Un messaggio SNMP è stato inviato da un'entità SNMP, ma è stato erroneamente richiesto di appartenere a una community nota.<br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ EGPNEIGHLOSS**</dt> </dl>    | Indica un trap di perdita Neighbor EGP. Un peer EGP è stato modificato in stato di inattività. La prima variabile nell'elenco Binding variabili identifica l'indirizzo IP del peer EGP.<br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ ENTERSPECIFIC**</dt> </dl> | Indica una trap specifica dell'organizzazione. Si è verificato un evento straordinario. Viene identificato nel parametro *specificTrap* con un valore specifico dell'organizzazione.<br/>               |



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

 

