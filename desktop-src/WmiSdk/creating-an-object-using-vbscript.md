---
description: È possibile creare un oggetto per WMI in Visual Basic Scripting Edition (VBScript) connettendosi a WMI e quindi chiamando CreateObject. Nella tabella seguente sono elencati i metodi dell'API di scripting per WMI che supportano la creazione di oggetti.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Creazione di un oggetto tramite VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485356"
---
# <a name="creating-an-object-using-vbscript"></a>Creazione di un oggetto tramite VBScript

È possibile creare un oggetto per WMI in Visual Basic Scripting Edition (VBScript) connettendosi a WMI e quindi chiamando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)). Nella tabella seguente sono elencati i metodi dell'API di scripting per WMI che supportano la creazione di oggetti.



| Interfaccia                                        | ProgID                             |
|--------------------------------------------------|------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)           | "WbemScripting. SwbemDateTime"      |
| [**SWbemLocator**](swbemlocator.md)             | "WbemScripting. SWbemLocator"       |
| [**SWbemLastError**](swbemlasterror.md)         | "WbemScripting. SWbem. LastError"    |
| [**SWbemObjectPath**](swbemobjectpath.md)       | "WbemScripting. SWbemObjectPath"    |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | "WbemScripting. SWbemNamedValueSet" |
| [**SWbemRefresher**](swbemrefresher.md)         | "WbemScripting. SWbemRefresher"     |
| [**SWbemSink**](swbemsink.md)                   | "WbemScripting. SWbemSink"          |



 

Nella procedura riportata di seguito viene descritto come creare un oggetto WMI utilizzando VBScript.

**Per creare un oggetto WMI utilizzando VBScript**

1.  Connettersi a WMI utilizzando un moniker o un oggetto [**SWbemLocator**](swbemlocator.md) .

    Per ulteriori informazioni, vedere [creazione di uno script WMI](creating-a-wmi-script.md).

2.  Effettuare una chiamata al metodo [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.

    Nell'esempio di codice seguente viene illustrato come creare un oggetto.

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    Se si usa un moniker nel passaggio 1, non è necessario chiamare di nuovo [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

 

 
