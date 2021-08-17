---
description: La clausola OBJECTS della macro NOTIFICATION-TYPE enumera il set di oggetti associati all'oggetto notifica.
ms.assetid: 0cb4776f-aae2-452d-9472-caf6d28fb870
ms.tgt_platform: multiple
title: Clausola OBJECTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9289be0a3fa228e74a720ec385a5b13354f849710a88287a9911f470e40758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131043"
---
# <a name="objects-clause"></a>Clausola OBJECTS

La clausola OBJECTS della macro [NOTIFICATION-TYPE](notification-type-macro.md) enumera il set di oggetti associati all'oggetto notifica.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

Quando si esegue il mapping alle classi CIM, si applicano le regole seguenti:

-   Ogni membro della clausola OBJECTS esegue il mapping a una proprietà della definizione della classe CIM. Il descrittore di oggetto del membro esegue il mapping verbatim al nome della proprietà CIM. Ad esempio, **ifIndex** converte in **ifIndex**.
-   Ogni proprietà CIM generata dal processo di mapping contiene il **qualificatore VarBindIndex.**

    **VarBindIndex** è un qualificatore **uint32** obbligatorio che descrive la posizione dell'oggetto come viene visualizzato nella clausola OBJECTS della macro [TRAP-TYPE](trap-type-macro.md) o [NOTIFICATION-TYPE.](notification-type-macro.md) Il numero intero specifica anche la posizione della proprietà così come viene visualizzata rispettivamente nell'elenco delle associazioni di variabili della PDU TRAP SNMPv1 o SNMPv2C (unità dati del protocollo). Poiché le prime due associazioni di variabili sono sempre TimeStamp e Identification, eventuali variabili aggiuntive vengono numerate dopo il valore 2.

    Quando la classe di evento CIM viene generata da una macro [TRAP-TYPE](trap-type-macro.md) SNMPv1, il qualificatore **VarBindIndex** ha un valore iniziale pari a 1 per la prima variabile nell'elenco di associazioni di variabili.

    Quando la classe di evento CIM viene generata da una macro SNMPv2C [NOTIFICATION-TYPE,](notification-type-macro.md) il qualificatore **VarBindIndex** ha un valore iniziale di 3 per la prima variabile nell'elenco di associazioni di variabili.

Quando si esegue il mapping di una classe CIM incapsulata, ogni membro della clausola OBJECTS esegue il mapping a una proprietà CIM che riflette il nome, il tipo e il valore dell'oggetto MIB corrispondente. Le procedure di mapping utilizzate sono specificate negli argomenti seguenti:

-   [Clausola SYNTAX](syntax-clause.md)
-   [TEXTUAL-CONVENTION Macro](textual-convention-macro.md)
-   [Clausole ACCESS e MAX-ACCESS](access-and-max-access-clauses.md)

Quando si usa una classe CIM referenziato, ogni membro della clausola OBJECTS esegue il mapping come segue:

-   Ogni membro della clausola OBJECTS esegue il mapping a una singola proprietà della classe CIM. La proprietà è fortemente tipizzato come oggetto incorporato.
-   La classe dell'oggetto incorporato viene generata tramite la procedura standard di mapping degli oggetti. Per altre informazioni, vedere [Object-TYPE Macro](object-type-macro.md). Ad esempio, **ifTable esegue** il mapping a una classe incorporata denominata **SNMP \_ RFC1213 \_ MIB \_ ifTable**.
-   I valori associati alle associazioni di variabili di una PDU TRAP vengono creati come oggetti incorporati di un oggetto della classe referente. Ogni oggetto incorporato contiene valori per ognuna delle proprietà con chiave dell'oggetto e il valore della proprietà nell'associazione di variabili di cui viene eseguito il mapping.

 

 



