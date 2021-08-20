---
title: Registrazione di un server EXE in esecuzione
description: Registrazione di un server EXE in esecuzione
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc4aa984090c35a4b700719d248a75c1a8d917dfcb707f288a6b9985c672742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104876"
---
# <a name="registering-a-running-exe-server"></a>Registrazione di un server EXE in esecuzione

Quando viene avviato un server eseguibile (EXE), deve chiamare [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), che registra il CLSID per il server in quella che viene chiamata tabella di classi (una tabella diversa dalla tabella degli oggetti in esecuzione). Quando un server viene registrato nella tabella di classi, consente a Gestione controllo servizi di determinare che non è necessario avviare nuovamente la classe, perché il server è già in esecuzione. Solo se il server non è elencato nella tabella di classi, Gestione controllo servizi verifica la presenza di valori appropriati nel Registro di sistema e avvia il server associato al CLSID specificato.

Si passa [**coRegisterClassObject al**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) CLSID per la classe e un puntatore alla relativa [**interfaccia IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) I client che successivamente chiamano [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con questo CLSID recupereranno un puntatore all'interfaccia richiesta, purché la sicurezza non lo proibi. Per una [descrizione di diverse funzioni](instance-creation-helper-functions.md) di creazione e attivazione di istanze, vedere Funzioni helper di creazione di istanze.

Il server per un oggetto classe deve chiamare [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) per revocare l'oggetto classe (rimuovere la registrazione) quando si verificano tutte le condizioni seguenti:

-   Non sono presenti istanze esistenti della definizione dell'oggetto.
-   Non sono presenti blocchi sull'oggetto classe.
-   L'applicazione che fornisce servizi all'oggetto classe non è sotto il controllo dell'utente (non visibile all'utente sullo schermo).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Installazione come applicazione di servizio](installing-as-a-service-application.md)
</dt> <dt>

[Registrazione di una classe durante l'installazione](registering-a-class-at-installation.md)
</dt> <dt>

[Registrazione di oggetti nella ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registrazione automatica](self-registration.md)
</dt> </dl>

 

 




