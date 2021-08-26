---
title: Requisiti IIS per i caricamenti BITS
description: Per i caricamenti, BITS richiede IIS 6.0 in Windows Server 2003 e IIS 7.0 in Windows Server 2008; BITS non supporta IIS 5.1 in Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb09ec8c55cce592baf48b4b39faf031e5d6c98909927c0e597be6aaae8712e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004991"
---
# <a name="iis-requirements-for-bits-uploads"></a>Requisiti IIS per i caricamenti BITS

Per i caricamenti, BITS richiede IIS 6.0 in Windows Server 2003 e IIS 7.0 in Windows Server 2008; BITS non supporta IIS 5.1 in Windows XP. La directory virtuale IIS deve essere abilitata per i caricamenti e deve essere configurata l'estensione IIS BITS.

**Installazioni di base di Windows Server:** Le estensioni IIS BITS non sono supportate.

In Windows Server 2008 usare il Server Manager **per** installare la funzionalità Estensioni del server BITS. Da **Server Manager** fare clic **su Funzionalità** nel riquadro sinistro. **Nell'Aggiunta guidata funzionalità** selezionare Estensioni del server BITS. Si noti che è necessario installare i ruoli Compatibilità gestione IIS 6.

In Windows Server 2003 usare l'Windows **guidata** componenti per installare l'estensione del server BITS. In **Pannello di controllo** selezionare **Installazione applicazioni.** Selezionare quindi **Aggiungi/Rimuovi componenti Windows componenti per** visualizzare l'Windows guidata **componenti**. L'estensione del server BITS è un sottocomponente di Internet Information Services (IIS), che è un componente secondario del server applicazioni Web.

> [!Note]  
> Se il servizio IISAdmin viene riavviato, il processo di lavoro IIS deve essere riciclato prima che il servizio BITS possa riprendere i caricamenti. Il processo di lavoro IIS può essere riciclato manualmente usando **l'utilità** IISReset.exedella riga di comando.

 

Per informazioni sulla configurazione di IIS per i caricamenti, vedere [Configurazione del server per i caricamenti](setting-up-the-server-for-uploads.md).

Per informazioni dettagliate sulle proprietà aggiunte da BITS a IIS, vedere [BitS Server Impostazioni for Upload Jobs](bits-server-settings-for-upload-jobs.md).

 

 




