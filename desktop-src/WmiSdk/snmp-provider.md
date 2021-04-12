---
description: Il provider Simple Network Management Protocol (SNMP) consente alle applicazioni client di accedere alle informazioni SNMP tramite Strumentazione gestione Windows (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI e SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233993"
---
# <a name="wmi-and-snmp"></a>WMI e SNMP

Il provider Simple Network Management Protocol (SNMP) consente alle applicazioni client di accedere alle informazioni SNMP tramite Strumentazione gestione Windows (WMI). Il provider SNMP non è installato per impostazione predefinita. Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

Simple Network Management Protocol (SNMP) usa uno schema per definire gli oggetti. Lo schema è diverso dallo schema utilizzato in WMI. Lo schema SNMPv1 e SNMPv2C è denominato struttura delle informazioni di gestione (SMI) ed è incluso in un pacchetto come file MIB (Management Information Base). I file MIB definiscono gli oggetti utilizzando un linguaggio standard, ovvero Abstract Syntax Notation 1 (ASN. 1), e una serie di definizioni di macro utilizzate come modelli per la descrizione degli oggetti. Le macro forniscono informazioni quali il nome dell'oggetto, l'identificatore, la sintassi, la descrizione, i diritti di accesso, le operazioni di protocollo e la codifica del protocollo. Nella tabella seguente viene elencato il modo in cui il provider SNMP gestisce diversi aspetti di un oggetto MIB.



| Argomento                                                    | Descrizione                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [Macro del tipo di notifica](notification-type-macro.md)   | Modalità di mapping della macro del **tipo di notifica** da SNMP a WMI.  |
| [Macro di tipo oggetto](object-type-macro.md)               | Modalità di mapping della macro di **tipo oggetto** da SNMP a WMI.        |
| [Macro convenzione testuale](textual-convention-macro.md) | Come viene eseguito il mapping della macro della **convenzione testuale** da SNMP a WMI. |
| [Macro di tipo TRAP](trap-type-macro.md)                   | Come viene eseguito il mapping della macro di **tipo trap** da SNMP a WMI.          |



 

Il provider SNMP è dotato di un compilatore che converte gli oggetti MIB in oggetti WMI. Il compilatore SNMP può inoltre restituire errori o altri messaggi. Per ulteriori informazioni, vedere [messaggi di errore del compilatore SNMP](snmp-compiler-error-messages.md) e [messaggi informativi generali](general-information-messages.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> <dt>

[Provider WMI](wmi-providers.md)
</dt> </dl>

 

 



