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
# <a name="troubleshooting-wmi-client-applications"></a><span data-ttu-id="d9c24-103">Risoluzione dei problemi relativi alle applicazioni client WMI</span><span class="sxs-lookup"><span data-stu-id="d9c24-103">Troubleshooting WMI Client Applications</span></span>

<span data-ttu-id="d9c24-104">WMI contiene un set di classi per la [risoluzione dei problemi relativi](wmi-troubleshooting-classes.md) alle applicazioni client che utilizzano provider WMI.</span><span class="sxs-lookup"><span data-stu-id="d9c24-104">WMI contains a set of classes for [troubleshooting](wmi-troubleshooting-classes.md) client applications that use WMI providers.</span></span> <span data-ttu-id="d9c24-105">Le classi di evento per la risoluzione dei problemi sono associate alle classi di evento WMI, in modo che sia possibile tenere traccia dell'esecuzione dell'applicazione usando un log degli eventi di risoluzione dei problemi acquisiti.</span><span class="sxs-lookup"><span data-stu-id="d9c24-105">The troubleshooting event classes are coupled to WMI event classes, such that you can track your application execution using a log of captured troubleshooting events.</span></span>

<span data-ttu-id="d9c24-106">Nell'elenco seguente sono riportati alcuni esempi di classi di evento per la risoluzione dei problemi:</span><span class="sxs-lookup"><span data-stu-id="d9c24-106">The following list contains examples of troubleshooting event classes:</span></span>

-   [<span data-ttu-id="d9c24-107">**MSFT \_ provider WMI \_ ExecMethodAsyncEvent \_ pre**</span><span class="sxs-lookup"><span data-stu-id="d9c24-107">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Pre**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    <span data-ttu-id="d9c24-108">Generato prima che WMI chiami [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) nel provider.</span><span class="sxs-lookup"><span data-stu-id="d9c24-108">Raised before WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

-   [<span data-ttu-id="d9c24-109">**\_Post provider WMI \_ ExecMethodAsyncEvent \_ MSFT**</span><span class="sxs-lookup"><span data-stu-id="d9c24-109">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Post**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    <span data-ttu-id="d9c24-110">Generato dopo la chiamata di WMI [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) nel provider.</span><span class="sxs-lookup"><span data-stu-id="d9c24-110">Raised after WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

<span data-ttu-id="d9c24-111">Nella procedura seguente viene illustrato come risolvere i problemi relativi all'esecuzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d9c24-111">The following procedure shows how to troubleshoot application execution.</span></span>

<span data-ttu-id="d9c24-112">**Per configurare la risoluzione dei problemi WMI**</span><span class="sxs-lookup"><span data-stu-id="d9c24-112">**To set up WMI troubleshooting**</span></span>

1.  <span data-ttu-id="d9c24-113">Creazione e compilazione di un file MOF per l'utilizzo del consumer di eventi di registrazione WMI.</span><span class="sxs-lookup"><span data-stu-id="d9c24-113">Create and compile a MOF file to use the WMI logging event consumer.</span></span>
2.  <span data-ttu-id="d9c24-114">Eseguire l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="d9c24-114">Run your client application.</span></span>
3.  <span data-ttu-id="d9c24-115">Consente di visualizzare il file di log per la risoluzione dei problemi relativi a tutti gli eventi di errore e di operazione del provider e analizzare il log per diagnosticare i problemi del client che si stanno riscontrando.</span><span class="sxs-lookup"><span data-stu-id="d9c24-115">View the troubleshooting log file for all provider operation and failure events, and analyze the log to diagnose the client problems you are encountering.</span></span>

<span data-ttu-id="d9c24-116">Un altro approccio per la risoluzione dei problemi consiste nel visualizzare l'elenco dei provider attualmente presenti nella cache del computer, enumerando i [**\_ provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) nello spazio dei nomi **\\ CIMV2 radice** .</span><span class="sxs-lookup"><span data-stu-id="d9c24-116">Another troubleshooting approach is to view the list of providers currently in the computer cache, by enumerating [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="d9c24-117">In questa classe sono disponibili metodi che consentono di caricare e scaricare i provider a scopo di debug o di installazione.</span><span class="sxs-lookup"><span data-stu-id="d9c24-117">There are methods in this class that enable you to load and unload providers for debugging or setup purposes.</span></span>

<span data-ttu-id="d9c24-118">Nell'esempio di codice seguente viene utilizzato il consumer di eventi di registrazione WMI per acquisire tutti gli eventi della classe di evento Parent, acquisendo quindi tutti gli eventi di operazione del provider.</span><span class="sxs-lookup"><span data-stu-id="d9c24-118">The following code example uses the WMI logging event consumer to capture all events of the parent event class, thus capturing all provider operation events.</span></span>

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

<span data-ttu-id="d9c24-119">Quando i messaggi di errore indicano un errore di caricamento del provider, utilizzare [**MSFT \_ provider WMI \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) per identificare il provider che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="d9c24-119">When error messages indicate provider load failure, use [**MSFT\_WmiProvider\_LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) to identify which provider caused the fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9c24-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9c24-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9c24-121">Risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="d9c24-121">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="d9c24-122">Classi di risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="d9c24-122">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
