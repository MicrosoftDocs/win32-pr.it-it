---
description: Altri strumenti Microsoft per la creazione di applicazioni distribuite
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Altri strumenti Microsoft per la creazione di applicazioni distribuite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9114454dbbeaa3c8f21cc1ea5166f93760fdd99772425f0245d7b8883f2db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070401"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a>Altri strumenti Microsoft per la creazione di applicazioni distribuite

Oltre agli strumenti in COM+, Microsoft offre gli strumenti seguenti per assistere lo sviluppatore nella creazione di applicazioni distribuite:

-   Microsoft Data Access Components (MDAC). Microsoft offre diverse possibilità per recuperare i dati da una miriade di origini. Ad esempio, OLE DB un set di interfacce COM per la compilazione di componenti di database. Le interfacce vengono definite in modo che i provider di dati possano implementare diversi livelli di supporto, in base alle funzionalità dell'archivio dati sottostante. Poiché OLE DB è basato su COM, può essere facilmente esteso e le estensioni vengono implementate come nuove interfacce. OLE DB include anche un'interfaccia di programmazione a livello di applicazione, denominata ActiveX Data Objects (ADO). ADO espone le interfacce duali, quindi può essere facilmente usato da linguaggi di scripting, Microsoft Visual C++, Visual Basic e altri strumenti di sviluppo.

    > [!Note]  
    > Gli sviluppatori possono anche scegliere di usare un'API generica indipendente dal fornitore, ad esempio l'API (Application Programming Interface) microsoft Open Database Connectivity (ODBC). L'API ODBC è un'interfaccia del linguaggio C per l'accesso ai dati in un dbms usando Structured Query Language (SQL). Gestione driver ODBC fornisce l'interfaccia di programmazione e i componenti di run-time per individuare i driver specifici di DBMS. I driver ODBC, in genere forniti dal fornitore DBMS, traducono le chiamate generiche dal gestore driver ODBC in chiamate al metodo di accesso ai dati nativo. Il vantaggio principale dell'uso dell'API ODBC è che è necessario apprendere una sola API per accedere a un'ampia gamma di DBMS.

     

-   Microsoft SQL Server. Oltre a fornire un sistema di database relazionali affidabile ed efficace, Microsoft SQL Server può fornire un'applicazione distribuita con pool di connessioni e sicurezza che possono integrarsi con il modello di sicurezza Windows sicurezza.

-   Integrazione delle transazioni COM (COMTI). COMTI può essere usato per integrare sistemi mainframe in Windows, incluse le applicazioni COM+. COMTI usa protocolli di comunicazione standard (ad esempio LU 6.2) per la comunicazione tra computer Windows e mainframe e minicomputer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presupposti e principi di progettazione COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Progettazione dell'applicazione COM+ tramite UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Progettazione generale Suggerimenti per l'uso di COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Ottimizzazione delle interazioni con il livello di logica di business COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



