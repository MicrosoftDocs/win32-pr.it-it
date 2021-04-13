---
title: Registrazione di una classe durante l'installazione
description: Se una classe deve essere disponibile per i client in qualsiasi momento, come la maggior parte delle applicazioni, in genere viene registrata tramite un programma di installazione e configurazione.
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4253c40cb3feb7e737368c947c0b20715f5becbd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339366"
---
# <a name="registering-a-class-at-installation"></a>Registrazione di una classe durante l'installazione

Se una classe deve essere disponibile per i client in qualsiasi momento, come la maggior parte delle applicazioni, in genere viene registrata tramite un programma di installazione e configurazione. Ciò significa inserire le informazioni relative all'applicazione nel registro di sistema, incluse le modalità e la posizione in cui devono essere create le istanze degli oggetti. Queste informazioni devono essere registrate per tutti i CLSID. Altre informazioni sono facoltative. Strumenti come regsvr32 semplificano la scrittura di un programma di installazione che registra i server durante l'installazione.

Se non si basano sulle impostazioni predefinite di sistema, nel registro di sistema sono presenti due chiavi importanti: CLSID e AppID. Tra le informazioni importanti in queste chiavi viene illustrato come creare un'istanza dell'oggetto. Gli oggetti possono essere designati come in-process, out-of-process locale o out-of-process remote.

Nella chiave AppID sono disponibili diversi valori che definiscono informazioni specifiche per l'applicazione. Tra questi sono [RemoteServerName](remoteservername.md) e [ActivateAtStorage](activateatstorage.md), entrambi possono essere usati per consentire a un client di creare un oggetto, con il client senza alcuna conoscenza incorporata della posizione del server. Per ulteriori informazioni sulla creazione di istanze remote, vedere [individuazione di](locating-a-remote-object.md) [funzioni di supporto](instance-creation-helper-functions.md)per la creazione di oggetti e istanze remote.

Un server può anche essere installato come servizio o per l'esecuzione con un account utente specifico. Per ulteriori informazioni, vedere [installazione come applicazione di servizio](installing-as-a-service-application.md).

Un oggetto server o ROT che non è un servizio o in esecuzione con un account utente specifico può essere definito come server "Activate As Activator". Per questi server, il contesto di sicurezza e la stazione/desktop della finestra del client devono corrispondere a quelli del server. Un client che tenta di connettersi a un server remoto viene considerato con una finestra Station/Desktop **null** , quindi viene confrontato solo il contesto di sicurezza del server in questa istanza. Per ulteriori informazioni sui SID, vedere [sicurezza in com](security-in-com.md). COM memorizza nella cache la stazione o il desktop di un processo quando il processo si connette per la prima volta al servizio COM distribuito. Di conseguenza, i client e i server COM non devono modificare la stazione di Windows o i desktop dei thread del processo dopo la chiamata di [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

Quando una classe viene registrata come in-process, una chiamata a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) per creare il relativo oggetto classe viene passata automaticamente da com alla funzione [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) , che deve essere implementata dalla classe per assegnare all'oggetto chiamante un puntatore al relativo oggetto classe.

Le classi implementate nei file eseguibili possono specificare che COM deve eseguire il processo e attendere che il processo registri l'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) dell'oggetto della classe tramite una chiamata alla funzione [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiavi del registro di sistema COM](com-registry-keys.md)
</dt> <dt>

[Installazione come applicazione di servizio](installing-as-a-service-application.md)
</dt> <dt>

[Registrazione di un server EXE in esecuzione](registering-a-running-exe-server.md)
</dt> <dt>

[Registrazione di componenti](registering-components.md)
</dt> <dt>

[Registrazione di oggetti nella tabella ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registrazione automatica](self-registration.md)
</dt> </dl>

 

 