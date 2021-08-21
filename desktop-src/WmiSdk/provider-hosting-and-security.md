---
description: Specifica il modello di hosting del provider. L'impostazione di questa proprietà determina il caricamento del provider in un processo host condiviso con un livello di privilegio specificato.
ms.assetid: 1e5c778d-cd29-449b-88e2-fe0c90d0edcd
ms.tgt_platform: multiple
title: Hosting e sicurezza dei provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce0853b268f3d0bef0c43cbeabc10651885f0bd3b07f79d5c1b29072b560c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050489"
---
# <a name="provider-hosting-and-security"></a>Hosting e sicurezza dei provider

La [**proprietà HostingModel**](--win32provider.md) nell'istanza **\_ \_ Win32Provider** che rappresenta il provider specifica il modello di hosting del provider. L'impostazione di questa proprietà determina il caricamento del provider in un processo host condiviso con un livello di privilegio specificato.

## <a name="shared-provider-host-process"></a>Processo host del provider condiviso

WMI risiede in un host del servizio condiviso con diversi altri servizi. Per evitare di arrestare tutti i servizi in caso di errore di un provider, i provider vengono caricati in un processo host separato denominato "Wmiprvse.exe". È possibile eseguire più di un processo con questo nome. Ognuno può essere eseguito con un account diverso con una protezione variabile. Tenere presente che, a partire da Windows Vista, usare il [**comando winmgmt**](winmgmt.md) per eseguire WMI in un processo separato usando una porta fissa. Per altre informazioni, vedere [Connessione a WMI in remoto a partire da Vista.](connecting-to-wmi-remotely-starting-with-vista.md)

L'host condiviso può essere eseguito con uno degli account di sistema seguenti in un Wmiprvse.exe processo host:

-   [LocalSystem](/windows/desktop/Services/localsystem-account)
-   [NetworkService](/windows/desktop/Services/networkservice-account)
-   [LocalService](/windows/desktop/Services/localservice-account)

Un provider può anche essere un server COM locale (.exe) o self-hosted, che non richiede un host del provider WMI.

## <a name="setting-the-hosting-model"></a>Impostazione del modello di hosting

Poiché LocalSystem è un account con privilegi, è consigliabile impostare [**HostingModel**](--win32provider.md) su **NetworkServiceHost** quando un provider è in esecuzione in un processo Wmiprvse.exe servizio. L'account NetworkServiceHost è per i servizi che non richiedono privilegi estesi, ma che devono comunicare in remoto con altri sistemi.

Se non si imposta un valore per la [**proprietà HostingModel,**](--win32provider.md) WMI imposta il valore predefinito **NetworkServiceHostOrSelfHost**. Se il **valore HostingModel** è impostato su **LocalSystemHost**, WMI usa la traccia per generare gli eventi 5603 e 5604 nel Windows eventi. Poiché l'account [LocalSystem](/windows/desktop/Services/localsystem-account) locale ha privilegi elevati, questa impostazione non è consigliata. È possibile visualizzare questi eventi nel **Visualizzatore eventi**. Per altre informazioni, vedere [Traccia dell'attività WMI.](tracing-wmi-activity.md)

