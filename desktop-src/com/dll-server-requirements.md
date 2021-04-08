---
title: Requisiti del server DLL
description: Sebbene la maggior parte delle dll possa essere eseguita in un surrogato, alcune dll non possono.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045368"
---
# <a name="dll-server-requirements"></a>Requisiti del server DLL

Sebbene la maggior parte delle dll possa essere eseguita in un surrogato, alcune dll non possono.

Se si desidera utilizzare il surrogato fornito dal sistema, la DLL deve essere ben compensata. Ad esempio, una DLL che chiama i metodi che registrano i callback dal client tenterà di richiamare tali callback come se i puntatori a funzione ricevuti fossero per istruzioni nello spazio degli indirizzi, che non è il caso. Analogamente, una DLL che usa una variabile globale a cui si aspetta che il client acceda non funzionerà. In generale, i parametri per i quali non è possibile effettuare il marshalling in modo corretto impediscono l'esecuzione del server DLL all'esterno del processo client. In molti casi, è possibile scrivere un surrogato personalizzato progettato appositamente per compensare il comportamento "errato". Per ulteriori informazioni, vedere [scrittura di un surrogato personalizzato](writing-a-custom-surrogate.md).

Se il server DLL utilizza interfacce personalizzate, è necessario assicurarsi che il codice di marshalling sia disponibile per tali interfacce. Ad esempio, è possibile compilare e registrare una DLL proxy oppure fornire e registrare una libreria dei tipi che consenta al server di funzionare correttamente durante l'esecuzione in un surrogato.

I server DLL verranno caricati solo in un processo surrogato in esecuzione nel contesto di sicurezza appropriato. Il contesto di sicurezza per il surrogato del server DLL viene determinato in modo analogo ai server EXE. Il surrogato del server DLL viene eseguito nello stesso contesto di sicurezza del client, a meno che non sia impostato un valore **RunAs** , che determina il contesto di sicurezza, nella sezione del registro di sistema [AppID](appid-clsid.md) per il server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Surrogati DLL](dll-surrogates.md)
</dt> </dl>

 

 




