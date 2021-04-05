---
title: Utilizzo degli elenchi di associazioni variabili
description: Un'associazione variabile è l'associazione di un nome di istanza dell'oggetto SNMP a un valore associato. Un elenco di associazioni variabili è una serie di voci di associazione variabili. In WinSNMP, un'unità dati del protocollo (PDU) include un elenco di associazioni variabili.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Utilizzo degli elenchi di associazione variabili SNMP
- Binding di variabili che elenca SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723663"
---
# <a name="working-with-variable-binding-lists"></a>Utilizzo degli elenchi di associazioni variabili

Un' *associazione variabile* è l'associazione di un nome di istanza dell'oggetto SNMP a un valore associato. Un *elenco di associazioni variabili* è una serie di voci di associazione variabili. In WinSNMP, un'unità dati del protocollo (PDU) include un elenco di associazioni variabili.

I dettagli della struttura dell'elenco di associazioni variabili sono limitati all'implementazione di Microsoft WinSNMP. Un'applicazione WinSNMP può accedere a un elenco di associazioni variabili con un handle di tipo **HSNMP \_ VBL**. Per altre informazioni, vedere [oggetti handle di risorsa](resource-handle-objects.md).

L'applicazione WinSNMP può creare e modificare elenchi di associazioni variabili e includerli in PDU. Per eseguire queste operazioni, l'applicazione usa le [funzioni di associazione della variabile](winsnmp-functions.md)WinSNMP. Per ulteriori informazioni sull'utilizzo di WinSNMP e degli elenchi di associazioni variabili, vedere gli argomenti elencati nella tabella seguente.



| Argomento                                                                    | Descrizione                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [Creazione di un elenco di associazioni variabili](creating-a-variable-binding-list.md) | Viene descritto come creare un elenco di associazioni variabili. |
| [Gestione di un elenco di associazioni variabili](managing-a-variable-binding-list.md) | Viene descritto come gestire un elenco di associazioni variabili. |



 

Per ulteriori informazioni sulle associazioni variabili e sugli elenchi di associazioni variabili, vedere [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "operazioni di protocollo per la versione 2 del Simple Network Management Protocol (SNMPv2)," e le [funzioni di associazione delle variabili](winsnmp-functions.md)WinSNMP.

 

 