Impostare la [**proprietà HostingModel**](--win32provider.md) per i provider disaccoccodati su "Decoupled:Com". I provider creati aggiungendo classi di strumentazione [**da Microsoft.Management.Infrastructure**](/previous-versions//hh872326(v=vs.85)) nel .NET Framework sono provider disaccoccodati. (**System.Management.Instrumentation** non è più supportato). Per altre informazioni sulla creazione di un provider disaccoccodato, vedere [Incorporamento di un provider in un'applicazione.](incorporating-a-provider-in-an-application.md)

Il modello di hosting viene specificato nella [**proprietà HostingModel**](--win32provider.md) nell'istanza **\_ \_ Win32Provider** che rappresenta il provider.

**Per impostare il modello di hosting per un provider**

1.  Nel file MOF che definisce il provider creare un'istanza di [**\_ \_ Win32Provider**](--win32provider.md).
2.  Assegnare un nome al provider nella proprietà **Name** e assegnare l'identificatore di classe (CLSID) dell'oggetto COM del provider alla **proprietà Clsid.**

    Nell'esempio di codice seguente viene assegnato un nome alla proprietà **Name** e l'elemento CSLID dell'oggetto COM del provider alla **proprietà Clsid.**

    ``` syntax
    Instance of __Win32Provider as $NewProvider
    {
        Name = "MyProvider";
        Clsid = "{.......}";
    }
    ```

3.  Assegnare il valore host condiviso appropriato alla [**proprietà HostingModel.**](--win32provider.md) I valori dell'host condiviso, ad esempio "NetworkServiceHost", sono definiti nella **proprietà HostingSpecification** della [**classe Provider \_ MSFT.**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)

    L'esempio di codice seguente assegna un valore host condiviso alla [**proprietà HostingModel.**](--win32provider.md)

    ``` syntax
    HostingModel = "NetworkServiceHost";
    ```

L'esempio di codice seguente illustra come registrare un provider in NetworkServiceHost.

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost";
}
```

Se si dispone di più provider, è possibile raggrupparli in un host del servizio specifico registrando il provider in modo che risieda nell'istanza specifica.

L'esempio di codice seguente registra anche un provider in NetworkServiceHost. La [**classe \_ Provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) definisce i valori per i due valori combinati per creare la [**\_ \_ proprietà HostingModel Win32Provider.**](--win32provider.md)  Nell'esempio, il valore "NetworkServiceHost" deriva dalla proprietà **HostingSpecification** dei provider **\_ MSFT** e "LocalServiceHost" deriva dalla **proprietà HostingGroup.**

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost:MySharedHost";
}
```

Esistono problemi di sviluppo speciali per i provider che non sono disaccodati e sono ospitati nel processo Wmiprvse. Per altre informazioni, vedere [Debugging Providers](debugging-providers.md).

Se si scrive un provider che contiene la registrazione del provider di proprietà o di classe, non tutti i modelli di threading funzionano. Per altre informazioni, vedere [Scelta della registrazione corretta.](choosing-correct-registration.md)

## <a name="hostingmodel-values-for-in-process-providers"></a>Valori HostingModel per In-Process provider

Nell'elenco seguente sono elencati i valori del modello di hosting del provider da usare nell'istanza [**\_ \_ win32Provider**](--win32provider.md) per i provider eseguiti in un Wmiprvse.exe processo.



