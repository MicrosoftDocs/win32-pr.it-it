---
title: Definizione di interfacce COM
description: Microsoft definisce molte interfacce COM. Nella maggior parte dei casi, è possibile riutilizzare queste interfacce generiche. Tuttavia, alcune applicazioni hanno requisiti specifici che rendono auspicabile o necessario definire interfacce a oggetti personalizzate.
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e676172e51fca810f0cbb7ba93b5d52b814319b6e8b890f20ba9c51617f7ac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071021"
---
# <a name="defining-com-interfaces"></a>Definizione di interfacce COM

Microsoft definisce molte interfacce COM. Nella maggior parte dei casi, è possibile riutilizzare queste interfacce generiche. Tuttavia, alcune applicazioni hanno requisiti specifici che rendono auspicabile o necessario definire interfacce a oggetti personalizzate.

Tutte le interfacce COM devono derivare, direttamente o indirettamente, [**dall'interfaccia IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) All'interno di tale vincolo, l'interfaccia personalizzata può supportare quasi tutti i metodi o i parametri, inclusi i metodi asincroni. È anche possibile generare una libreria dei tipi per le interfacce personalizzate in modo che i client possano accedere alle informazioni sui metodi dell'oggetto in fase di esecuzione. Dopo aver definito un'interfaccia, descriverla in Microsoft Interface Definition Language (MIDL), compilarla e registrarla, usarla come qualsiasi interfaccia generica. Con COM distribuito, i metodi di interfaccia sono disponibili sia per i processi remoti che per altri processi nello stesso computer.

Infine, la compilazione di interfacce COM richiede un ambiente di sviluppo che include un compilatore C/C++ e il Midl.exe di compilazione.

I passaggi per la creazione di un'interfaccia COM sono i seguenti:

-   Decidere come si vuole fornire il supporto del marshalling per l'interfaccia. con il marshalling basato su libreria dei tipi o con una DLL proxy/stub. È necessario effettuare il marshalling anche delle interfacce in-process se devono essere usate attraverso i limiti dell'apartment. È buona idea creare il supporto per il marshalling in ogni interfaccia COM, anche se non si pensa che sarà necessario. Per [altre informazioni, vedere Marshalling](interface-marshaling.md) dell'interfaccia.
-   Descrivere l'interfaccia o le interfacce in un file di definizione dell'interfaccia (IDL). Inoltre, è possibile specificare alcuni aspetti locali dell'interfaccia in un file di configurazione dell'applicazione (ACF). Se si usa il marshalling basato su [](/windows/desktop/Midl/library) libreria dei tipi, aggiungere un'istruzione di libreria che faccia riferimento alle interfacce per cui si desidera generare informazioni sul tipo.
-   Usare il compilatore MIDL per generare un file della libreria dei tipi e un file di intestazione o file proxy/stub del linguaggio C, file di identificatore di interfaccia, file di dati DLL e file di intestazione. Per [altre informazioni, vedere Compilazione MIDL.](midl-compilation.md)
-   A seconda del metodo di marshalling scelto, scrivere un file di definizione del modulo (DEF), compilare e collegare tutti i file generati da MIDL in una singola DLL proxy e registrare l'interfaccia nel Registro di sistema o registrare la libreria dei tipi. Per [altre informazioni, vedere Caricamento e registrazione di una libreria dei tipi](loading-and-registering-a-type-library.md) e Compilazione e registrazione di una DLL [proxy.](building-and-registering-a-proxy-dll.md)

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

 

 