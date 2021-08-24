---
title: Installazione del provider
description: La procedura per l'installazione del provider WMI DNS è diversa in base alla versione Windows in cui è installato.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Domain Name System, provider WMI, installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9b4b976ccb1a600f56042cb75b500577335059966a82dbb1f9e77b04f7a4df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693041"
---
# <a name="installing-the-provider"></a>Installazione del provider

La procedura per l'installazione del provider WMI DNS è diversa in base alla versione Windows in cui è installato. La procedura seguente descrive come installare e configurare il provider WMI DNS in Windows 2000. Per ottenere il provider WMI DNS per Windows 2000, scaricare il file seguente:

**AVVISO:** I file del provider WMI DNS non sono intercambiabili. Windows server DNS 2000 richiedono file diversi e una procedura diversa rispetto ai server DNS Windows Server 2003. Viene fornita la procedura per ogni .

**Per installare il provider WMI DNS in Windows 2000 Server**

1.  Ottenere il provider WMI DNS per Windows 2000 da Windows 2000 Server Resource Kit oppure scaricare il file Dnsprov.zip da: ftp://ftp.microsoft.com/reskit/win2000/
2.  Copiare i file DNS WMI Provider (Dnsprov.dll) e Dnsschema.mof nella <winntdir> \\ directory system32 \\ wbem.
3.  Compilare il file MOF. In questo modo lo schema viene personalizzato in modo che corrisponda al server.

    **mofcomp dnsschema.mof**

4.  Registrare la DLL nel server DNS.

    **regsvr32 dnsprov.dll**

5.  È quindi possibile utilizzare script o programmi che utilizzano il provider WMI DNS per gestire i server DNS. Gli script o i programmi possono essere eseguiti dal server DNS o da un computer client.
    > [!Note]  
    > WMI SDK non è necessario per eseguire il provider WMI DNS, ma contiene molti strumenti utili.

     

Il provider WMI DNS deve essere installato in qualsiasi server DNS da gestire. Gli script DNS, tuttavia, possono essere eseguiti nel server DNS o in un host remoto.

**Per installare il provider WMI DNS in Windows Server 2003**

-   Per Windows server 2003, il provider WMI DNS viene installato e registrato automaticamente e il relativo file MOF viene compilato quando viene installato il servizio Server DNS.

 

 




