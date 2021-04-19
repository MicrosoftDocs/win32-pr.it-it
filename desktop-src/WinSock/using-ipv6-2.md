---
description: In Windows XP a versioni successive viene fornito un nuovo strumento da riga di comando per la configurazione e la gestione di IPv4. Questo strumento usa il \# comando &0034; netsh interface ip&\# 0034; per la configurazione e la gestione di IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Utilizzo di IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317608"
---
# <a name="using-ipv6"></a>Utilizzo di IPv6

In Windows XP a versioni successive viene fornito un nuovo strumento da riga di comando per la configurazione e la gestione di IPv4. Questo strumento usa il comando "netsh interface IP" per la configurazione e la gestione di IPv4.

In Windows XP con Service Pack 1 (SP1) e versioni successive, questo nuovo strumento da riga di comando è stato migliorato per supportare la configurazione e la gestione di IPv6. Questo strumento avanzato è il comando "netsh interface IPv6". Le modifiche di configurazione apportate utilizzando i comandi Netsh.exe sono permanenti e non vengono perse quando il computer o il protocollo IPv6 viene riavviato.

Il seguente comando è disponibile in Windows XP con SP1 e versioni successive per eseguire query e configurare IPv6 in un computer locale:

-   [Netsh.exe](netsh-exe.md)

Prima di Windows XP con Service Pack 1 (SP1), la configurazione e la gestione di IPv6 usavano diversi strumenti della riga di comando precedenti per la configurazione e la gestione di IPv6. Utilizzando questi strumenti obsoleti, le modifiche IPv6 non sono permanenti e vengono perse quando il computer o il protocollo IPv6 è stato riavviato.

I comandi precedenti seguenti sono disponibili in Windows XP

-   [Net.exe](net-exe-2.md)
-   [Ipv6.exe](ipv6-exe-2.md)
-   [Ipsec6.exe](ipsec6-exe-2.md)

Questi strumenti meno recenti erano disponibili anche nella versione di anteprima della tecnologia IPv6 per Windows 2000

Le modifiche di configurazione che utilizzano questi strumenti meno recenti possono essere gestite inserendole come righe di comando in un file script di comando (con estensione cmd) che viene eseguito dopo il riavvio del computer o del protocollo IPv6. Per ripristinare automaticamente le modifiche alla configurazione dopo il riavvio, è possibile utilizzare le attività pianificate di Windows per eseguire il file con estensione cmd all'avvio del computer.

Questi strumenti meno recenti non sono disponibili in Windows Server 2003 e versioni successive. Lo strumento "netsh interface IPv6" viene fornito per la configurazione e la gestione di IPv6 dalla riga di comando in Windows Server 2003 e versioni successive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protocollo IP versione 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Guida a IPv6 per le applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Anteprima della tecnologia IPv6 per Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