| Valore in [ **\_ \_ Win32Provider.HostingModel**](--win32provider.md) | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SelfHost**                                                       | Il provider inizia a usare l'implementazione del server locale anziché in-process. Il contesto di sicurezza del processo in cui viene eseguito il provider determina il contesto di sicurezza del provider.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LocalSystemHost**                                                | Il provider, se implementato come in-process, viene caricato in un host del provider condiviso in esecuzione nel [contesto LocalSystem.](/windows/desktop/Services/localsystem-account) A partire Windows Vista, **LocalSystemHost** non è più il modello di hosting predefinito se [**hostingModel**](--win32provider.md) di un provider WMI (**\_ \_ Win32Provider**.**HostingModel** property) non è specificato. Per altre informazioni, vedere [Sicurezza dei modelli di hosting.](#provider-hosting-and-security)                                                                                                                                                                                                                                                                               |
| **LocalSystemHostOrSelfHost**                                      | Il provider è self-hosted o caricato nel processo Wmiprvse.exe in esecuzione con l'account [LocalSystem.](/windows/desktop/Services/localsystem-account) Poiché LocalSystem è un account con privilegi elevati, viene generata una voce nel registro eventi NT di sicurezza per notificare agli amministratori di un provider in esecuzione in questo stato attendibile.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **NetworkServiceHost**                                             | Il provider, se implementato come in-process, viene caricato nel processo Wmiprvse.exe in esecuzione con l'account [NetworkService.](/windows/desktop/Services/networkservice-account) A partire Windows Vista, questo è il modello di hosting predefinito se [**hostingModel**](--win32provider.md) di un provider WMI (**\_ \_ Win32Provider**.**HostingModel** property) non è specificato. Per altre informazioni, vedere [Sicurezza dei modelli di hosting.](#provider-hosting-and-security)<br/> **NetworkServiceHost dispone** di privilegi limitati e pertanto riduce la possibilità di un attacco di elevazione dei privilegi. Se il provider funziona solo all'interno del computer locale, impostare la [**proprietà HostingModel**](--win32provider.md) su **LocalServiceHost.**<br/> |
| **NetworkServiceHostOrSelfHost**                                   | Il provider è self-hosted o caricato nel processo WmiPrvse.exe in esecuzione con l'account [NetworkService.](/windows/desktop/Services/networkservice-account) **NetworkServiceHostOrSelfHost è** la configurazione predefinita quando la [**proprietà HostingModel**](--win32provider.md) in **\_ \_ Win32Provider** è **NULL.** Poiché **NetworkServiceHostOrSelfHost** è l'impostazione predefinita, i provider dei sistemi operativi precedenti possono continuare a funzionare in Windows Vista, Windows Server 2008 e sistemi operativi successivi.                                                                                                                                                                                                                                             |
| **LocalServiceHost**                                               | Il provider, se implementato come in-process, viene caricato nel processo Wmiprvse.exe in esecuzione con l'account [LocalService.](/windows/desktop/Services/localservice-account) Questo è il modello di hosting consigliato per i servizi perché LocalService ha privilegi limitati.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="hostingmodel-values-for-decoupled-providers"></a>Valori HostingModel per provider disaccoccodati

Nell'elenco seguente sono elencati i valori del modello di hosting del provider per i provider disaccoccodati.

<dl> <dt>

<span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**Disaccoccodato:Com**
</dt> <dd>

Il provider è un provider disaccoccodato ospitato in un processo separato da client a WMI.

L'esempio seguente illustra l'identificatore FoldIdentity per la proprietà [**HostingModel**](--win32provider.md) impostata su **FALSE,** che consente al provider di rappresentare il client.

``` syntax
Decoupled:Com:FoldIdentity(FALSE)
```

Se FoldIdentity non viene specificato, il valore foldIdentity viene impostato su **TRUE** per impostazione predefinita. Per motivi di sicurezza, è consigliabile non specificare FoldIdentity(FALSE) perché un'applicazione non autorizzata con rappresentazione di Delegate può influire su un intero dominio.

Nell'esempio seguente viene illustrata la proprietà [**HostingModel**](--win32provider.md) impostata nel modo consigliato equivalente all'impostazione di FoldIdentity(TRUE).

``` syntax
Decoupled:Com
```

</dd> <dt>

<span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**Disaccoccodato:Noncom**
</dt> <dd>

Solo per uso interno. Non supportata.

</dd> </dl>

## <a name="security-of-hosting-models"></a>Sicurezza dei modelli di hosting

Nella maggior parte dei **casi, LocalSystem** non è necessario e **il contesto NetworkServiceHost** è più appropriato. La maggior parte dei provider WMI deve rappresentare il contesto di sicurezza client per eseguire le operazioni richieste per conto del client WMI. A partire Windows Vista, un provider WMI che non dispone di una definizione di modello di hosting e viene eseguito come se fosse in esecuzione in **LocalSystem** non verrà eseguito correttamente. Per risolvere questo problema, modificare il modello di hosting previsto e assicurarsi che il codice del provider WMI esegua le operazioni nel contesto di sicurezza client rappresentando il client WMI. LocalSystem è raramente un requisito. Se il provider deve avere tale livello di privilegio, specificare il modello di hosting con l'istruzione seguente nel file MOF.

``` syntax
HostingModel=LocalSystemHost
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scelta della registrazione corretta](choosing-correct-registration.md)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Classi di configurazione e risoluzione dei problemi del provider](provider-configuration-and-troubleshooting-classes.md)
</dt> <dt>

[**Provider \_ MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 

