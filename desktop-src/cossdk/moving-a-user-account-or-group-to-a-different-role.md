---
description: È possibile rimuovere gli account utente o i gruppi da un ruolo quando gli utenti o i membri dei gruppi non devono più avere accesso alle risorse dell'applicazione a cui è assegnato il ruolo.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Spostamento di un account utente o di un gruppo in un ruolo diverso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea402b6012fa4f6e7769e4bbb29a2a11da6e750636b0c139d5f5d6701a397116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047339"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a>Spostamento di un account utente o di un gruppo in un ruolo diverso

È possibile rimuovere gli account utente o i gruppi da un ruolo quando gli utenti o i membri dei gruppi non devono più avere accesso alle risorse dell'applicazione a cui è assegnato il ruolo.

**Per rimuovere un account utente o un gruppo da un ruolo**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il ruolo a cui si è interessati. Espandere la visualizzazione nell'albero della console fino a visualizzare gli utenti per il ruolo.

2.  Fare clic con il pulsante destro del mouse sull'account utente o sul gruppo da rimuovere e quindi scegliere **Elimina.**

3.  Quando richiesto dalla finestra di dialogo **Conferma eliminazione** elemento , fare clic su **Sì** per eliminare l'account utente o il gruppo.

L'account utente o il gruppo rimosso dal ruolo non viene più visualizzato nella **cartella** Utenti. La nuova appartenenza al ruolo ha effetto al successivo avvio dell'applicazione. Se sono state apportate modifiche all'applicazione **di sistema**, è necessario riavviare il computer per l'applicazione delle modifiche.

 

 



