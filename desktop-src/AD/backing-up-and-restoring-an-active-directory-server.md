---
title: Backup e ripristino di un server Active Directory
description: Active Directory Domain Services funzioni per il backup e il ripristino dei dati nel database della directory.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, uso, backup e ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1955c70daed8cfaed0f5afe6c498a599aebb30f5d7b1846442d22cf84e9634e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024158"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a>Backup e ripristino di un server Active Directory

Active Directory Domain Services funzioni per il backup e il ripristino dei dati nel database della directory. Questa sezione descrive come eseguire [il backup e](backing-up-an-active-directory-server.md) il ripristino di [un](restoring-an-active-directory-server.md) server Active Directory. Per altre informazioni sul backup di un server Active Directory usando le utilità fornite nei sistemi operativi Windows 2000 e Windows Server 2003, vedere il Resource Kit applicabile, disponibile nel sito Web Microsoft TechNet.

Il backup di un server Active Directory deve essere eseguito online e deve essere eseguito quando Active Directory Domain Services installati. Active Directory Domain Services si basano su un database speciale ed esportano un set di funzioni di backup che forniscono l'interfaccia di backup a livello di codice. Il backup non supporta i backup incrementali. Un'applicazione di backup esegue il binding a una DLL sul lato client locale con i punti di ingresso definiti in Ntdsbcli.h.

Il ripristino di un server Active Directory viene sempre eseguito offline.

Anche se negli argomenti di questa sezione viene descritto solo come eseguire il backup e il ripristino di un server Active Directory, tenere presente che Windows 2000 e i sistemi operativi Windows Server 2003 hanno diversi componenti "stato del sistema" che devono essere sottoposti a backup e ripristino insieme. Questi componenti dello stato del sistema sono costituiti da:

-   File di avvio come ntldr, ntdetect, tutti i file protetti da SFP e la configurazione dei contatori delle prestazioni
-   Controller Dominio di Active Directory
-   SysVol (solo controller di dominio)
-   Server dei certificati (solo CA)
-   Database del cluster (solo nodo del cluster)
-   Registro
-   Database di registrazione della classe COM+

È possibile eseguire il backup dello stato del sistema in qualsiasi ordine, ma il ripristino dello stato del sistema deve essere eseguito nell'ordine seguente:

1.  Ripristinare i file di avvio.
2.  Ripristinare SysVol, Il server di certificati, il database cluster e il database di registrazione della classe COM+, se applicabile.
3.  Ripristinare il server Active Directory.
4.  Ripristinare il Registro di sistema.

Per altre informazioni sul backup e il ripristino di Servizi certificati, vedere [Uso delle funzioni di backup e](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions)ripristino di Servizi certificati .

Per altre informazioni sul backup e il ripristino di Active Directory Domain Services, vedere:

-   [Considerazioni per il Active Directory Domain Services backup](considerations-for-active-directory-domain-services-backup.md)
-   [Backup di un server Active Directory](backing-up-an-active-directory-server.md)
-   [Ripristino di un server Active Directory](restoring-an-active-directory-server.md)
-   [Funzioni di backup della directory](directory-backup-functions.md)

 

 