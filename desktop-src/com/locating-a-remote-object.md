---
title: Individuazione di un oggetto remoto
description: Individuazione di un oggetto remoto
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96577ddd018ab6b00c5af59a9824984c1ffe255dc91849b4391b256b493b765a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992451"
---
# <a name="locating-a-remote-object"></a>Individuazione di un oggetto remoto

Con l'avvento di COM per i sistemi distribuiti, COM usa il modello di base per la creazione di oggetti descritto in Oggetti classe COM e [CLSID](com-class-objects-and-clsids.md) e aggiunge più di un modo per individuare un oggetto che potrebbe risiedere in un altro sistema in una rete, senza sovraccaricare l'applicazione client.

COM ha aggiunto chiavi del Registro di sistema che consentono a un server di registrare il nome del computer in cui risiede o il computer in cui si trova una memoria esistente. Pertanto, le applicazioni client devono conoscere solo il CLSID del server.

Tuttavia, nei casi in cui si desidera, COM ha sostituito un parametro precedentemente riservato [**di CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con una [**struttura COSERVERINFO,**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) che consente a un client di specificare la posizione di un server. Un altro valore importante nella funzione **CoGetClassObject** è l'enumerazione [**CLSCTX,**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) che specifica se l'oggetto previsto deve essere eseguito in-process, out-of-process locale o out-of-process remoto. Nel loro insieme, questi due valori e i valori nel Registro di sistema determinano come e dove eseguire l'oggetto.

> [!Note]  
> Le chiamate di creazione di istanze, quando specificano un percorso del server, possono eseguire l'override di un'impostazione del Registro di sistema. L'algoritmo utilizzato da COM per eseguire questa operazione è descritto nel riferimento per [**l'enumerazione CLSCTX.**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)

 

L'attivazione remota dipende dalla relazione di sicurezza tra client e server. Per altre informazioni, vedere [Sicurezza in COM.](security-in-com.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti classe COM e CLSID](com-class-objects-and-clsids.md)
</dt> <dt>

[Creazione di un oggetto tramite un oggetto classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 