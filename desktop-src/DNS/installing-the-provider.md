---
title: Installazione del provider
description: La procedura per l'installazione del provider WMI DNS varia a seconda della versione di Windows in cui è installata.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Domain Name System, provider WMI, installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708647"
---
# <a name="installing-the-provider"></a>Installazione del provider

La procedura per l'installazione del provider WMI DNS varia a seconda della versione di Windows in cui è installata. Nella procedura seguente viene descritto come installare e configurare il provider WMI DNS in Windows 2000. Per ottenere il provider WMI DNS per Windows 2000, scaricare il file seguente:

**Avviso:** I file del provider WMI DNS non sono intercambiabili. I server DNS di Windows 2000 richiedono file diversi e una procedura diversa rispetto ai server DNS di Windows Server 2003. Viene fornita la procedura per ogni.

**Per installare il provider WMI DNS in Windows Server 2000**

1.  Ottenere il provider WMI DNS per Windows 2000 dal Resource Kit di Windows 2000 Server oppure scaricare il file Dnsprov.zip da: ftp://ftp.microsoft.com/reskit/win2000/
2.  Copiare i file del provider WMI DNS (Dnsprov.dll) e Dnsschema. mof nella <winntdir> \\ \\ directory WBEM di system32.
3.  Compilare il file MOF. Questa operazione consente di personalizzare lo schema in modo che corrisponda al server.

    **mofcomp Dnsschema. mof**

4.  Registrare la DLL nel server DNS.

    **regsvr32 dnsprov.dll**

5.  È possibile utilizzare script o programmi che utilizzano il provider WMI DNS per gestire i server DNS. Gli script o i programmi possono essere eseguiti dal server DNS o da un computer client.
    > [!Note]  
    > WMI SDK non è necessario per eseguire il provider WMI DNS, ma contiene molti strumenti utili.

     

Il provider WMI DNS deve essere installato in qualsiasi server DNS da gestire; gli script DNS, tuttavia, possono essere eseguiti nel server DNS o in un host remoto.

**Per installare il provider WMI DNS in Windows Server 2003**

-   Per i sistemi operativi Windows Server 2003, il provider WMI DNS viene installato e registrato automaticamente e il relativo file MOF viene compilato quando viene installato il servizio server DNS.

 

 




