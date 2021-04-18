---
title: Registrazione di un server EXE in esecuzione
description: Registrazione di un server EXE in esecuzione
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331583"
---
# <a name="registering-a-running-exe-server"></a>Registrazione di un server EXE in esecuzione

Quando viene avviato un server eseguibile (EXE), deve chiamare [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), che registra il CLSID per il server in ciò che viene chiamato tabella della classe (una tabella diversa rispetto alla tabella degli oggetti in esecuzione). Quando un server viene registrato nella tabella della classe, consente a gestione controllo servizi di determinare che non è necessario avviare di nuovo la classe, perché il server è già in esecuzione. Solo se il server non è elencato nella tabella della classe, SCM verificherà i valori appropriati nel registro di sistema e avvierà il server associato al CLSID specificato.

Si passa [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) al CLSID per la classe e un puntatore alla relativa interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . I client che successivamente chiamano [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con questo CLSID recupereranno un puntatore all'interfaccia richiesta, purché la sicurezza non lo vieti. Vedere [funzioni helper](instance-creation-helper-functions.md) per la creazione di istanze per una descrizione di diverse funzioni di creazione e attivazione di istanze.

Il server per un oggetto classe deve chiamare [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) per revocare l'oggetto classe (rimuovere la registrazione) quando si verificano tutte le condizioni seguenti:

-   Nessuna istanza esistente della definizione dell'oggetto.
-   Non ci sono blocchi sull'oggetto classe.
-   L'applicazione che fornisce servizi all'oggetto classe non è sotto il controllo utente (non visibile all'utente sullo schermo).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Installazione come applicazione di servizio](installing-as-a-service-application.md)
</dt> <dt>

[Registrazione di una classe durante l'installazione](registering-a-class-at-installation.md)
</dt> <dt>

[Registrazione di oggetti nella tabella ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registrazione automatica](self-registration.md)
</dt> </dl>

 

 




