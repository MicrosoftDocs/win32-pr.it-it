---
description: WMI contiene un set di classi per la risoluzione dei problemi delle applicazioni client che usano provider WMI.
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
ms.openlocfilehash: 7fb9eb8c438faab8915691ee2c9c8a4c77d247c6802f8f114683a79d2833bd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050029"
---
# <a name="troubleshooting-wmi-client-applications"></a>Risoluzione dei problemi relativi alle applicazioni client WMI

WMI contiene un set di classi per la risoluzione [dei problemi delle](wmi-troubleshooting-classes.md) applicazioni client che usano provider WMI. Le classi di eventi di risoluzione dei problemi sono abbinate alle classi di eventi WMI, in modo che sia possibile tenere traccia dell'esecuzione dell'applicazione usando un log degli eventi di risoluzione dei problemi acquisiti.

L'elenco seguente contiene esempi di classi di evento per la risoluzione dei problemi:

-   [**Msft \_ WmiProvider \_ ExecMethodAsyncEvent \_ Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    Generato prima che WMI [**chiami IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) nel provider.

-   [**Msft \_ WmiProvider \_ ExecMethodAsyncEvent \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    Generato dopo che WMI chiama [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) nel provider.

La procedura seguente illustra come risolvere i problemi di esecuzione dell'applicazione.

**Per configurare la risoluzione dei problemi WMI**

1.  Creare e compilare un file MOF per usare il consumer di eventi di registrazione WMI.
2.  Eseguire l'applicazione client.
3.  Visualizzare il file di log per la risoluzione dei problemi relativi a tutti gli eventi di operazione ed errore del provider e analizzare il log per diagnosticare i problemi del client riscontrati.

Un altro approccio per la risoluzione dei problemi consiste nel visualizzare l'elenco dei provider attualmente presenti nella cache del computer enumerando i provider [**MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) nello spazio **dei nomi \\ cimv2** radice. In questa classe sono disponibili metodi che consentono di caricare e scaricare provider a scopo di debug o installazione.

Nell'esempio di codice seguente viene utilizzato il consumer di eventi di registrazione WMI per acquisire tutti gli eventi della classe di evento padre, acquisendo così tutti gli eventi dell'operazione del provider.

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

Quando i messaggi di errore indicano un errore di caricamento del provider, usare [**\_ MSFT WmiProvider \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) per identificare il provider che ha causato l'errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi di WMI](wmi-troubleshooting.md)
</dt> <dt>

[Classi per la risoluzione dei problemi WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
