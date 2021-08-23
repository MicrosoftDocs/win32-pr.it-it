---
description: Metodi definiti dall'interfaccia IMSCEPSetup.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Metodi di IMSCEPSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7dcadeb6c3815a37f1b1e87453a7ff737c70f53d76e0904bc67211ed7028f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622231"
---
# <a name="methods-of-imscepsetup"></a>Metodi di IMSCEPSetup

I metodi seguenti sono definiti [**dall'interfaccia IMSCEPSetup.**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) I metodi di accesso alle proprietà non sono illustrati qui. Per visualizzare le proprietà per **IMSCEPSetup,** vedere [Proprietà di IMSCEPSetup.](properties-of-imscepsetup.md)



| Metodo                                                             | Descrizione                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Ottiene l'elenco [*delle lunghezze di chiave*](../secgloss/k-gly.md) supportate dal provider del servizio di [*crittografia*](../secgloss/c-gly.md) (CSP) specificato. |
| [**GetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Ottiene un valore della proprietà per una servizio Registrazione dispositivi di rete (NDES).                                                                                                                                                                                               |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Ottiene l'elenco di CSP che forniscono la firma della chiave asimmetrica e gli algoritmi di scambio nel computer.                                                                                                                                                                              |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Inizializza un oggetto **CMSCEPSetup con** i valori predefiniti per abilitare l'installazione di un ruolo NDES.                                                                                                                                                                                  |
| [**Installazione**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Installa un ruolo come configurato **nell'oggetto CMSCEPSetup.**                                                                                                                                                                                                                      |
| [**IsMSCEPStoreEmpty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Restituisce sempre **VARIANT \_ TRUE** e non deve essere usato.                                                                                                                                                                                                                          |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Questo metodo non è implementato. in quanto è riservata per utilizzi futuri.                                                                                                                                                                                                                    |
| [**PreInstallazione**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Rimuove le impostazioni del Registro di sistema e IIS per il ruolo NDES.                                                                                                                                                                                                                              |
| [**SetAccountInformation**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Imposta le informazioni sull'account utente usate dall'estensione iis NDES per eseguire la registrazione per conto dei dispositivi di rete.                                                                                                                                                              |
| [**SetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Imposta un valore della proprietà per una configurazione NDES.                                                                                                                                                                                                                                  |



 

 

 
