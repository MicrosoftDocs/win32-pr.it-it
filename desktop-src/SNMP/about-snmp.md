---
title: Informazioni su SNMP
description: SNMP usa un'architettura distribuita costituita da Manager e agenti.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047188"
---
# <a name="about-snmp"></a>Informazioni su SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

SNMP usa un'architettura distribuita costituita da Manager e agenti. Un agente è un'applicazione SNMP che risponde alle query dalle applicazioni di gestione SNMP. L'agente SNMP è responsabile del recupero e dell'aggiornamento delle informazioni di gestione locali in base alle richieste di gestione SNMP. L'agente invia inoltre una notifica ai responsabili registrati quando si verificano eventi o trap significativi. Un Manager è un'applicazione SNMP che genera query per le applicazioni dell'agente SNMP e riceve trap dalle applicazioni dell'agente SNMP.

Nei computer che eseguono Microsoft Windows XP/Windows 2000/Windows NT, l'agente SNMP viene implementato dal servizio SNMP (SNMP.EXE). SNMP Manager è in genere un'applicazione console di gestione SNMP di terze parti. Non è necessario che l'applicazione console di gestione venga eseguita nello stesso host dell'agente SNMP. Per utilizzare le informazioni fornite dal servizio SNMP Microsoft, è necessaria almeno un'applicazione console di gestione SNMP. Il sistema include librerie che supportano le applicazioni console di gestione SNMP, ma in questo momento non include un'applicazione console di gestione SNMP.

 

 