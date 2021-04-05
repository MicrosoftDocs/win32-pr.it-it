---
title: Controllo di accesso e eliminazione di oggetti
description: Active Directory consente di eliminare un oggetto se si dispone dell'accesso DELETE per l'oggetto o ADS \_ Rights \_ DS \_ Delete \_ child Access per il tipo di oggetto nel contenitore padre.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- Active Directory per il controllo di accesso e l'eliminazione di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724375"
---
# <a name="access-control-and-object-deletion"></a>Controllo di accesso e eliminazione di oggetti

Active Directory Domain Services consentono di eliminare un oggetto se si dispone di uno dei seguenti diritti di accesso:

-   Elimina accesso all'oggetto stesso
-   ADS \_ Rights \_ DS \_ eliminare l' \_ accesso figlio per quel tipo di oggetto nel contenitore padre

Tenere presente che il sistema verifica il descrittore di sicurezza sia per l'oggetto che per il relativo elemento padre prima di negare l'eliminazione. Ciò significa che una voce ACE che nega in modo esplicito l'accesso DELETE a un utente non ha alcun effetto se l'utente dispone dell' \_ accesso figlio Delete nell'elemento padre. Analogamente, è possibile eseguire l'override di una voce ACE che nega l' \_ accesso figlio Delete nell'elemento padre se l'accesso DELETE è consentito per l'oggetto stesso.

Per eseguire un'operazione di eliminazione di una struttura ad albero, ad esempio usando il metodo [**IADsDeleteOps::D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) , è necessario avere ads \_ Rights \_ DS \_ Delete \_ Tree Access all'oggetto. Se si dispone di questo diritto di accesso, è possibile eliminare l'oggetto e tutti gli oggetti figlio indipendentemente dalle protezioni sugli oggetti figlio. Per eliminare un albero se non si ha ADS \_ Rights \_ DS \_ Delete \_ Tree Access, è necessario attraversare in modo ricorsivo l'albero, eliminando singolarmente ogni oggetto. In questo caso, è necessario disporre dell'accesso figlio DELETE o DELETE necessario \_ per ogni oggetto nell'albero.

> [!WARNING]
> Se gli utenti hanno ADS \_ Rights \_ DS \_ Delete \_ Tree Access per un oggetto, ciò consente di eliminare un intero sottoalbero, inclusi tutti gli oggetti figlio. Per questo motivo, è possibile prendere in considerazione la revoca dell'autorizzazione di accesso "Delete subtree" per tutti gli utenti in un contenitore padre.

 

 

 