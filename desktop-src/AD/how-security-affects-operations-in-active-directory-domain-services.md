---
title: Effetti della sicurezza sulle operazioni in Active Directory Domain Services
description: Active Directory Domain Services usare il controllo di accesso per concedere o negare l'accesso a oggetti, proprietà e operazioni in base all'identità dell'utente che esegue il tentativo di accesso.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Effetti della sicurezza in Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be628acd1709985aeaa9539bfa527de674732ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855422"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a>Effetti della sicurezza sulle operazioni in Active Directory Domain Services

Active Directory Domain Services usare il controllo di accesso per concedere o negare l'accesso a oggetti, proprietà e operazioni in base all'identità dell'utente che esegue il tentativo di accesso. Quando l'applicazione viene associata alla directory, viene associata a credenziali utente specifiche. Una volta autenticate, queste credenziali determinano il contesto di sicurezza dell'applicazione. Indipendentemente dal fatto che le credenziali siano quelle dell'utente connesso, un utente specificato, un account del servizio, un account computer o un utente non autenticato (Guest/Everyone), il Active Directory Server verifica il diritto dell'utente di accedere a un oggetto prima che venga eseguita un'operazione sull'oggetto. L'utente può, o meno, avere accesso a un particolare oggetto, ai relativi elementi figlio, alle relative proprietà o alle operazioni su tale oggetto, il che significa che l'applicazione deve gestire i potenziali errori causati dall'accesso negato.

Per ulteriori informazioni sui contesti di sicurezza e sugli effetti del controllo di accesso su varie operazioni, vedere:

-   [Controllo di accesso e operazioni di lettura](access-control-and-read-operations.md)
-   [Operazioni di scrittura e controllo di accesso](access-control-and-write-operations.md)
-   [Controllo di accesso e creazione di oggetti](access-control-and-object-creation.md)
-   [Controllo di accesso e eliminazione di oggetti](access-control-and-object-deletion.md)

 

 




