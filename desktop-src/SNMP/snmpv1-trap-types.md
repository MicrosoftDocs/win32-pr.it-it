---
title: Tipi di trap SNMPv1 (Snmp.h)
description: I tipi di trap SNMPv1 descrivono un set predefinito di tipi di trap generici formattati per la conformità con lo standard PDU trap SNMPv1.
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
ms.openlocfilehash: 7067a6bf5aa1ea11135279484cb74722b8bcc197b507f6bba9b30e35630a2861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886241"
---
# <a name="snmpv1-trap-types"></a>Tipi di trap SNMPv1

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

I tipi di trap SNMPv1 descrivono un set predefinito di tipi di trap generici formattati per la conformità con lo standard PDU trap SNMPv1.



| Costante                                                                                                                                                                                                          | Descrizione                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ COLDSTART**</dt> </dl>             | Indica una trap di avvio a freddo. L'agente sta inizializzando le entità di protocollo in modalità gestita. Può modificare gli oggetti nella relativa visualizzazione.<br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ WARMSTART**</dt> </dl>             | Indica una trap di avvio a caldo. L'agente sta reinizializzando se stesso, ma non modifica gli oggetti nella visualizzazione.<br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ LINKDOWN**</dt> </dl>                | Indica una trap di collegamento. Un'interfaccia collegata è stata modificata dallo stato verso l'alto verso il basso. La prima variabile nell'elenco di associazioni di variabili identifica l'interfaccia.<br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <dt>**COLLEGAMENTO SNMP \_ GENERICTRAP \_**</dt> </dl>                      | Indica una trap di collegamento. Un'interfaccia collegata è stata modificata dall'inizio verso il basso allo stato attivo. La prima variabile nell'elenco di associazioni di variabili identifica l'interfaccia.<br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ AUTHFAILURE**</dt> </dl>       | Indica una trap di errore di autenticazione. Un'entità SNMP ha inviato un messaggio SNMP, ma ha falsamente dichiarato di appartenere a una community nota.<br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ EGPNEIGHLOSS**</dt> </dl>    | Indica una trap di perdita del router adiacente EGP. Un peer EGP è stato modificato nello stato down. La prima variabile nell'elenco delle associazioni di variabili identifica l'indirizzo IP del peer EGP.<br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ ENTERSPECIFIC**</dt> </dl> | Indica una trap specifica dell'organizzazione. Si è verificato un evento straordinario. Viene identificato nel parametro *specificTrap* con un valore specifico dell'organizzazione.<br/>               |



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

 

