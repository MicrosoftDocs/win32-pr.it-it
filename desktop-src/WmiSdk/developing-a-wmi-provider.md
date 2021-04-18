---
description: Un provider è un oggetto Component Object Model (COM) che funge da intermediario tra WMI e un oggetto gestito.
ms.assetid: a4f537ba-9081-43b4-acff-4d206de3d9d7
ms.tgt_platform: multiple
title: Sviluppo di un provider WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9249c251f75f08f9e5142e70a507b0dced8f91df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310373"
---
# <a name="developing-a-wmi-provider"></a>Sviluppo di un provider WMI

Un provider è un oggetto Component Object Model (COM) che funge da intermediario tra WMI e un oggetto gestito. Ad esempio, quando un'applicazione o uno script richiede dati del disco utilizzando la classe WMI [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , i dati vengono ottenuti in modo dinamico tramite il [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider)preinstallato.

Se si desidera fornire dati tramite WMI ad altre applicazioni, è possibile creare un provider di codice non gestito scrivendo un server COM o tramite le **procedure guidate di WMI ATL** in Visual Studio. È possibile scrivere un provider di codice gestito utilizzando WMI nel .NET Framework. Negli argomenti di questa sezione viene descritto il processo di scrittura di un provider COM non gestito.

> [!Note]  
> Per assicurarsi che tutte le definizioni delle classi WMI per gli oggetti gestiti vengano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e viene riavviato, usare l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) nel file Managed Object Format (MOF).

 

Un provider è costituito da classi definite nello schema [*Managed Object Format (MOF)*](gloss-m.md) e da un file dll che esegue le funzioni del provider. Ad esempio, il file MOF che definisce le classi del provider Win32 è CIMWin32. mof e la DLL è CIMWin32.dll, entrambi sono presenti in% windir% \\ system32 \\ WBEM.

Lo schema MOF per il provider può contenere diversi tipi di provider. Ad esempio, il [provider di log eventi](/previous-versions/windows/desktop/eventlogprov/event-log-provider) dispone di tipi di istanza, metodo e provider di eventi in un file MOF denominato ntevt. mof. È consigliabile che tutte le classi e lo schema di registrazione per i provider correlati vengano assemblati in un unico file, anziché creare un file per classe.

Oltre a usare i provider preinstallati, è possibile creare un provider personalizzato per fornire informazioni su un dispositivo hardware o sulle operazioni del software.

Nella tabella seguente sono elencate le attività di base per la creazione di un provider.



| Attività                                                                                                                                                            | Descrizione                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)                                                              | Sviluppare un modello per le entità che si desidera gestire tramite WMI e creare un file di Managed Object Format (MOF) per descrivere lo schema.<br/> |
| [Fornire dati a WMI scrivendo un provider](supplying-data-to-wmi-by-writing-a-provider.md)                                                                  | Creare il provider più elementare associato a WMI.<br/>                                                                                |
| [Incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md)                                                                    | Includere il provider come componente all'interno di un'applicazione, se non viene eseguito in qualsiasi momento.<br/>                                         |
| [Registrazione di un provider](registering-a-provider.md)                                                                                                            | Registrare il provider con COM e WMI.<br/>                                                                                               |
| [Inizializzazione di un provider](initializing-a-provider.md)                                                                                                          | Implementare le interfacce [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .<br/>   |
| [Esecuzione di chiamate a WMI](making-calls-to-wmi.md)                                                                                                                  | Chiamare le interfacce WMI da un provider.<br/>                                                                                                  |
| [Rappresentazione di un client](impersonating-a-client.md)                                                                                                            | Impostare la sicurezza per accedere a un'applicazione client.<br/>                                                                                          |
| [Aggiornamento di un provider](updating-a-provider.md)                                                                                                                  | Migliorare il provider in base alle esigenze.<br/>                                                                                                       |
| [Scaricamento di un provider](unloading-a-provider.md)                                                                                                                | Rimuovere il provider dalla memoria durante l'arresto o quando il provider è inattivo.<br/>                                                         |
| [Provider di debug](debugging-providers.md) e [classi di risoluzione dei problemi e configurazione del provider](provider-configuration-and-troubleshooting-classes.md) | Eseguire il debug del provider utilizzando le funzionalità fornite da WMI.<br/>                                                                                 |
| [Ottenere e fornire dati in un computer a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md)                                                          | Valutare se è necessario un provider di compatibilità delle applicazioni a 32 bit o se il provider a 64 bit può fornire dati a entrambi i client.<br/>      |



 

Negli argomenti seguenti vengono illustrati i passaggi necessari per scrivere tipi diversi di provider:

-   [Scrittura di un provider di istanze](writing-an-instance-provider.md)
-   [Scrittura di un provider di metodi](writing-a-method-provider.md)
-   [Scrittura di un provider di eventi](writing-an-event-provider.md)
-   [Scrittura di un provider di consumer di eventi](writing-an-event-consumer-provider.md)
-   [Scrittura di un provider di classi](writing-a-class-provider.md)
-   [Scrittura di un provider di proprietà](writing-a-property-provider.md)
-   [Creazione di un provider di istanze in un provider di High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)

 

