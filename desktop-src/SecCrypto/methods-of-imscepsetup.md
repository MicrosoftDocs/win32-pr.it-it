---
description: Metodi definiti dall'interfaccia IMSCEPSetup.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Metodi di IMSCEPSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f543bb4525a3335128846ec5724e1a9a09a35f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526731"
---
# <a name="methods-of-imscepsetup"></a>Metodi di IMSCEPSetup

I metodi seguenti sono definiti dall'interfaccia [**IMSCEPSetup**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) . I metodi di accesso alle proprietà non sono visualizzati qui. Per visualizzare le proprietà di **IMSCEPSetup**, vedere [proprietà di IMSCEPSetup](properties-of-imscepsetup.md).



| Metodo                                                             | Descrizione                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Ottiene l'elenco delle [*lunghezze di chiave*](../secgloss/k-gly.md) supportate dal [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) specificato. |
| [**GetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Ottiene un valore della proprietà per una configurazione del servizio Registrazione dispositivi di rete (registrazione dispositivi).                                                                                                                                                                                               |
| [**GetProviderName**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Ottiene l'elenco dei CSP che forniscono la firma della chiave asimmetrica e gli algoritmi di scambio nel computer.                                                                                                                                                                              |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Inizializza un oggetto **CMSCEPSetup** con i valori predefiniti per consentire l'installazione di un ruolo Registrazione dispositivi.                                                                                                                                                                                  |
| [**Installazione**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Installa un ruolo come configurato nell'oggetto **CMSCEPSetup** .                                                                                                                                                                                                                      |
| [**IsMSCEPStoreEmpty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Restituisce sempre **Variant \_ true** e non deve essere utilizzato.                                                                                                                                                                                                                          |
| [**Comandi**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Questo metodo non è implementato. in quanto è riservata per utilizzi futuri.                                                                                                                                                                                                                    |
| [**Disinstallazione**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Rimuove il registro di sistema e le impostazioni IIS per il ruolo Registrazione dispositivi.                                                                                                                                                                                                                              |
| [**SetAccountInformation**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Imposta le informazioni sull'account utente utilizzate dall'estensione IIS Registrazione dispositivi per eseguire la registrazione per conto dei dispositivi di rete.                                                                                                                                                              |
| [**SetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Imposta un valore della proprietà per una configurazione Registrazione dispositivi.                                                                                                                                                                                                                                  |



 

 

 
