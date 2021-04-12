---
description: WMI contiene un set di classi per la risoluzione dei problemi relativi alle applicazioni client che utilizzano provider WMI.
ms.assetid: f69b360a-2c24-4776-bcda-b51edde0dcde
ms.tgt_platform: multiple
title: Risoluzione dei problemi relativi alle applicazioni client WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a84646aa42cd0ccd649e3937f0eba257343e9a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232620"
---
# <a name="troubleshooting-wmi-client-applications"></a>Risoluzione dei problemi relativi alle applicazioni client WMI

WMI contiene un set di classi per la [risoluzione dei problemi relativi](wmi-troubleshooting-classes.md) alle applicazioni client che utilizzano provider WMI. Le classi di evento per la risoluzione dei problemi sono associate alle classi di evento WMI, in modo che sia possibile tenere traccia dell'esecuzione dell'applicazione usando un log degli eventi di risoluzione dei problemi acquisiti.

Nell'elenco seguente sono riportati alcuni esempi di classi di evento per la risoluzione dei problemi:

-   [**MSFT \_ provider WMI \_ ExecMethodAsyncEvent \_ pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    Generato prima che WMI chiami [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) nel provider.

-   [**\_Post provider WMI \_ ExecMethodAsyncEvent \_ MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    Generato dopo la chiamata di WMI [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) nel provider.

Nella procedura seguente viene illustrato come risolvere i problemi relativi all'esecuzione dell'applicazione.

**Per configurare la risoluzione dei problemi WMI**

1.  Creazione e compilazione di un file MOF per l'utilizzo del consumer di eventi di registrazione WMI.
2.  Eseguire l'applicazione client.
3.  Consente di visualizzare il file di log per la risoluzione dei problemi relativi a tutti gli eventi di errore e di operazione del provider e analizzare il log per diagnosticare i problemi del client che si stanno riscontrando.

Un altro approccio per la risoluzione dei problemi consiste nel visualizzare l'elenco dei provider attualmente presenti nella cache del computer, enumerando i [**\_ provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) nello spazio dei nomi **\\ CIMV2 radice** . In questa classe sono disponibili metodi che consentono di caricare e scaricare i provider a scopo di debug o di installazione.

Nell'esempio di codice seguente viene utilizzato il consumer di eventi di registrazione WMI per acquisire tutti gli eventi della classe di evento Parent, acquisendo quindi tutti gli eventi di operazione del provider.

``` syntax
#pragma autorecover
#pragma namespace("\\\\.\\root\\subscription")

instance of __EventFilter as $Filter
{
  Name = "ProviderOperationEvents" ;
  EventNamespace = "root\\cimv2" ;
  Query = "SELECT * FROM MSFT_WmiProvider_OperationEvent" ;
  QueryLanguage = "WQL" ;
} ;

Instance of LogFileEventConsumer as $Consumer
{
  Name = "ProviderOperationEvents" ;
  FileName = "C:\\test.txt" ;
  Text = "Operation - %__TEXT%" ;
} ;

instance of __FilterToConsumerBinding
{
  Filter = $Filter ;
  Consumer = $Consumer ;
  MaintainSecurityContext = TRUE ;
} ;
```

Quando i messaggi di errore indicano un errore di caricamento del provider, utilizzare [**MSFT \_ provider WMI \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) per identificare il provider che ha causato l'errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> <dt>

[Classi di risoluzione dei problemi WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
