---
description: Altri strumenti Microsoft per la creazione di applicazioni distribuite
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Altri strumenti Microsoft per la creazione di applicazioni distribuite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305136"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a>Altri strumenti Microsoft per la creazione di applicazioni distribuite

Oltre agli strumenti di COM+, Microsoft offre gli strumenti seguenti per aiutare gli sviluppatori nella creazione di applicazioni distribuite:

-   Microsoft Data Access Components (MDAC). Microsoft offre diverse vie per il recupero di dati da una miriade di origini. OLE DB, ad esempio, offre un set di interfacce COM per la compilazione di componenti di database. Le interfacce sono definite in modo che i provider di dati possano implementare livelli di supporto diversi, in base alle funzionalità dell'archivio dati sottostante. Poiché OLE DB è basato su COM, può essere facilmente esteso e le estensioni vengono implementate come nuove interfacce. OLE DB include anche un'interfaccia di programmazione a livello di applicazione, denominata ActiveX Data Objects (ADO). ADO espone le interfacce duali, in modo che possa essere usato facilmente da linguaggi di scripting, nonché Microsoft Visual C++, Visual Basic e altri strumenti di sviluppo.

    > [!Note]  
    > Gli sviluppatori possono anche scegliere di usare un'API generica e indipendente dal fornitore, ad esempio Microsoft Open Database Connectivity (ODBC) Application Programming Interface (API). L'API ODBC è un'interfaccia del linguaggio C per accedere ai dati in un sistema DBMS utilizzando Structured Query Language (SQL). Gestione driver ODBC fornisce l'interfaccia di programmazione e i componenti di runtime per individuare i driver specifici del sistema DBMS. I driver ODBC, in genere forniti dal fornitore del sistema DBMS, convertono chiamate generiche da Gestione driver ODBC in chiamate al metodo di accesso ai dati nativi. Il vantaggio principale dell'utilizzo dell'API ODBC è che è necessario apprendere una sola API per accedere a un'ampia gamma di sistemi DBMS.

     

-   Microsoft SQL Server. Oltre a fornire un sistema di database relazionale solido ed eloquente, Microsoft SQL Server possibile fornire un'applicazione distribuita con pool di connessioni e sicurezza che può integrarsi con il modello di sicurezza di Windows.

-   Integrazione delle transazioni COM (COMTI). COMTI può essere usato per integrare i sistemi mainframe nei sistemi Windows, incluse le applicazioni COM+. COMTI usa protocolli di comunicazione standard (ad esempio, LU 6,2) per la comunicazione tra computer Windows e mainframe e minicomputer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presupposti e principi di progettazione COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Progettazione dell'applicazione COM+ tramite UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Suggerimenti di progettazione generali per l'utilizzo di COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Ottimizzazione delle interazioni con il livello di logica di business COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



