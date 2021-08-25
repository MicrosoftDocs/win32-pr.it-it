---
description: Non è possibile usare le Certadm.dll di backup e ripristino per eseguire il backup delle chiavi private di Servizi certificati.
ms.assetid: 27ee8caa-8f5e-46dc-b55d-afde5471507e
title: Backup e ripristino della chiave privata di Servizi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65b8c25e627e516d92b8dc8219db9c7933bd8d9902b1f75bea204d723edd61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879781"
---
# <a name="backing-up-and-restoring-the-certificate-services-private-key"></a>Backup e ripristino della chiave privata di Servizi certificati

Non è possibile usare le Certadm.dll di backup e ripristino per eseguire il backup delle chiavi [*private di*](../secgloss/p-gly.md)Servizi certificati . Queste funzioni non possono eseguire il backup delle chiavi private perché queste funzioni sono destinate al backup e al ripristino del database di Servizi certificati (e dei file correlati) e questo database non contiene chiavi private (anche per i certificati autoemessi).

Per eseguire il backup di una chiave privata di Servizi certificati, usare lo snap-in MMC Autorità di certificazione o il comando certutil (con -backup o -backupkey specificato). Il backup della chiave privata con lo snap-in MMC autorità di certificazione o certutil comporta la scrittura della chiave privata nel file PKCS \# 12. Anche se questo file PKCS 12 è protetto da password, deve essere considerato estremamente sensibile e deve essere archiviato in modo sicuro. Anche la password per il \# file PKCS 12 deve essere protetta da utenti non \# autorizzati.

Analogamente, le chiavi private non possono essere ripristinate dalle funzioni di backup e ripristino di Servizi certificati. Una chiave di backup di Servizi certificati contenuta in un file PKCS 12 può essere ripristinata dallo snap-in MMC autorità di certificazione o dal comando certutil (specificando i verbi -restore o -restorekey); si noti che l'utente che esegue l'operazione di ripristino dovrà conoscere la password per il \# file PKCS \# 12.

Esistono solo due casi in cui è necessario eseguire il backup di una chiave privata di Servizi certificati. Il primo caso è dopo l'installazione di Servizi certificati. Il secondo caso è dopo qualsiasi operazione di rinnovo del certificato di Servizi certificati.

 

 
