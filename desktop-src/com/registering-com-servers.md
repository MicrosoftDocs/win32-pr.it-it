---
title: Registrazione di server COM
description: Registrazione di server COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118487"
---
# <a name="registering-com-servers"></a>Registrazione di server COM

Dopo aver definito una classe nel codice (garantendo che implementi [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) e avergli assegnato un CLSID, è necessario inserire nel registro di sistema le informazioni che consentiranno a com, su richiesta di un client con il CLSID, di creare istanze dei relativi oggetti. Queste informazioni indicano al sistema, per un determinato CLSID, dove si trova il codice DLL o EXE per la classe e come deve essere avviato.

Esiste più di un modo per registrare una classe nel registro di sistema. Inoltre, esistono altri modi per "registrare" una classe con il sistema durante l'esecuzione, in modo che il sistema sia in grado di riconoscere che un oggetto in esecuzione è attualmente nel sistema.

Per ulteriori informazioni sulla registrazione, vedere gli argomenti seguenti:

-   [Registrazione di una classe durante l'installazione](registering-a-class-at-installation.md)
-   [Registrazione di un server EXE in esecuzione](registering-a-running-exe-server.md)
-   [Registrazione di oggetti nella tabella ROT](registering-objects-in-the-rot.md)
-   [Registrazione automatica](self-registration.md)
-   [Installazione come applicazione di servizio](installing-as-a-service-application.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Responsabilità server COM](com-server-responsibilities.md)
</dt> </dl>

 

 