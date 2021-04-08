---
description: Microsoft&\# 160; Il provider Win32 recupera e aggiorna i dati rilevanti per i sistemi Windows&\# 8212, dati quali le impostazioni correnti delle variabili di ambiente e gli attributi di un disco logico.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Provider Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747903"
---
# <a name="win32-provider"></a>Provider Win32

Il provider Microsoft Win32 recupera e aggiorna i dati rilevanti per i sistemi Windows: dati quali le impostazioni correnti delle variabili di ambiente e gli attributi di un disco logico. Con il provider Win32, le applicazioni di gestione possono utilizzare WMI per accedere facilmente a questi dati. Il provider Win32 recupera le informazioni effettuando chiamate di funzioni Windows ed eseguendo query sul Registro di sistema.

Il provider Win32 definisce le classi utilizzate per descrivere l'hardware o il software disponibile nei sistemi Windows e le relazioni tra di essi.

Come provider di istanze e di metodi, il provider Win32 implementa l'interfaccia [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) standard, oltre ai metodi [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) seguenti:

-   [**CreateInstanceEnumAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**DeleteInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [**ExecMethodAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

Nella tabella seguente sono elencate le categorie di classi del provider Win32.



| Classi                                                                             | Descrizione                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Classi hardware del sistema del computer](computer-system-hardware-classes.md)<br/> | Oggetti correlati all'hardware.<br/>                                      |
| [Classi del sistema operativo](operating-system-classes.md)<br/>                 | Oggetti correlati al sistema operativo.<br/>                              |
| [Classi del contatore delle prestazioni](performance-counter-classes.md)<br/>           | Dati sulle prestazioni non elaborati e calcolati dai contatori delle prestazioni.<br/> |
| [Classi di gestione del servizio WMI](wmi-service-management-classes.md)<br/>     | Gestione per WMI.<br/>                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI CIMWin32](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
