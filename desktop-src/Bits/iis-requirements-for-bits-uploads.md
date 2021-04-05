---
title: Requisiti di IIS per i caricamenti BITS
description: Per i caricamenti, BITS richiede IIS 6,0 in Windows Server 2003 e IIS 7,0 su Windows Server 2008; BITS non supporta IIS 5,1 in Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708119"
---
# <a name="iis-requirements-for-bits-uploads"></a>Requisiti di IIS per i caricamenti BITS

Per i caricamenti, BITS richiede IIS 6,0 in Windows Server 2003 e IIS 7,0 su Windows Server 2008; BITS non supporta IIS 5,1 in Windows XP. È necessario abilitare la directory virtuale IIS per i caricamenti e configurare le estensioni IIS BITS.

**Installazioni di base di Windows Server:** Le estensioni IIS BITS non sono supportate.

In Windows Server 2008, utilizzare il **Server Manager** per installare la funzionalità estensioni server BITS. Dal **Server Manager** fare clic su **funzionalità** nel riquadro sinistro. Nell' **Aggiunta guidata funzionalità**, controllare le estensioni del server BITS. Si noti che è necessario installare i ruoli di compatibilità di gestione con IIS 6.

In Windows Server 2003, utilizzare la **procedura guidata componenti di Windows** per installare l'estensione del server BITS. Nel **Pannello di controllo** selezionare **Installazione applicazioni**. Selezionare quindi **Aggiungi/Rimuovi componenti di Windows** per visualizzare la **procedura guidata componenti di Windows**. L'estensione del server BITS è un sottocomponente di Internet Information Services (IIS), che è un componente secondario del server applicazioni Web.

> [!Note]  
> Se il servizio IISAdmin viene riavviato, il processo di lavoro IIS deve essere riciclato prima che il servizio BITS possa riprendere i caricamenti. È possibile riciclare manualmente il processo di lavoro IIS utilizzando l'utilità della riga di comando **IISReset.exe** .

 

Per informazioni sulla configurazione di IIS per il caricamento, vedere [configurazione del server per il caricamento](setting-up-the-server-for-uploads.md).

Per informazioni dettagliate sulle proprietà aggiunte da BITS a IIS, vedere [BITS Server Settings for upload Jobs](bits-server-settings-for-upload-jobs.md).

 

 




