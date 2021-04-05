---
title: Recupero di dati dal computer locale
description: Sebbene Gestione remota Windows e il protocollo di WS-Management siano progettati in modo esplicito per la comunicazione remota, è il caso più semplice stabilire una sessione nel computer locale.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727407"
---
# <a name="obtaining-data-from-the-local-computer"></a>Recupero di dati dal computer locale

Sebbene Gestione remota Windows e il protocollo di WS-Management siano progettati in modo esplicito per la comunicazione remota, è il caso più semplice stabilire una sessione nel computer locale. È possibile che alcuni script richiedano l'accesso ai dati nel computer locale e nei computer remoti.

**WinRM versione 2,0:  **

Tutte le operazioni sono considerate remote e il servizio gestione remota Windows deve essere avviato prima dell'esecuzione di qualsiasi operazione. Se non viene specificata una destinazione remota, il localhost viene usato per impostazione predefinita e tutte le operazioni verranno inviate al servizio gestione remota Windows locale. Per ulteriori informazioni sull'avvio del servizio gestione remota Windows, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).

Quando si utilizza il servizio gestione remota Windows per le operazioni locali, è necessario considerare i fattori seguenti:

-   La configurazione locale di WinRM può essere letta solo dagli amministratori.
-   Per gli spazi dei nomi WMI è necessario impostare autorizzazioni Remote Enable. Per ulteriori informazioni, vedere [protezione di una connessione WMI remota](../wmisdk/securing-a-remote-wmi-connection.md).
-   Se non viene creato un [*listener*](windows-remote-management-glossary.md) WinRM, il servizio WinRM è in ascolto delle richieste locali sulla porta 47001.

Ogni script WinRM deve iniziare stabilendo una sessione o una connessione a un computer creando un oggetto [**sessione**](session.md) . Dopo aver creato la sessione, è possibile utilizzare i metodi dell'oggetto **sessione** , ad esempio [**Session. enumerate**](session-enumerate.md) o [**Session. Invoke**](session-invoke.md) , per ottenere i dati o per eseguire metodi.

La creazione di una sessione è piuttosto simile alla [connessione](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) a uno spazio dei nomi di Strumentazione gestione Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page)). La sessione è essenzialmente un livello che consente di inviare e ricevere dati tramite messaggi [*SOAP*](windows-remote-management-glossary.md) e il protocollo WS-Management. Per ulteriori informazioni, vedere [protocollo WS-Management](ws-management-protocol.md).

Chiamando il metodo [**WSMan. CreateSession**](wsman-createsession.md) per creare un oggetto [**sessione**](session.md) , viene avviata una [*sessione*](windows-remote-management-glossary.md) di che si connette alla gestione remota Windows locale.

**Per creare una sessione WSMan e ottenere i dati**

1.  Creare un oggetto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Creare una sessione chiamando il metodo [**WSMan. CreateSession**](wsman-createsession.md) . Questa sessione viene eseguita con il nome utente e la password di accesso e può ottenere dati tramite la gestione remota Windows locale.

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  Creare un [*URI*](windows-remote-management-glossary.md) di risorsa per identificare la [*risorsa*](windows-remote-management-glossary.md) che si vuole gestire o per cui si desidera ottenere i dati. Per altre informazioni sulla formattazione di un URI, vedere [URI di risorsa](resource-uris.md). Questo URI di risorsa è relativo a un'istanza specifica della classe del [**\_ servizio WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) , il servizio Winmgmt. Per ulteriori informazioni, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  Chiamare i metodi di [**sessione**](session.md) che ottengono o enumerano i dati usando l'URI della risorsa. Per ulteriori informazioni, vedere [API di scripting WinRM](winrm-scripting-api.md).

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  Per ottenere o gestire i dati da un altro computer o usare metodi di autenticazione diversi, vedere [recupero di dati da un computer remoto](obtaining-data-from-a-remote-computer.md).

Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo che consente di ottenere l'istanza specifica del [**\_ servizio WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) denominato "WinMgmt".


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo con la trasformazione dei dati. Per ulteriori informazioni, vedere [visualizzazione dell'output XML dagli script WinRM](displaying-xml-output-from-winrm-scripts.md).


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Utilizzo di Gestione remota Windows](using-windows-remote-management.md)
</dt> <dt>

[Riferimento Gestione remota Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 