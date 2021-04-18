---
description: Specifica il modello di hosting del provider. L'impostazione di questa proprietà determina il caricamento del provider in un processo host condiviso con un livello di privilegio specificato.
ms.assetid: 1e5c778d-cd29-449b-88e2-fe0c90d0edcd
ms.tgt_platform: multiple
title: Hosting e sicurezza del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6b88a5727f34fbb76baf62dcdf0488e5eb9eb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316562"
---
# <a name="provider-hosting-and-security"></a>Hosting e sicurezza del provider

La proprietà [**HostingModel**](--win32provider.md) nell'istanza **\_ \_ Win32Provider** che rappresenta il provider specifica il modello di hosting del provider. L'impostazione di questa proprietà determina il caricamento del provider in un processo host condiviso con un livello di privilegio specificato.

## <a name="shared-provider-host-process"></a>Processo host provider condiviso

WMI risiede in un host del servizio condiviso con molti altri servizi. Per evitare di arrestare tutti i servizi in caso di errore di un provider, i provider vengono caricati in un processo host separato denominato "Wmiprvse.exe". È possibile eseguire più di un processo con questo nome. Ognuno di essi può essere eseguito con un account diverso con una sicurezza variabile. Tenere presente che, a partire da Windows Vista, utilizzare il comando [**WinMgmt**](winmgmt.md) per eseguire WMI in un processo separato utilizzando una porta fissa. Per ulteriori informazioni, vedere [connessione a WMI in modalità remota a partire da vista](connecting-to-wmi-remotely-starting-with-vista.md).

L'host condiviso può essere eseguito con uno degli account di sistema seguenti in un processo host Wmiprvse.exe:

-   [LocalSystem](/windows/desktop/Services/localsystem-account)
-   [NetworkService](/windows/desktop/Services/networkservice-account)
-   [LocalService](/windows/desktop/Services/localservice-account)

Un provider può inoltre essere un server COM locale (con estensione exe) o self-hosted che non richiede un host del provider WMI.

## <a name="setting-the-hosting-model"></a>Impostazione del modello di hosting

Poiché LocalSystem è un account con privilegi, è consigliabile impostare [**HostingModel**](--win32provider.md) su **NetworkServiceHost** quando un provider viene eseguito in un Wmiprvse.exe processo. L'account NetworkServiceHost è per i servizi che non richiedono privilegi estesi, ma che devono comunicare in remoto con altri sistemi.

Se non si imposta un valore per la proprietà [**HostingModel**](--win32provider.md) , WMI imposta un valore predefinito di **NetworkServiceHostOrSelfHost**. Se il valore **HostingModel** è impostato su **LocalSystemHost**, WMI utilizza la traccia per generare gli eventi 5603 e 5604 nel registro eventi di Windows. Poiché l'account [LocalSystem](/windows/desktop/Services/localsystem-account) locale è con privilegi elevati, questa impostazione non è consigliata. È possibile visualizzare questi eventi nel **Visualizzatore eventi**. Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).

