---
title: Registrazione di una classe durante l'installazione
description: Se una classe è destinata a essere disponibile per i client in qualsiasi momento, come la maggior parte delle applicazioni, in genere la si registra tramite un programma di installazione e installazione.
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017e4393a4c5422157c8f9b9e9b7f366c2fafc8cfe6af5722e451a3d1b9fa069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047859"
---
# <a name="registering-a-class-at-installation"></a>Registrazione di una classe durante l'installazione

Se una classe è destinata a essere disponibile per i client in qualsiasi momento, come la maggior parte delle applicazioni, in genere la si registra tramite un programma di installazione e installazione. Ciò significa inserire informazioni sull'applicazione nel Registro di sistema, tra cui come e dove creare un'istanza dei relativi oggetti. Queste informazioni devono essere registrate per tutti i CLSID. Altre informazioni sono facoltative. Strumenti come Regsvr32 rendono più semplice scrivere un programma di installazione che registra i server durante l'installazione.

Se non si basano sulle impostazioni predefinite del sistema, nel Registro di sistema sono presenti due chiavi importanti: CLSID e AppID. Tra le informazioni importanti sotto queste chiavi c'è la modalità di creazione di un'istanza dell'oggetto. Gli oggetti possono essere designati come in-process, locali out-of-process o remoti out-of-process.

Nella chiave AppID sono presenti diversi valori che definiscono informazioni specifiche per l'applicazione. Tra questi sono [RemoteServerName](remoteservername.md) e [ActivateAtStorage,](activateatstorage.md)entrambi che possono essere usati per consentire a un client di creare un oggetto, senza che il client abbia una conoscenza predefinita della posizione del server. Per altre informazioni sulla creazione di istanze remote, vedere [Individuazione di](locating-a-remote-object.md) un oggetto remoto e funzioni helper per la creazione [di istanze.](instance-creation-helper-functions.md)

Un server può anche essere installato come servizio o per l'esecuzione con un account utente specifico. Per altre informazioni, vedere [Installazione come applicazione di servizio.](installing-as-a-service-application.md)

Un server o un oggetto ROT che non è un servizio o in esecuzione con un account utente specifico può essere definito server "attivatore". Per questi server, il contesto di sicurezza e la stazione/desktop della finestra del client devono corrispondere a del server. Un client che tenta di connettersi a un server remoto viene considerato con una finestra/desktop **NULL,** pertanto in questa istanza viene confrontato solo il contesto di sicurezza del server. Per altre informazioni sui SID, vedere [Sicurezza in COM.](security-in-com.md) COM memorizza nella cache la stazione/desktop della finestra di un processo quando il processo si connette per la prima volta al servizio COM distribuito. Pertanto, i client e i server COM non devono modificare i desktop delle finestre o dei thread del processo dopo aver chiamato [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)

Quando una classe viene registrata come in-process, una chiamata a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) per creare l'oggetto classe viene passata automaticamente da COM alla funzione [**DllGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) che la classe deve implementare per assegnare all'oggetto chiamante un puntatore al relativo oggetto classe.

Le classi implementate nei file eseguibili possono specificare che COM deve eseguire il processo e attendere che il processo registri l'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) dell'oggetto classe tramite una chiamata alla [**funzione CoRegisterClassObject.**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiavi del Registro di sistema COM](com-registry-keys.md)
</dt> <dt>

[Installazione come applicazione di servizio](installing-as-a-service-application.md)
</dt> <dt>

[Registrazione di un server EXE in esecuzione](registering-a-running-exe-server.md)
</dt> <dt>

[Registrazione di componenti](registering-components.md)
</dt> <dt>

[Registrazione di oggetti nella ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registrazione automatica](self-registration.md)
</dt> </dl>

 

 