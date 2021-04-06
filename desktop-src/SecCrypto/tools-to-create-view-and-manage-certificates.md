---
description: Gli strumenti CryptoAPI sono strumenti per eseguire attività comuni di gestione dei certificati.
ms.assetid: 29146de8-adae-444b-bc75-fa43a19ab8f9
title: Strumenti per creare, visualizzare e gestire i certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fb4595b7c7711b10271bd97a447a77f3a01c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759623"
---
# <a name="tools-to-create-view-and-manage-certificates"></a>Strumenti per creare, visualizzare e gestire i certificati

Gli strumenti CryptoAPI sono strumenti per eseguire attività comuni di gestione dei certificati.



| Strumento                                | Commenti                                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MakeCert](makecert.md)<br/> | Crea un certificato [*X. 509*](../secgloss/x-gly.md) di test.<br/>                                                                                |
| [Cert2SPC](cert2spc.md)<br/> | Crea un [*certificato di autore del software*](../secgloss/s-gly.md) di test (SPC).<br/>           |
| [CertMgr](certmgr.md)<br/>   | Gestisce certificati, scopi consentiti e [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL).<br/> |



 

Tutti gli input utente per questi strumenti non fanno distinzione tra maiuscole e minuscole. Sono ora disponibili opzioni separate per il nome della [*coppia di chiavi*](../secgloss/k-gly.md) e il file di [*chiave privata*](../secgloss/p-gly.md) .

## <a name="additional-tools"></a>Strumenti aggiuntivi

Certutil.exe è uno strumento da riga di comando che viene installato come parte di Servizi certificati. È possibile utilizzare Certutil.exe per eseguire il dump e visualizzare le informazioni di configurazione dell' [*autorità di certificazione*](../secgloss/c-gly.md) (CA), configurare i servizi certificati, eseguire il backup e ripristinare i componenti CA e verificare i [*certificati*](../secgloss/c-gly.md), le [*coppie di chiavi*](../secgloss/k-gly.md)e le catene di certificati. Per ulteriori informazioni su Certutil, vedere l'argomento [certutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732443(v=ws.11)) in Microsoft TechNet.

 

 
