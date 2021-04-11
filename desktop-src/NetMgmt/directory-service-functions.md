---
title: Funzioni del servizio directory (gestione della rete)
description: Le funzioni del servizio directory di gestione della rete consentono agli sviluppatori di utilizzare il controller di dominio e l'appartenenza al dominio nel servizio directory.
ms.assetid: 9eeb8f40-85c0-49db-a307-193703e4f463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9e843e06762b4a7ef55b3f979b12a62ee6adf3
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104047580"
---
# <a name="directory-service-functions"></a>Funzioni del servizio directory

Le funzioni del servizio directory di gestione della rete consentono agli sviluppatori di utilizzare il controller di dominio e l'appartenenza al dominio nel servizio directory.

Le funzioni del servizio directory di gestione della rete sono elencate di seguito.



| Funzione                                                                 | Descrizione                                                                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)       | Aggiunge un nome alternativo per il computer specificato.                                                                                                                                          |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)           | Enumera i nomi per il computer specificato.                                                                                                                                                |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                           | Recupera un elenco di unità organizzative (OU) in cui è possibile creare un account computer.                                                                                                  |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                   | Recupera le informazioni sullo stato del join per il computer specificato.                                                                                                                               |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                   | Aggiunge un computer a un gruppo di lavoro o a un dominio.                                                                                                                                                  |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)       | Effettua il provisioning di un account computer per un uso successivo in un'operazione di aggiunta al dominio offline.                                                                                                           |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername) | Rimuove un nome alternativo per il computer specificato.                                                                                                                                       |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)             | Modifica il nome di un computer in un dominio.                                                                                                                                                 |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)           | Imposta il nome del computer primario per il computer specificato.                                                                                                                                  |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                               | Separare un computer da un gruppo di lavoro o da un dominio.                                                                                                                                            |
| [**NetValidateName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                               | Verifica la validità di un nome di computer, di un nome di gruppo di lavoro o di un nome di dominio.                                                                                                                   |



 

Per ulteriori informazioni sulla programmazione per Active Directory, vedere l' [Active Directory di riferimento](/windows/desktop/AD/active-directory-domain-services-reference). Per ulteriori informazioni sulle unità organizzative, vedere [gestione degli utenti](/windows/desktop/AD/managing-users) nella documentazione di Active Directory.

 

 