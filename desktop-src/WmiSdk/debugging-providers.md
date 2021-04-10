---
description: I provider, a meno che non siano provider disaccoppiati in esecuzione all'interno di un'applicazione, vengono caricati in un processo di Wmiprvse.exe e non tramite Svchost.exe con un processo di Winmgmt.exe. Per altre informazioni, vedere Hosting e sicurezza del provider.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Provider di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967130"
---
# <a name="debugging-providers"></a>Provider di debug

I provider, a meno che non siano [*provider disaccoppiati*](gloss-d.md) in esecuzione all'interno di un'applicazione, vengono caricati in un processo di Wmiprvse.exe e non tramite Svchost.exe con un processo di Winmgmt.exe. Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).

Quando si arresta in corrispondenza di un punto di interruzione, il debugger di Visual Studio blocca l'intero processo host del provider, che in genere è l'host condiviso Wmiprvse.exe. In questo modo si impedisce il funzionamento di tutti gli altri componenti ospitati in tale processo, inclusa l'estensione WMI Esplora server. Sono bloccate anche le applicazioni client che eseguono chiamate al provider. I problemi che risultano peggiorano in Windows 2000 e versioni precedenti perché il provider viene caricato nel processo del servizio WMI (Winmgmt.exe).

Se si esegue WMI Esplora server in un'altra istanza, l'IDE di Visual Studio non viene bloccato ed è possibile rilasciare il punto di interruzione. Si consiglia di eseguire il provider in un processo di hosting distinto durante la fase di sviluppo, in modo che l'arresto in corrispondenza di un punto di interruzione blocchi solo il processo che ospita il provider. Le altre funzioni di WMI continuano a essere accessibili a WMI Esplora server e a qualsiasi altro script o applicazione basata su WMI. Inoltre, se il provider si arresta in modo anomalo, non influisce sul funzionamento di altri provider caricati nello stesso processo host.

Per eseguire il caricamento del provider nel proprio processo host, modificare la registrazione del provider per impostare la proprietà [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) su Where il provider `NetworkServiceHost:[MyProvider]` può essere qualsiasi stringa che identifichi in modo univoco il provider. Usare, ad esempio, il valore **\_ \_ Win32Provider. CLSID** . Quando il provider è pronto per la spedizione, restituire **\_ \_ Win32Provider. HostingModel** al valore previsto, ad esempio **NetworkServiceHost**.

Se non si esegue il debug del caricamento del provider, è possibile chiamare il [**metodo Load della \_ classe Providers MSFT**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) per forzare il caricamento del provider, quindi connettersi al processo di Wmiprvse.exe con la dll caricata ed eseguire il debug in base alle esigenze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> <dt>

[Classi di risoluzione dei problemi WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