Impostare la proprietà [**HostingModel**](--win32provider.md) per i provider disaccoppiati come "disaccoppiata: com". I provider creati aggiungendo classi di strumentazione da [**Microsoft. Management. Infrastructure**](/previous-versions//hh872326(v=vs.85)) nel .NET Framework sono provider disaccoppiati. (**System. Management. Instrumentation** non è più supportato). Per ulteriori informazioni sulla creazione di un provider disaccoppiato, vedere [incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md).

Il modello di hosting viene specificato nella proprietà [**HostingModel**](--win32provider.md) dell'istanza **\_ \_ Win32Provider** che rappresenta il provider.

**Per impostare il modello di hosting per un provider**

1.  Nel file MOF che definisce il provider creare un'istanza di [**\_ \_ Win32Provider**](--win32provider.md).
2.  Assegnare un nome al provider nella proprietà **Name** e assegnare l'identificatore di classe (CLSID) dell'oggetto com del provider alla proprietà **CLSID** .

    Nell'esempio di codice seguente viene assegnato un nome alla proprietà del **nome** e il CSLID dell'oggetto com del provider alla proprietà **CLSID** .

    ``` syntax
    Instance of __Win32Provider as $NewProvider
    {
        Name = "MyProvider";
        Clsid = "{.......}";
    }
    ```

3.  Assegnare il valore host condiviso appropriato alla proprietà [**HostingModel**](--win32provider.md) . I valori host condivisi, ad esempio "NetworkServiceHost", sono definiti nella proprietà **HostingSpecification** della classe [**\_ provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) .

    Nell'esempio di codice seguente viene assegnato un valore host condiviso alla proprietà [**HostingModel**](--win32provider.md) .

    ``` syntax
    HostingModel = "NetworkServiceHost";
    ```

Nell'esempio di codice seguente viene illustrato come registrare un provider in NetworkServiceHost.

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost";
}
```

Se si dispone di più provider, è possibile raggrupparli in uno specifico host del servizio registrando il provider in modo che risieda nell'istanza specifica.

Nell'esempio di codice riportato di seguito viene inoltre registrato un provider in NetworkServiceHost. La classe dei [**\_ provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) definisce i valori per i due valori che combinano per creare la proprietà **HostingModel** di [**\_ \_ Win32Provider**](--win32provider.md) . Nell'esempio, il valore "NetworkServiceHost" deriva dalla proprietà **HostingSpecification** dei **\_ provider MSFT** e "localservicehost" deriva dalla proprietà **HostingGroup** .

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost:MySharedHost";
}
```

Esistono problemi di sviluppo speciali per i provider che non sono disaccoppiati e sono ospitati nel processo Wmiprvse. Per ulteriori informazioni, vedere [provider di debug](debugging-providers.md).

Se si scrive un provider che contiene la registrazione di una proprietà o di un provider di classi, non tutti i modelli di threading funzionano. Per ulteriori informazioni, vedere [scelta della registrazione corretta](choosing-correct-registration.md).

## <a name="hostingmodel-values-for-in-process-providers"></a>Valori HostingModel per provider di In-Process

Nell'elenco seguente sono elencati i valori del modello di hosting del provider da utilizzare nell'istanza [**\_ \_ Win32Provider**](--win32provider.md) per i provider eseguiti in un processo Wmiprvse.exe.



