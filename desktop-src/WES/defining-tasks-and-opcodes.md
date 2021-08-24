---
title: Definizione di attività e opcode
description: I provider usano attività e opcode per raggruppare gli eventi in modo logico. Il raggruppamento degli eventi consente ai consumer di eseguire query solo per gli eventi che contengono combinazioni di attività e codice operativo specifiche.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb576251edf4de14c564c6e468209ece93e5840da9e0d821c20b132794f48ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032471"
---
# <a name="defining-tasks-and-opcodes"></a>Definizione di attività e opcode

I provider usano attività e opcode per raggruppare gli eventi in modo logico. Il raggruppamento degli eventi consente ai consumer di eseguire query solo per gli eventi che contengono combinazioni di attività e codice operativo specifiche. In genere, si usano le attività per identificare un componente principale del provider, ad esempio il componente di rete o di database. È quindi possibile usare i codici operativo per identificare le operazioni eseguite dal componente, ad esempio le operazioni di invio e ricezione per un componente di rete. Se si ha un solo componente, è possibile usare l'attività per riflettere un'operazione principale nel componente, ad esempio la connessione o la disconnessione, e usare il codice operativo per riflettere un'attività all'interno dell'operazione, ad esempio la lettura del Registro di sistema. È anche possibile usare il codice operativo senza specificare un'attività. La modalità di utilizzo di task e opcode per raggruppare gli eventi per il consumer è completamente all'utente.

Per definire un'attività, usare **l'elemento** task. Per definire un codice operativo, usare **l'elemento opcode.** È possibile specificare fino a 228 codici operativo. Il valore **dell'attività** deve essere maggiore di 0. I codici operativo devono essere nell'intervallo compreso tra 11 e 239. Il Winmeta.xml file definisce operazioni comuni che è possibile usare invece di definirne di proprie.

L'esempio seguente illustra come definire diverse attività e opcode.

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
