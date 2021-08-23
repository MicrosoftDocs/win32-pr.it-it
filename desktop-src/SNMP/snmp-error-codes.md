---
title: Codici di errore SNMP (Snmp.h)
description: Microsoft implementa i codici di errore SNMP seguenti definiti dalla specifica SNMPv2C.
ms.assetid: 7e7e2bc0-a058-4853-b736-1946e64a0c4a
topic_type:
- apiref
api_name:
- SNMP_ERRORSTATUS_NOERROR
- SNMP_ERRORSTATUS_TOOBIG
- SNMP_ERRORSTATUS_NOSUCHNAME
- SNMP_ERRORSTATUS_BADVALUE
- SNMP_ERRORSTATUS_READONLY
- SNMP_ERRORSTATUS_GENERR
- SNMP_ERRORSTATUS_NOACCESS
- SNMP_ERRORSTATUS_WRONGTYPE
- SNMP_ERRORSTATUS_WRONGLENGTH
- SNMP_ERRORSTATUS_WRONGENCODING
- SNMP_ERRORSTATUS_WRONGVALUE
- SNMP_ERRORSTATUS_NOCREATION
- SNMP_ERRORSTATUS_INCONSISTENTVALUE
- SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE
- SNMP_ERRORSTATUS_COMMITFAILED
- SNMP_ERRORSTATUS_UNDOFAILED
- SNMP_ERRORSTATUS_AUTHORIZATIONERROR
- SNMP_ERRORSTATUS_NOTWRITABLE
- SNMP_ERRORSTATUS_INCONSISTENTNAME
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583394dfc3093f4f0d5cf3d7c7cef68d7ff6d57930e3abf957d857defec227c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008929"
---
# <a name="snmp-error-codes"></a>Codici di errore SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

Microsoft implementa i codici di errore SNMP seguenti definiti dalla specifica SNMPv2C.



| Costante/valore                                                                                                                                                                                                                                                                              | Descrizione                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_ERRORSTATUS_NOERROR"></span><span id="snmp_errorstatus_noerror"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOERROR**</dt> <dt>0</dt> </dl>                                      | L'agente segnala che non si sono verificati errori durante la trasmissione.<br/>                                                                                      |
| <span id="SNMP_ERRORSTATUS_TOOBIG"></span><span id="snmp_errorstatus_toobig"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ TOOBIG**</dt> <dt>1</dt> </dl>                                         | L'agente non è stato in grado di inserire i risultati dell'operazione SNMP richiesta in un singolo messaggio SNMP.<br/>                                                     |
| <span id="SNMP_ERRORSTATUS_NOSUCHNAME"></span><span id="snmp_errorstatus_nosuchname"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOSUCHNAME**</dt> <dt>2</dt> </dl>                             | L'operazione SNMP richiesta ha identificato una variabile sconosciuta.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_BADVALUE"></span><span id="snmp_errorstatus_badvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ BADVALUE**</dt> <dt>3</dt> </dl>                                   | L'operazione SNMP richiesta ha tentato di modificare una variabile, ma ha specificato un errore di sintassi o di valore.<br/>                                            |
| <span id="SNMP_ERRORSTATUS_READONLY"></span><span id="snmp_errorstatus_readonly"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ READONLY**</dt> <dt>4</dt> </dl>                                   | L'operazione SNMP richiesta ha tentato di modificare una variabile che non era consentita per la modifica, in base al profilo della community della variabile.<br/>         |
| <span id="SNMP_ERRORSTATUS_GENERR"></span><span id="snmp_errorstatus_generr"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ GENERR**</dt> <dt>5</dt> </dl>                                         | Si è verificato un errore diverso da uno di quelli elencati di seguito durante l'operazione SNMP richiesta.<br/>                                                          |
| <span id="SNMP_ERRORSTATUS_NOACCESS"></span><span id="snmp_errorstatus_noaccess"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOACCESS**</dt> <dt>6</dt> </dl>                                   | La variabile SNMP specificata non è accessibile.<br/>                                                                                                      |
| <span id="SNMP_ERRORSTATUS_WRONGTYPE"></span><span id="snmp_errorstatus_wrongtype"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGTYPE**</dt> <dt>7</dt> </dl>                                | Il valore specifica un tipo incoerente con il tipo richiesto per la variabile.<br/>                                                            |
| <span id="SNMP_ERRORSTATUS_WRONGLENGTH"></span><span id="snmp_errorstatus_wronglength"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGLENGTH**</dt> <dt>8</dt> </dl>                          | Il valore specifica una lunghezza incoerente con la lunghezza richiesta per la variabile.<br/>                                                        |
| <span id="SNMP_ERRORSTATUS_WRONGENCODING"></span><span id="snmp_errorstatus_wrongencoding"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGENCODING**</dt> <dt>9</dt> </dl>                    | Il valore contiene una codifica ASN.1 (Abstract Syntax Notation One) incoerente con il tag ASN.1 del campo.<br/>                           |
| <span id="SNMP_ERRORSTATUS_WRONGVALUE"></span><span id="snmp_errorstatus_wrongvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGVALUE**</dt> <dt>10</dt> </dl>                            | Il valore non può essere assegnato alla variabile.<br/>                                                                                                       |
| <span id="SNMP_ERRORSTATUS_NOCREATION"></span><span id="snmp_errorstatus_nocreation"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOCREATION**</dt> <dt>11</dt> </dl>                            | La variabile non esiste e l'agente non può crearla.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTVALUE"></span><span id="snmp_errorstatus_inconsistentvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ INCONSISTENTVALUE**</dt> <dt>12</dt> </dl>       | Il valore non è coerente con i valori di altri oggetti gestiti.<br/>                                                                                     |
| <span id="SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE"></span><span id="snmp_errorstatus_resourceunavailable"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ RESOURCEUNAVAILABLE**</dt> <dt>13</dt> </dl> | L'assegnazione del valore alla variabile richiede l'allocazione delle risorse attualmente non disponibili.<br/>                                                |
| <span id="SNMP_ERRORSTATUS_COMMITFAILED"></span><span id="snmp_errorstatus_commitfailed"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ COMMITFAILED**</dt> <dt>14</dt> </dl>                      | Non si sono verificati errori di convalida, ma non sono state aggiornate variabili.<br/>                                                                                       |
| <span id="SNMP_ERRORSTATUS_UNDOFAILED"></span><span id="snmp_errorstatus_undofailed"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ UNDOFAILED**</dt> <dt>15</dt> </dl>                            | Non si sono verificati errori di convalida. Alcune variabili sono state aggiornate perché non è stato possibile annullare l'assegnazione.<br/>                                    |
| <span id="SNMP_ERRORSTATUS_AUTHORIZATIONERROR"></span><span id="snmp_errorstatus_authorizationerror"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ AUTHORIZATIONERROR**</dt> <dt>16</dt> </dl>    | Si è verificato un errore di autorizzazione.<br/>                                                                                                                    |
| <span id="SNMP_ERRORSTATUS_NOTWRITABLE"></span><span id="snmp_errorstatus_notwritable"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOTWRITABLE**</dt> <dt>17</dt> </dl>                         | La variabile esiste ma l'agente non può modificarla.<br/>                                                                                                 |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTNAME"></span><span id="snmp_errorstatus_inconsistentname"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ INCONSISTENTNAME**</dt> <dt>18</dt> </dl>          | La variabile non esiste. L'agente non può crearlo perché l'istanza dell'oggetto denominata non è coerente con i valori di altri oggetti gestiti.<br/> |



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
</dt> </dl>

 