| Valore in [ **\_ \_ Win32Provider. HostingModel**](--win32provider.md) | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SelfHost**                                                       | Il provider inizia a usare l'implementazione del server locale anziché in-process. Il contesto di sicurezza del processo in cui viene eseguito il provider determina il contesto di sicurezza del provider.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LocalSystemHost**                                                | Il provider, se implementato come in-process, viene caricato in un host del provider condiviso in esecuzione nel contesto [LocalSystem](/windows/desktop/Services/localsystem-account) . A partire da Windows Vista, **LocalSystemHost** non è più il modello di hosting predefinito se il [**HostingModel**](--win32provider.md) di un provider WMI (**\_ \_ Win32Provider**.**** La proprietà HostingModel) non è specificata. Per ulteriori informazioni, vedere [sicurezza dei modelli di hosting](#provider-hosting-and-security).                                                                                                                                                                                                                                                                               |
| **LocalSystemHostOrSelfHost**                                      | Il provider è self-hosted o caricato nel processo Wmiprvse.exe in esecuzione con l'account [LocalSystem](/windows/desktop/Services/localsystem-account) . Poiché LocalSystem è un account con privilegi elevati, viene generata una voce nel registro eventi di sicurezza NT per notificare agli amministratori di un provider in esecuzione in questo stato attendibile.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **NetworkServiceHost**                                             | Il provider, se implementato come in-process, viene caricato nel processo di Wmiprvse.exe in esecuzione con l'account [NetworkService](/windows/desktop/Services/networkservice-account) . A partire da Windows Vista, questo è il modello di hosting predefinito se il [**HostingModel**](--win32provider.md) di un provider WMI (**\_ \_ Win32Provider**.**** La proprietà HostingModel) non è specificata. Per ulteriori informazioni, vedere [sicurezza dei modelli di hosting](#provider-hosting-and-security).<br/> **NetworkServiceHost** dispone di privilegi limitati e quindi riduce la possibilità di un attacco con elevazione dei privilegi. Se il provider opera solo nel computer locale, impostare la proprietà [**HostingModel**](--win32provider.md) su **localservicehost**.<br/> |
| **NetworkServiceHostOrSelfHost**                                   | Il provider è self-hosted o caricato nel processo WmiPrvse.exe in esecuzione con l'account [NetworkService](/windows/desktop/Services/networkservice-account) . **NetworkServiceHostOrSelfHost** è la configurazione predefinita quando la proprietà [**HostingModel**](--win32provider.md) in **\_ \_ Win32Provider** è **null**. Poiché **NetworkServiceHostOrSelfHost** è l'impostazione predefinita, i provider di sistemi operativi precedenti possono continuare a funzionare in Windows Vista, windows Server 2008 e nei sistemi operativi successivi.                                                                                                                                                                                                                                             |
| **LocalServiceHost**                                               | Il provider, se implementato come in-process, viene caricato nel processo di Wmiprvse.exe in esecuzione con l'account [LocalService](/windows/desktop/Services/localservice-account) . Si tratta del modello di hosting consigliato per i servizi perché LocalService ha privilegi limitati.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="hostingmodel-values-for-decoupled-providers"></a>Valori HostingModel per i provider disaccoppiati

Nell'elenco seguente sono elencati i valori del modello di hosting del provider per i provider disaccoppiati.

<dl> <dt>

<span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**Separato: com**
</dt> <dd>

Il provider è un provider disaccoppiato ospitato in un processo separato che è un client di WMI.

Nell'esempio seguente viene illustrato l'identificatore FoldIdentity per la proprietà [**HostingModel**](--win32provider.md) impostata su **false**, che consente al provider di rappresentare il client.

``` syntax
Decoupled:Com:FoldIdentity(FALSE)
```

Se FoldIdentity non è specificato, il valore di FoldIdentity viene impostato su **true** per impostazione predefinita. Per motivi di sicurezza, è consigliabile non specificare FoldIdentity (FALSE) poiché un'applicazione non autorizzata con rappresentazione del delegato può influire su un intero dominio.

Nell'esempio seguente viene illustrata la proprietà [**HostingModel**](--win32provider.md) impostata nel modo consigliato che equivale a impostare FOLDIDENTITY (true).

``` syntax
Decoupled:Com
```

</dd> <dt>

<span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**Separato: noncom**
</dt> <dd>

Solo per uso interno. Non supportata.

</dd> </dl>

## <a name="security-of-hosting-models"></a>Sicurezza dei modelli di hosting

Per la maggior parte delle situazioni, **LocalSystem** non è necessario e il contesto **NetworkServiceHost** è più appropriato. La maggior parte dei provider WMI deve rappresentare il contesto di sicurezza del client per eseguire operazioni richieste per conto del client WMI. A partire da Windows Vista, un provider WMI che non dispone di una definizione di modello di hosting e viene eseguito come se fosse in esecuzione in **LocalSystem** non verrà eseguito correttamente. Per correggere questa situazione, modificare il modello di hosting previsto e assicurarsi che il codice del provider WMI esegua le operazioni nel contesto di sicurezza del client rappresentando il client WMI. LocalSystem è raramente un requisito. Se il provider deve disporre di tale livello di privilegio, specificare il modello di hosting con l'istruzione seguente nel file MOF.

``` syntax
HostingModel=LocalSystemHost
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scelta della registrazione corretta](choosing-correct-registration.md)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Sicurezza degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Classi di configurazione e risoluzione dei problemi del provider](provider-configuration-and-troubleshooting-classes.md)
</dt> <dt>

[**\_Provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 

