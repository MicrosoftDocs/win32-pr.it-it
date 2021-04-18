---
title: Definizione di attività e OpCode
description: I provider utilizzano attività e codici operativi per raggruppare logicamente gli eventi. Gli eventi di raggruppamento consentono agli utenti di eseguire query solo sugli eventi che contengono combinazioni di attività e codici operativi specifici.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257166a34c167d076fec39ac6997d12dc785450
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104516690"
---
# <a name="defining-tasks-and-opcodes"></a>Definizione di attività e OpCode

I provider utilizzano attività e codici operativi per raggruppare logicamente gli eventi. Gli eventi di raggruppamento consentono agli utenti di eseguire query solo sugli eventi che contengono combinazioni di attività e codici operativi specifici. In genere, è possibile utilizzare le attività per identificare un componente principale del provider, ad esempio il componente di rete o di database. È quindi possibile utilizzare i codici operativi per identificare le operazioni eseguite dal componente, ad esempio le operazioni di invio e ricezione per un componente di rete. Se si dispone di un solo componente, è possibile utilizzare l'attività per riflettere un'operazione principale nel componente, ad esempio Connect o Disconnect, e utilizzare Opcode per riflettere un'attività all'interno dell'operazione, ad esempio la lettura del registro di sistema. È anche possibile usare opcode senza specificare un'attività. Il modo in cui si usano le attività e i codici operativi per raggruppare gli eventi per il consumer è completamente attivo.

Per definire un'attività, usare l'elemento **Task** . Per definire un codice operativo, usare l'elemento **OpCode** . È possibile specificare fino a 228 codici operativi. Il **valore** dell'attività deve essere maggiore di 0. I codici operativi devono essere compresi tra 11 e 239. Il file Winmeta.xml definisce le operazioni comuni che è possibile usare anziché definire i propri.

Nell'esempio seguente viene illustrato come definire diverse attività e codici operativi.

```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <tasks>
                    <task name="Disconnect" 
                          symbol="TASK_DISCONNECT"
                          value="1"
                          message="$(string.Task.Disconnect)"/>
 
                    <task name="Connect" 
                          symbol="TASK_CONNECT"
                          value="2"
                          message="$(string.Task.Connect)">
                    </task>

                    <task name="Validate" 
                          symbol="TASK_VALIDATE"
                          value="3"
                          message="$(string.Task.Validate)">
                    </task>
                </tasks>

                <opcodes>
                    <opcode name="Initialize" 
                            symbol="OPCODE_INITIALIZE" 
                            value="12"
                            message="$(string.Opcode.Initialize)"/>

                    <opcode name="Cleanup" 
                            symbol="OPCODE_CLEANUP" 
                            value="13"
                            message="$(string.Opcode.Cleanup)"/>
                 </opcodes>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Task.Disconnect" value="Disconnect"/>
                <string id="Task.Connect" value="Connect"/>
                <string id="Task.Connect.ReadRegistry" value="ReadRegistry"/>
                <string id="Task.Validate" value="Connect"/>
                <string id="Task.Validate.GetRules" value="GetRules"/>
                <string id="Opcode.Initialize" value="Initialize"/>
                <string id="Opcode.Cleanup" value="Cleanup"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
