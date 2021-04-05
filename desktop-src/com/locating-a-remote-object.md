---
title: Individuazione di un oggetto remoto
description: Individuazione di un oggetto remoto
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873034"
---
# <a name="locating-a-remote-object"></a>Individuazione di un oggetto remoto

Con l'avvento di COM per sistemi distribuiti, COM utilizza il modello di base per la creazione di oggetti descritti in [oggetti e CLSID della classe com](com-class-objects-and-clsids.md) e aggiunge più di un modo per individuare un oggetto che potrebbe trovarsi in un altro sistema in una rete, senza sovraccaricare l'applicazione client.

COM ha aggiunto chiavi del registro di sistema che consentono a un server di registrare il nome del computer in cui risiede o il computer in cui si trova una risorsa di archiviazione esistente. Pertanto, le applicazioni client devono essere in grado di comprendere solo il CLSID del server.

Tuttavia, per i casi in cui si desidera, COM ha sostituito un parametro precedentemente riservato di [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con una struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , che consente a un client di specificare il percorso di un server. Un altro importante valore nella funzione **CoGetClassObject** è l'enumerazione [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) , che specifica se l'oggetto previsto deve essere eseguito in-process, out-of-process locale o out-of-process remote. Insieme, questi due valori e i valori nel registro di sistema determinano come e dove deve essere eseguito l'oggetto.

> [!Note]  
> Per la creazione di istanze, quando specificano un percorso del server, può eseguire l'override di un'impostazione del registro di sistema. L'algoritmo COM utilizzato per eseguire questa operazione è descritto nel riferimento per l'enumerazione [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) .

 

L'attivazione remota dipende dalla relazione di sicurezza tra client e server. Per ulteriori informazioni, vedere [sicurezza in com](security-in-com.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti classe COM e CLSID](com-class-objects-and-clsids.md)
</dt> <dt>

[Creazione di un oggetto tramite un oggetto classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 