---
title: Requisiti del server DLL
description: Anche se la maggior parte delle DLL può essere eseguita in un surrogato, alcune DLL non possono.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 624b516f4b6c9deb00e3a093bd3531d3453e631450a1e5ec3b0810569580961a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993241"
---
# <a name="dll-server-requirements"></a>Requisiti del server DLL

Anche se la maggior parte delle DLL può essere eseguita in un surrogato, alcune DLL non possono.

La DLL deve avere un comportamento corretto se si vuole usare il surrogato fornito dal sistema. Ad esempio, una DLL che chiama i metodi che registrano i callback dal client tenterebbe di richiamare tali callback come se i puntatori a funzione ricevuti fossero per istruzioni nello spazio degli indirizzi, cosa che non è il caso. Analogamente, una DLL che usa una variabile globale a cui si aspetta che il client accedono non funzionerà. In generale, i parametri di cui non è possibile eseguire correttamente il marshalling impediranno l'esecuzione del server DLL all'esterno del processo client. In molti casi, è possibile scrivere un surrogato personalizzato appositamente progettato per compensare il comportamento "non corretto". Per altre informazioni, vedere [Scrittura di un surrogato personalizzato.](writing-a-custom-surrogate.md)

Se il server DLL usa interfacce personalizzate, è necessario assicurarsi che il codice di marshalling sia disponibile per tali interfacce. Ad esempio, è possibile compilare e registrare una DLL proxy o fornire e registrare una libreria dei tipi che consenta al server di funzionare correttamente durante l'esecuzione in un surrogato.

I server DLL verranno caricati solo in un processo surrogato in esecuzione nel contesto di sicurezza appropriato. Il contesto di sicurezza per il surrogato del server DLL viene determinato come per i server EXE. Il surrogato del server DLL viene eseguito nello stesso contesto di sicurezza del client, a meno che non venga impostato un valore **RunAs,** che determina il contesto di sicurezza, nella sezione del Registro di sistema [AppID](appid-clsid.md) per il server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Surrogati DLL](dll-surrogates.md)
</dt> </dl>

 

 




