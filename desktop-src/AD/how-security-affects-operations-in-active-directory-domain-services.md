---
title: Effetti della sicurezza sulle operazioni in Active Directory Domain Services
description: Active Directory Domain Services il controllo di accesso per concedere o negare l'accesso a oggetti, proprietà e operazioni in base all'identità dell'utente che esegue il tentativo di accesso.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Effetti sulla sicurezza in Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8f5599afbc8552f9708fcfa953a069f429a152c4f0fff37546ffb7d9f6b809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188206"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a>Effetti della sicurezza sulle operazioni in Active Directory Domain Services

Active Directory Domain Services il controllo di accesso per concedere o negare l'accesso a oggetti, proprietà e operazioni in base all'identità dell'utente che esegue il tentativo di accesso. Quando l'applicazione viene associata alla directory, viene associata a credenziali utente specifiche. Dopo l'autenticazione, queste credenziali determinano il contesto di sicurezza dell'applicazione. Indipendentemente dal fatto che le credenziali siano quelle dell'utente connesso, di un utente specificato, di un account del servizio, di un account computer o di un utente non autenticato (Guest/Everyone), il server Active Directory verifica il diritto dell'utente di accedere a un oggetto prima che venga eseguita qualsiasi operazione su tale oggetto. L'utente può o meno avere accesso a un determinato oggetto, ai relativi elementi figlio, alle relative proprietà o a operazioni su tale oggetto, il che significa che l'applicazione deve gestire i potenziali errori causati dall'accesso negato.

Per altre informazioni sui contesti di sicurezza e sugli effetti del controllo di accesso su varie operazioni, vedere:

-   [Controllo di accesso e operazioni di lettura](access-control-and-read-operations.md)
-   [Controllo di accesso e operazioni di scrittura](access-control-and-write-operations.md)
-   [Controllo di accesso e creazione di oggetti](access-control-and-object-creation.md)
-   [Controllo di accesso ed eliminazione di oggetti](access-control-and-object-deletion.md)

 

 




