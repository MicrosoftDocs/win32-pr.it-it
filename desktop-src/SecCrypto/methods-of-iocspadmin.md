---
description: I metodi seguenti sono definiti dall'interfaccia IOCSPAdmin. I metodi di accesso alle proprietà non sono visualizzati qui. Per visualizzare le proprietà di IOCSPAdmin, vedere Proprietà di IOCSPAdmin.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Metodi di IOCSPAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecd14d2566c5e80e863ba06e38b2945492f59b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343846"
---
# <a name="methods-of-iocspadmin"></a>Metodi di IOCSPAdmin

I metodi seguenti sono definiti dall'interfaccia [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) . I metodi di accesso alle proprietà non sono visualizzati qui. Per visualizzare le proprietà di **IOCSPAdmin**, vedere [proprietà di IOCSPAdmin](properties-of-iocspadmin.md).



| Metodo                                                              | Descrizione                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | Si connette a un server risponditore OCSP (Online Certificate Status Protocol) e Inizializza un oggetto **OCSPAdmin** con le informazioni di configurazione dal server.                                                                                                     |
| [**Gethashalgorithms**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | Ottiene un elenco di nomi di algoritmi hash. Il server risponditore usa uno degli algoritmi denominati per firmare le risposte OCSP per una determinata configurazione dell' [*autorità di certificazione*](../secgloss/c-gly.md) (CA). |
| [**GetMyRoles**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | Ottiene la maschera di accesso dei ruoli dei privilegi per un utente in un server di risponditore specificato.                                                                                                                                                                                           |
| [**GetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | Ottiene le informazioni sul descrittore di sicurezza per un server risponditore.                                                                                                                                                                                                              |
| [**GetSigningCertificates**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | Ottiene i certificati di firma disponibili in un server risponditore per un certificato CA specificato.                                                                                                                                                                        |
| [**Ping**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | Verifica una connessione DCOM con un servizio risponditore.                                                                                                                                                                                                                         |
| [**SetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | Aggiorna un servizio risponditore con modifiche di configurazione.                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | Aggiorna le informazioni sul descrittore di sicurezza per un server risponditore OCSP.                                                                                                                                                                                                     |



 

 

 
