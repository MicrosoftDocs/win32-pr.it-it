---
title: Backup e ripristino di un server di Active Directory
description: Active Directory Domain Services forniscono funzioni per il backup e il ripristino dei dati nel database di directory.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, utilizzo, backup e ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724650"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a>Backup e ripristino di un server di Active Directory

Active Directory Domain Services forniscono funzioni per il backup e il ripristino dei dati nel database di directory. In questa sezione viene descritto come [eseguire il backup](backing-up-an-active-directory-server.md) e il [ripristino](restoring-an-active-directory-server.md) di un server Active Directory. Per ulteriori informazioni sul backup di un server di Active Directory utilizzando le utilità disponibili nei sistemi operativi Windows 2000 e Windows Server 2003, vedere il Resource Kit applicabile, disponibile sul sito Web Microsoft TechNet.

Il backup di un server di Active Directory deve essere eseguito online e deve essere eseguito durante l'installazione del Active Directory Domain Services. Active Directory Domain Services si basano su un database speciale ed esporta un set di funzioni di backup che forniscono l'interfaccia di backup a livello di codice. Il backup non supporta i backup incrementali. Un'applicazione di backup viene associata a una DLL sul lato client locale con i punti di ingresso definiti in ntdsbcli. h.

Il ripristino di un server di Active Directory viene sempre eseguito offline.

Sebbene gli argomenti di questa sezione descrivano solo come eseguire il backup e il ripristino di un server di Active Directory, tenere presente che Windows 2000 e i sistemi operativi Windows Server 2003 hanno diversi componenti "stato del sistema" che devono essere sottoposti a backup e ripristinati insieme. Questi componenti di stato del sistema sono costituiti da:

-   File di avvio, ad esempio Ntldr, Ntdetect, tutti i file protetti da SFP e la configurazione del contatore delle prestazioni
-   Controller di Dominio di Active Directory
-   SysVol (solo controller di dominio)
-   Server di certificazione (solo CA)
-   Database cluster (solo nodo cluster)
-   Registro
-   Database di registrazione della classe COM+

È possibile eseguire il backup dello stato del sistema in qualsiasi ordine, ma il ripristino dello stato del sistema deve essere eseguito nell'ordine seguente:

1.  Ripristinare i file di avvio.
2.  Ripristinare SysVol, server di certificati, database cluster e database di registrazione della classe COM+, come applicabile.
3.  Ripristinare il server Active Directory.
4.  Ripristinare il registro di sistema.

Per ulteriori informazioni sul backup e il ripristino di Servizi certificati, vedere [utilizzo delle funzioni di backup e ripristino di Servizi certificati](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).

Per ulteriori informazioni sul backup e il ripristino di Active Directory Domain Services, vedere:

-   [Considerazioni per il backup Active Directory Domain Services](considerations-for-active-directory-domain-services-backup.md)
-   [Esecuzione del backup di un server di Active Directory](backing-up-an-active-directory-server.md)
-   [Ripristino di un server di Active Directory](restoring-an-active-directory-server.md)
-   [Funzioni di backup della directory](directory-backup-functions.md)

 

 