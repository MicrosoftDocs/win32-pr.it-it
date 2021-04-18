---
description: Uso di file di configurazione Per-Application
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: Uso di file di configurazione Per-Application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4d59d05f6a7b9b894a2577eb55cceffa49d267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304723"
---
# <a name="using-per-application-configuration-files"></a>Uso di file di configurazione Per-Application

Per l'utilizzo di file di configurazione per applicazione COM+ sono necessari i passaggi di base seguenti:

-   Configurare una directory radice dell'applicazione per un'applicazione COM+.
-   Creare file Application. manifest e application.config nella directory radice dell'applicazione COM+.

> [!Note]  
> I file di configurazione per applicazione sono disponibili solo a partire da Windows XP con Service Pack 2 (SP2) e Windows Server 2003.

 

**Per usare un file di configurazione per applicazione**

1.  Creare una libreria di classi .NET con un riferimento all'assembly System. EnterpriseServices.

2.  La libreria di classi deve contenere il codice seguente:

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    Si noti che "ConfigData1" è un nome di impostazione di esempio. È possibile sostituirlo con il nome dell'impostazione scelta.

3.  Creare un'applicazione COM+ vuota. Per istruzioni su come eseguire questa operazione, vedere [creazione di una nuova applicazione com+](creating-a-new-com--application.md).
4.  Installare la libreria di classi creata nell'applicazione COM+. Per istruzioni su come eseguire questa operazione, vedere [installazione di nuovi componenti](installing-new-components.md).
5.  Nello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sull'applicazione COM+ creata e selezionare **Proprietà**.
6.  Nella finestra di dialogo **Proprietà** selezionare la scheda **attivazione** .
7.  Verificare che il **tipo di attivazione** sia impostato su **applicazione server**.
8.  Nella casella di testo **directory radice dell'applicazione** immettere il percorso o selezionare la directory in cui si desidera archiviare i file di configurazione dell'applicazione.
9.  Fare clic su **OK**.

    Si noti che è inoltre possibile specificare la directory radice dell'applicazione COM+ tramite la proprietà ApplicationDirectory della classe [**COMAdminCatalogObject**](comadmincatalogobject.md) . Per ulteriori informazioni, vedere [**applicazioni**](applications.md).

10. Nella directory in cui si è scelto di archiviare i file di configurazione dell'applicazione, creare un file denominato *Application*. manifest. Con un editor di testo, aggiungere il testo seguente al file:

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. Nella stessa directory creare un file denominato *Application*. config. Con un editor di testo, aggiungere il testo seguente al file:

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    Si noti che questo file di configurazione è solo un esempio. È possibile creare più chiavi con nomi e valori diversi. Si noti, tuttavia, che "ConfigData1" corrisponde al nome dell'impostazione usato nella libreria di classi creata in precedenza.

12. Creare un'applicazione console .NET, con un riferimento alla libreria di classi .NET creata in precedenza e un riferimento all'assembly System. EnterpriseServices.
13. L'applicazione console deve contenere il codice seguente:
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

Eseguire l'applicazione console. L'output dovrebbe essere simile al seguente:

``` syntax
Configuration Data Number 1
```

 

 



