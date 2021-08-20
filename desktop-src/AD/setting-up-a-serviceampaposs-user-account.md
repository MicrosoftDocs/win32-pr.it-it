---
title: Configurazione dell'account utente di un servizio
description: Il programma di installazione del servizio può suggerire un account di accesso predefinito per un'istanza del servizio e consentire all'amministratore di selezionare l'account predefinito o specificarne uno diverso.
ms.assetid: 37285c23-8922-4da5-9f0b-922ea5e5794e
ms.tgt_platform: multiple
keywords:
- Configurazione dell'account utente di un servizio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f310ee97c68ded8c4086694302feccb5991d726e01f9addbeced21cc5b9acfdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183278"
---
# <a name="setting-up-a-services-user-account"></a>Configurazione dell'account utente di un servizio

Il programma di installazione del servizio può suggerire un account di accesso predefinito per un'istanza del servizio e consentire all'amministratore di selezionare l'account predefinito o specificarne uno diverso. Se l'amministratore seleziona un account utente anziché l'account LocalSystem, l'account deve esistere prima di chiamare la funzione [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) per installare un'istanza del servizio in un server host. Per altre informazioni e un esempio di codice che può essere usato per creare un nuovo oggetto utente di dominio in Active Directory Domain Services, vedere [Creazione di un utente](creating-a-user.md).

Idealmente, ogni istanza di un servizio, indipendentemente dal fatto che sia basato su host o replicabile, deve avere un proprio account utente di dominio. L'uso di account separati per ogni istanza del servizio è più sicuro rispetto alla condivisione dello stesso account da parte di più istanze. Inoltre, l'uso di account separati consente di controllare le attività di ogni istanza del servizio.

Quando il programma di installazione suggerisce un account di accesso predefinito, deve specificare il nome di un nuovo account da creare per la nuova istanza del servizio. Il nome dell'account può essere composto dagli stessi elementi usati per comporre un nome di entità servizio, ad esempio la classe del servizio, il computer host e il nome del servizio. Per altre informazioni vedere [Service Principal Names](service-principal-names.md) (Nomi di entità servizio). In genere, l'account viene creato nel contenitore Users nel dominio del computer host.

È necessario generare una password per ogni account. Per altre informazioni su come scrivere uno strumento che automatizza l'attività di aggiornamento delle password dell'account del servizio, vedere Modifica della [password nell'account](changing-the-password-on-a-serviceampaposs-user-account.md)utente di un servizio.

 

 