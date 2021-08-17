---
description: Il provider Simple Network Management Protocol (SNMP) consente alle applicazioni client di accedere alle informazioni SNMP Windows Management Instrumentation (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI e SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f1327afe2a86a1f56f40c0a93d904148ccaf1fd0547b6cb623d9eb420c2a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992301"
---
# <a name="wmi-and-snmp"></a>WMI e SNMP

Il provider Simple Network Management Protocol (SNMP) consente alle applicazioni client di accedere alle informazioni SNMP Windows Management Instrumentation (WMI). Il provider SNMP non è installato per impostazione predefinita. Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

Simple Network Management Protocol (SNMP) usa uno schema per definire gli oggetti. Lo schema è diverso da quello usato in WMI. Lo schema SNMPv1 e SNMPv2C è denominato Struttura delle informazioni di gestione (SMI) ed è in pacchetto come file MIB (Management Information Base). I file MIB definiscono gli oggetti usando un linguaggio standard, Abstract Syntax Notation 1 (ASN.1) e una serie di definizioni di macro che fungono da modelli per descrivere gli oggetti. Le macro forniscono informazioni quali il nome dell'oggetto, l'identificatore, la sintassi, la descrizione, i diritti di accesso, le operazioni del protocollo e la codifica del protocollo. La tabella seguente elenca il modo in cui il provider SNMP gestisce diversi aspetti di un oggetto MIB.



| Argomento                                                    | Descrizione                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [NOTIFICATION-TYPE Macro](notification-type-macro.md)   | Modalità di mapping della macro **NOTIFICATION-TYPE** da SNMP a WMI.  |
| [OBJECT-TYPE Macro](object-type-macro.md)               | Modalità di mapping della macro **OBJECT-TYPE** da SNMP a WMI.        |
| [TEXTUAL-CONVENTION Macro](textual-convention-macro.md) | Mapping della macro **TEXTUAL-CONVENTION** da SNMP a WMI. |
| [TRAP-TYPE Macro](trap-type-macro.md)                   | Modalità di mapping della macro **TRAP-TYPE** da SNMP a WMI.          |



 

Il provider SNMP viene fornito con un compilatore che converte gli oggetti MIB in oggetti WMI. Il compilatore SNMP può anche inviare un errore o altri messaggi. Per altre informazioni, vedere [Messaggi di errore del compilatore SNMP](snmp-compiler-error-messages.md) e Messaggi di informazioni [generali.](general-information-messages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> <dt>

[Provider WMI](wmi-providers.md)
</dt> </dl>

 

 



