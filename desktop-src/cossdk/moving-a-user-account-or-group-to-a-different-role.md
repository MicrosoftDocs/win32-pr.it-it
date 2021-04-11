---
description: È possibile rimuovere gli account utente o i gruppi da un ruolo quando agli utenti o ai membri dei gruppi non deve più essere concesso l'accesso alle risorse dell'applicazione a cui è assegnato il ruolo.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Trasferimento di un account utente o di un gruppo a un ruolo diverso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2401d792066212269d4eaa4eb11eadfef6e2d73e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127406"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a>Trasferimento di un account utente o di un gruppo a un ruolo diverso

È possibile rimuovere gli account utente o i gruppi da un ruolo quando agli utenti o ai membri dei gruppi non deve più essere concesso l'accesso alle risorse dell'applicazione a cui è assegnato il ruolo.

**Per rimuovere un account utente o un gruppo da un ruolo**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il ruolo a cui si è interessati. Espandere la visualizzazione nell'albero della console fino a quando non saranno visibili gli utenti per il ruolo.

2.  Fare clic con il pulsante destro del mouse sull'account utente o sul gruppo che si desidera rimuovere, quindi scegliere **Elimina**.

3.  Quando richiesto dalla finestra di dialogo **Conferma eliminazione elemento** , fare clic su **Sì** per eliminare l'account utente o il gruppo.

L'account utente o il gruppo rimosso dal ruolo non viene più visualizzato nella cartella **utenti** . L'appartenenza al nuovo ruolo diventa effettiva al successivo avvio dell'applicazione. Se sono state apportate modifiche all' **applicazione di sistema**, è necessario riavviare il computer per rendere effettive le modifiche.

 

 



