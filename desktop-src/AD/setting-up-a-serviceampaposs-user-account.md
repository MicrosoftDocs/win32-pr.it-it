---
title: Configurazione dell'account utente di un servizio
description: Il programma di installazione del servizio può suggerire un account di accesso predefinito per un'istanza del servizio e consentire all'amministratore di selezionare l'account predefinito o specificarne uno diverso.
ms.assetid: 37285c23-8922-4da5-9f0b-922ea5e5794e
ms.tgt_platform: multiple
keywords:
- Impostazione dell'account utente di un servizio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705fa16d8d2cce137755f4a5086716aaaef8046a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724407"
---
# <a name="setting-up-a-services-user-account"></a>Configurazione dell'account utente di un servizio

Il programma di installazione del servizio può suggerire un account di accesso predefinito per un'istanza del servizio e consentire all'amministratore di selezionare l'account predefinito o specificarne uno diverso. Se l'amministratore seleziona un account utente, anziché l'account LocalSystem, l'account deve esistere prima di chiamare la funzione [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) per installare un'istanza del servizio in un server host. Per ulteriori informazioni e un esempio di codice che può essere utilizzato per creare un nuovo oggetto utente di dominio in Active Directory Domain Services, vedere [creazione di un utente](creating-a-user.md).

Idealmente, ogni istanza di un servizio, sia che si tratti di un servizio basato su host o replicabile, deve disporre di un proprio account utente di dominio. L'utilizzo di account separati per ogni istanza del servizio è più sicuro rispetto alla condivisione dello stesso account da parte di più istanze. Inoltre, l'utilizzo di account separati consente di controllare le attività di ogni istanza del servizio.

Quando il programma di installazione suggerisce un account di accesso predefinito, è necessario specificare il nome di un nuovo account da creare per la nuova istanza del servizio. Il nome dell'account può essere composto dagli stessi elementi utilizzati per comporre un nome dell'entità servizio, ad esempio la classe del servizio, il computer host e il nome del servizio. Per altre informazioni vedere [Service Principal Names](service-principal-names.md) (Nomi di entità servizio). In genere, l'account viene creato nel contenitore degli utenti nel dominio del computer host.

È necessario generare una password per ogni account. Per ulteriori informazioni su come scrivere uno strumento che consente di automatizzare l'attività di aggiornamento delle password degli account del servizio, vedere [modifica della password per l'account utente di un servizio](changing-the-password-on-a-serviceampaposs-user-account.md).

 

 