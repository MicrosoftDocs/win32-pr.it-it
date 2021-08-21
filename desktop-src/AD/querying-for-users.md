---
title: Esecuzione di query per gli utenti
description: Per eseguire una query per un utente, la query deve contenere l'espressione di ricerca \ 0034;( (objectClass user) (objectCategory person)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- users AD , esecuzione di query per gli utenti
- Active Directory, uso, utenti, query per gli utenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae6939cef858c3dfc108611a1b0e7ab0367c302a091ca436c9c69b2fb5277b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025319"
---
# <a name="querying-for-users"></a>Esecuzione di query per gli utenti

Per eseguire una query per un utente, la query deve contenere l'espressione di ricerca "(&(objectClass=user)(objectCategory=person))".

Poiché la classe computer è una sottoclasse di user, una query contenente solo (objectClass=user) restituirebbe oggetti utente e oggetti computer. Inoltre, la categoria di oggetti dell'oggetto utente è person (non user); Pertanto, l'espressione (objectCategory=user) non restituisce alcun utente. Se si usa l'espressione (objectCategory=person), la query restituisce gli oggetti utente e gli oggetti contatto.

Gli utenti possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio, nonché nella radice del dominio. Ciò significa che gli utenti possono essere in numerose posizioni nella gerarchia di directory. È possibile eseguire una ricerca approfondita di "(objectCategory=user)" per trovare tutti gli utenti in un contenitore, un'unità organizzativa, un dominio, un albero di dominio o una foresta, a seconda dell'oggetto a cui è associato il puntatore [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) in uso.

 

 