---
title: Identificatori di visualizzazione
description: In Active Directory Domain Services, una classe di oggetti o una classe definisce un tipo di oggetto che può essere creato in Active Directory Domain Services.
ms.assetid: 0c31b02b-9fd3-4547-9ebc-d511a10d7106
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be9df0b81427bafa6ebe6707a33e86b6aff7416
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956337"
---
# <a name="display-specifiers"></a>Identificatori di visualizzazione

In Active Directory Domain Services, una classe di oggetti o una classe definisce un tipo di oggetto che può essere creato in Active Directory Domain Services. La definizione di ogni classe di oggetti viene archiviata come oggetto [**classSchema**](/windows/desktop/ADSchema/c-classschema) nello [schema Active Directory](active-directory-schema.md). Oltre alla definizione **classSchema** , ogni classe di oggetti può avere uno o più identificatori di visualizzazione che specificano i dati dell'interfaccia utente per gli oggetti di tale classe.

Un identificatore di visualizzazione è un oggetto della classe [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) . Gli attributi di un oggetto **displaySpecifier** specificano i dati localizzati dell'interfaccia utente che descrivono i vari elementi dell'interfaccia utente per una particolare classe di oggetti. Gli identificatori di visualizzazione archiviano i dati per le finestre delle proprietà, i menu di scelta rapida, le icone, le creazioni guidate e i nomi delle classi e degli attributi Per le pagine delle proprietà e i menu di scelta rapida, la shell di Windows e Active Directory gli snap-in amministrativi utilizzano questi dati per creare interfacce utente diverse per gli amministratori e gli utenti finali: un set di pagine delle proprietà e/o menu di scelta rapida può essere associato a applicazioni amministrative, mentre un set di elementi diverso può essere associato alle applicazioni dell'utente finale.

Gli oggetti [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) vengono archiviati in contenitori specifici delle impostazioni locali nel contenitore DisplaySpecifiers del contenitore di configurazione, che viene replicato in tutti i controller di dominio della foresta aziendale. Il contenitore DisplaySpecifiers contiene sottocontenitori che corrispondono alle diverse impostazioni locali supportate dall'installazione aziendale. Questi sottocontenitori vengono denominati usando gli identificatori di lingua. Ad esempio, il nome del contenitore delle impostazioni locali per US-English è 409, che corrisponde all'identificatore di lingua esadecimale, 0x0409. Una classe di oggetti può quindi avere più identificatori di visualizzazione: uno in ogni sottocontenitore delle impostazioni locali. Per ulteriori informazioni e per un elenco di identificatori di lingua possibili, vedere [costanti e stringhe dell'identificatore di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings). Per ulteriori informazioni sulle impostazioni locali, vedere [impostazioni locali e lingue](/windows/desktop/Intl/locales-and-languages).

Il nome di un oggetto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) viene creato aggiungendo la stringa "-display" al [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) della classe dell'oggetto. Ad esempio, il nome di un oggetto **displaySpecifier** per la classe [**utente**](/windows/desktop/ADSchema/c-user) è "user-Display".

È possibile aggiungere, eliminare o modificare le proprietà degli oggetti [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) di una classe per specificare gli elementi dell'interfaccia utente (nome della classe, nomi degli attributi, finestre delle proprietà, menu di scelta rapida, icona e così via) che vengono visualizzati per ogni istanza di un oggetto di tale classe.

Per ulteriori informazioni sugli identificatori di visualizzazione, vedere [contenitore DisplaySpecifiers](displayspecifiers-container.md).

 

 