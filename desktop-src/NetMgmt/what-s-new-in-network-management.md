---
title: Novità della gestione della rete
description: Novità della gestione della rete
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e688d340b8282015b99ccb3d7fa6404dfa332748
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104399909"
---
# <a name="whats-new-in-network-management"></a>Novità della gestione della rete

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

In Microsoft Windows 8 sono state introdotte nuove funzionalità di programmazione per la gestione della rete. Questi nuovi elementi estendono le funzionalità di gestione della rete per creare pacchetti di provisioning per operazioni di aggiunta a un dominio offline quando si effettua il provisioning dei computer con Windows 8.

Di seguito sono riportate le nuove funzioni di gestione della rete:

-   [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

Di seguito sono riportate le nuove strutture di gestione della rete:

-   [**\_parametri di PROvisioning di Netsetup \_**](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [**\_Informazioni utente \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

La funzione [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) è stata migliorata in Windows 8 per supportare un nuovo livello di informazioni e restituire una struttura [**\_ Info utente \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) con le informazioni sull'account utente per un account connesso a un'identità Internet.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

In Microsoft Windows 7 sono state introdotte nuove funzionalità di programmazione per la gestione della rete. Questi elementi estendono le funzionalità di gestione della rete per consentire operazioni di aggiunta a un dominio offline durante il provisioning dei computer con Windows 7.

Di seguito sono riportate le nuove funzioni di gestione della rete:

-   [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

Le funzioni di gestione di rete esistenti seguenti sono state migliorate per supportare opzioni aggiuntive:

-   [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a>Windows Server 2003

Microsoft Windows Server 2003 introduce nuove funzionalità di programmazione per la gestione della rete. Questi elementi estendono le funzionalità delle operazioni di gestione della rete in Windows Server 2003 e versioni successive.

## <a name="windows-xp"></a>Windows XP

In Microsoft Windows XP sono state introdotte nuove funzionalità di programmazione per la gestione della rete. Questi elementi estendono le funzionalità di gestione della rete in Windows XP e versioni successive.

Di seguito sono riportate le nuove funzioni di gestione della rete:

-   [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




