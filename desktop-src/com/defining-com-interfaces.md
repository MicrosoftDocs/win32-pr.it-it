---
title: Definizione di interfacce COM
description: Microsoft definisce numerose interfacce COM. Nella maggior parte dei casi, è possibile riutilizzare queste interfacce generiche. Tuttavia, alcune applicazioni prevedono requisiti specifici che consentono di definire interfacce di oggetti personalizzate.
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516c02a2c337b2c76229094b0e42d75b44f65d16
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118511"
---
# <a name="defining-com-interfaces"></a>Definizione di interfacce COM

Microsoft definisce numerose interfacce COM. Nella maggior parte dei casi, è possibile riutilizzare queste interfacce generiche. Tuttavia, alcune applicazioni prevedono requisiti specifici che consentono di definire interfacce di oggetti personalizzate.

Tutte le interfacce COM devono derivare, direttamente o indirettamente, dall'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . All'interno di tale vincolo, l'interfaccia personalizzata può supportare quasi qualsiasi metodo o parametro, inclusi i metodi asincroni. È anche possibile generare una libreria dei tipi per le interfacce personalizzate in modo che i client possano accedere alle informazioni sui metodi dell'oggetto in fase di esecuzione. Dopo aver definito un'interfaccia, descriverla in Microsoft Interface Definition Language (MIDL), compilarla e registrarla in modo analogo a qualsiasi interfaccia generica. Con Distributed COM, i metodi di interfaccia sono disponibili sia per i processi remoti che per altri processi nello stesso computer.

Infine, la compilazione di interfacce COM richiede un ambiente di sviluppo che includa un compilatore C/C++ e il compilatore Midl.exe.

I passaggi per la creazione di un'interfaccia COM sono i seguenti:

-   Decidere come si desidera fornire supporto per il marshalling per l'interfaccia. con marshalling guidato dalla libreria dei tipi o con una DLL proxy/stub. È necessario effettuare il marshalling anche delle interfacce in-process se devono essere usate tra i limiti dell'Apartment. È consigliabile creare il supporto del marshalling in ogni interfaccia COM, anche se non si ritiene che sia necessario. Per ulteriori informazioni, vedere [marshalling di interfaccia](interface-marshaling.md) .
-   Descrivere l'interfaccia o le interfacce in un file di definizione di interfaccia (IDL). Inoltre, è possibile specificare determinati aspetti locali dell'interfaccia in un file di configurazione dell'applicazione (ACF). Se si usa il marshalling guidato dalla libreria dei tipi, aggiungere un'istruzione [**Library**](/windows/desktop/Midl/library) che faccia riferimento alle interfacce per le quali si desidera generare informazioni sul tipo.
-   Usare il compilatore MIDL per generare un file della libreria dei tipi e un file di intestazione, file di proxy/stub del linguaggio C, un file di identificatore di interfaccia, un file di dati DLL e un file di intestazione. Per ulteriori informazioni, vedere [compilazione MIDL](midl-compilation.md) .
-   A seconda del metodo di marshalling scelto, scrivere un file di definizione di modulo (DEF), compilare e collegare tutti i file generati da MIDL in una singola DLL proxy e registrare l'interfaccia nel registro di sistema oppure registrare la libreria dei tipi. Per ulteriori informazioni, vedere [caricamento e registrazione di una libreria dei tipi](loading-and-registering-a-type-library.md) e [compilazione e registrazione di una DLL proxy](building-and-registering-a-proxy-dll.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anatomia di un file IDL](anatomy-of-an-idl-file.md)
</dt> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> <dt>

[Regole di progettazione dell'interfaccia](interface-design-rules.md)
</dt> <dt>

[Component Object Model (COM)](the-component-object-model.md)
</dt> </dl>

 

 