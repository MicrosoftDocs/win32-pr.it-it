---
description: Non è possibile utilizzare le funzioni di backup e ripristino Certadm.dll per eseguire il backup delle chiavi private dei servizi certificati.
ms.assetid: 27ee8caa-8f5e-46dc-b55d-afde5471507e
title: Backup e ripristino della chiave privata dei servizi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 891794f36e87b2aa4b6a5d5c8dde55304da20601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307700"
---
# <a name="backing-up-and-restoring-the-certificate-services-private-key"></a>Backup e ripristino della chiave privata dei servizi certificati

Non è possibile utilizzare le funzioni di backup e ripristino Certadm.dll per eseguire il backup delle [*chiavi private*](../secgloss/p-gly.md)dei servizi certificati. Non è possibile eseguire il backup delle chiavi private da queste funzioni perché queste funzioni sono progettate per eseguire il backup e il ripristino del database dei servizi certificati (e dei file correlati) e il database non contiene chiavi private (anche per i certificati autofirmati).

Per eseguire il backup di una chiave privata di Servizi certificati, utilizzare lo snap-in MMC Autorità di certificazione o il comando certutil (con-backup o-backupkey specificato). Il backup della chiave privata con lo snap-in MMC dell'autorità di certificazione o certutil comporta la scrittura della chiave privata nel \# file PKCS 12. Anche se il \# file PKCS 12 è protetto da password, deve essere considerato estremamente sensibile e deve essere archiviato in modo sicuro. la password per il \# file PKCS 12 deve anche essere sorvegliata da persone non autorizzate.

Analogamente, le chiavi private non possono essere ripristinate dalle funzioni di backup e ripristino di Servizi certificati. Una chiave di backup di Servizi certificati contenuta in un \# file PKCS 12 può essere ripristinata dallo snap-in MMC dell'autorità di certificazione o dal comando certutil (specificando i verbi-Restore o-restorekey); si noti che l'utente che esegue l'operazione di ripristino dovrà essere a conoscenza della password per il \# file PKCS 12.

Esistono solo due casi in cui è necessario eseguire il backup di una chiave privata di Servizi certificati. Il primo caso è dopo l'installazione di Servizi certificati. Il secondo caso è dopo qualsiasi operazione di rinnovo del certificato di Servizi certificati.

 

 
