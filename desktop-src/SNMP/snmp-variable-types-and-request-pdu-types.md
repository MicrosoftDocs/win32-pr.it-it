---
title: Tipi di variabili SNMP e tipi PDU di richiesta
description: Le definizioni per alcuni tipi di variabile SNMP e i tipi di richiesta PDU sono state modificate. Il file SNMP. h esegue il mapping dei tipi obsoleti ai nuovi tipi corrispondenti.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728954"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a>Tipi di variabili SNMP e tipi PDU di richiesta

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

Le definizioni per alcuni tipi di variabile SNMP e i tipi di richiesta PDU sono state modificate. Il file SNMP. h esegue il mapping dei tipi obsoleti ai nuovi tipi corrispondenti.

## <a name="modified-snmp-variable-types"></a>Tipi di variabili SNMP modificate

Quando si sviluppano applicazioni di gestione che usano l'API di gestione SNMP Microsoft, è consigliabile usare i nuovi tipi di variabili SNMP elencati nella tabella seguente. La tabella elenca i tipi di variabili SNMP obsoleti con i nuovi tipi di variabile corrispondenti.

| Tipo di variabile precedente        | Nuovo tipo di variabile |
|--------------------------|-------------------|
| \_IPAddress RFC1155 \_ ASN  | \_indirizzo IP ASN    |
| \_Contatore RFC1155 \_ ASN    | \_COUNTER32 ASN    |
| \_ \_ Misuratore RFC1155 ASN      | \_GAUGE32 ASN      |
| \_TimeTicks RFC1155 \_ ASN  | \_TimeTicks ASN    |
| \_Opaco RFC1155 \_ ASN     | ASN \_ opaco       |
| \_DISPSTRING RFC1213 \_ ASN | \_OCTETSTRING ASN  |



 

## <a name="modified-snmp-pdu-request-types"></a>Tipi di richiesta PDU SNMP modificati

Quando si sviluppano applicazioni di gestione che usano l'API di gestione SNMP Microsoft, è necessario usare i nuovi tipi di PDU SNMP elencati nella tabella seguente. La tabella elenca i vecchi tipi di PDU SNMP con i nuovi tipi PDU corrispondenti.

| Tipo PDU precedente                 | Nuovo tipo PDU        |
|------------------------------|---------------------|
| \_GetRequest RFC1157 ASN \_     | \_Get SNMP PDU \_      |
| \_GETNEXTREQUEST RFC1157 \_ ASN | datanext di SNMP \_ PDU \_  |
| \_GetResponse RFC1157 ASN \_    | \_risposta PDU \_ SNMP |
| \_Richiesta RFC1157 \_ ASN     | \_set PDU \_ SNMP      |
| \_Trap RFC1157 \_ ASN           | \_V1TRAP PDU \_ SNMP   |



 

 

 