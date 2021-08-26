---
description: I metodi seguenti sono definiti dall'interfaccia IOCSPAdmin. I metodi di accesso alle proprietà non vengono visualizzati qui. Per visualizzare le proprietà di IOCSPAdmin, vedere Proprietà di IOCSPAdmin.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Metodi di IOCSPAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a455ae5cfbb49d60cc0d0a03265d05c98efa2f2217746086b0acf0a4230709dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992851"
---
# <a name="methods-of-iocspadmin"></a>Metodi di IOCSPAdmin

I metodi seguenti sono definiti [**dall'interfaccia IOCSPAdmin.**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) I metodi di accesso alle proprietà non vengono visualizzati qui. Per visualizzare le proprietà di **IOCSPAdmin,** vedere [Proprietà di IOCSPAdmin](properties-of-iocspadmin.md).



| Metodo                                                              | Descrizione                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | Si connette a un server risponditore OCSP (Online Certificate Status Protocol) e inizializza un oggetto **OCSPAdmin** con le informazioni di configurazione del server.                                                                                                     |
| [**GetHashAlgorithms**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | Ottiene un elenco di nomi di algoritmi hash. Il server risponditore usa uno degli algoritmi denominati per firmare le risposte OCSP per una determinata configurazione [*dell'autorità*](../secgloss/c-gly.md) di certificazione (CA). |
| [**GetMyRoles**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | Ottiene la maschera di accesso dei ruoli dei privilegi per un utente in un determinato server risponditore.                                                                                                                                                                                           |
| [**GetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | Ottiene informazioni sul descrittore di sicurezza per un server risponditore.                                                                                                                                                                                                              |
| [**GetSigningCertificates**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | Ottiene i certificati di firma disponibili in un server risponditore per un certificato CA specificato.                                                                                                                                                                        |
| [**Ping**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | Verifica una connessione DCOM con un servizio risponditore.                                                                                                                                                                                                                         |
| [**SetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | Aggiorna un servizio risponditore con modifiche di configurazione.                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | Aggiorna le informazioni sul descrittore di sicurezza per un server risponditore OCSP.                                                                                                                                                                                                     |



 

 

 
