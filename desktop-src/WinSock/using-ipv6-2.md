---
description: In Windows XP in un secondo momento viene fornito un nuovo strumento da riga di comando per la configurazione e la gestione di IPv4. Questo strumento usa il comando &\# 0034;netsh interface ip&0034; per la configurazione e la gestione \# di IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Utilizzo di IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 675441d1ae18e287541ad4c354aca19c3779fb14f3630ac1636cd360024fcd31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559207"
---
# <a name="using-ipv6"></a>Utilizzo di IPv6

In Windows XP in un secondo momento viene fornito un nuovo strumento da riga di comando per la configurazione e la gestione di IPv4. Questo strumento usa il comando "netsh interface ip" per la configurazione e la gestione di IPv4.

In Windows XP con Service Pack 1 (SP1) e versioni successive, questo nuovo strumento da riga di comando è stato migliorato per supportare la configurazione e la gestione di IPv6. Questo strumento avanzato è il comando "netsh interface ipv6". Le modifiche di configurazione apportate Netsh.exe comandi sono permanenti e non vengono perse al riavvio del computer o del protocollo IPv6.

Il comando seguente è disponibile in Windows XP con SP1 e versioni successive per eseguire query e configurare IPv6 in un computer locale:

-   [Netsh.exe](netsh-exe.md)

Prima di Windows XP con Service Pack 1 (SP1), la configurazione e la gestione IPv6 usava diversi strumenti da riga di comando meno recenti per configurare e gestire IPv6. Usando questi strumenti precedenti, le modifiche IPv6 non sono permanenti e vengono perse quando il computer o il protocollo IPv6 è stato riavviato.

I comandi precedenti seguenti sono disponibili in Windows XP

-   [Net.exe](net-exe-2.md)
-   [Ipv6.exe](ipv6-exe-2.md)
-   [Ipsec6.exe](ipsec6-exe-2.md)

Questi strumenti meno recenti sono stati forniti anche in IPv6 Technology Preview per Windows 2000

Le modifiche di configurazione che usano questi strumenti meno recenti possono essere mantenute inserendole come righe di comando in un file di script di comando (con estensione cmd) eseguito dopo il riavvio del computer o del protocollo IPv6. Per ripristinare automaticamente le modifiche di configurazione dopo il riavvio, è possibile usare il Windows Attività pianificate per eseguire il file con estensione cmd all'avvio del computer.

Questi strumenti meno recenti non sono disponibili in Windows Server 2003 e versioni successive. Lo strumento "netsh interface ipv6" viene fornito per la configurazione e la gestione di IPv6 dalla riga di comando in Windows Server 2003 e versioni successive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protocollo Internet versione 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Guida IPv6 per applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[IPv6 Technology Preview per Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



