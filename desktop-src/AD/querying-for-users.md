---
title: Esecuzione di query per gli utenti
description: Per eseguire una query per un utente, la query deve contenere l'espressione di ricerca \ 0034;( (utente objectClass) (objectCategory person)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- utenti AD, esecuzione di query per gli utenti
- Active Directory, utilizzo di, utenti, esecuzione di query per gli utenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39037ff805dab753aae066d1f6611432b28ea73c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724458"
---
# <a name="querying-for-users"></a>Esecuzione di query per gli utenti

Per eseguire una query per un utente, la query deve contenere l'espressione di ricerca "(& (objectClass = user) (objectCategory = person))".

Poiché la classe computer è una sottoclasse di User, una query contenente solo (objectClass = user) restituirà oggetti utente e computer. Inoltre, la categoria dell'oggetto utente è persona (non utente); Pertanto, l'espressione (objectCategory = user) non restituisce alcun utente. Se si utilizza l'espressione (objectCategory = person), la query restituisce oggetti utente e oggetti contatto.

Gli utenti possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio e nella radice del dominio. Questo significa che gli utenti possono trovarsi in numerose posizioni nella gerarchia di directory. È possibile eseguire una ricerca completa di "(objectCategory = user)" per trovare tutti gli utenti in un contenitore, in un'unità organizzativa, in un dominio, in un albero di dominio o in una foresta, a seconda dell'oggetto a cui è associato il puntatore [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) in uso.

 

 