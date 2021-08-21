---
title: Controllo di accesso e creazione di oggetti
description: Il server Active Directory non riuscirà a creare un oggetto figlio se il chiamante non dispone di ADS RIGHT DS CREATE CHILD per tale tipo di oggetto \_ \_ nel \_ \_ contenitore padre.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- Controllo di accesso e creazione di oggetti AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b99251cd9c9c93177e0b6cfc362c7003078c870e809b48c9aba351e620e1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025724"
---
# <a name="access-control-and-object-creation"></a>Controllo di accesso e creazione di oggetti

Il server Active Directory non riuscirà a creare un oggetto figlio se il chiamante non dispone di **ADS \_ RIGHT \_ DS \_ CREATE \_ CHILD** per tale tipo di oggetto nel contenitore padre. Per determinare i tipi di oggetti figlio che il chiamante può creare in un oggetto directory, leggere l'attributo **allowedChildClassesEffective** dell'oggetto.

Quando si usa il [**metodo IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) per creare un oggetto figlio, l'oggetto non viene reso persistente fino a quando non viene chiamato [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) sul nuovo oggetto. Tra le **chiamate Create** **e SetInfo,** il thread di creazione può inserire valori in una delle proprietà del nuovo oggetto. Dopo la **chiamata a SetInfo,** il thread di creazione non dispone necessariamente dei diritti di accesso per impostare le proprietà del nuovo oggetto. Per assicurarsi che il chiamante abbia questi diritti, specificare un descrittore di sicurezza esplicito durante la creazione. L'elenco DACL deve avere una ACE che fornisce al chiamante i diritti di accesso necessari per l'oggetto.

Per altre informazioni sul controllo di accesso e sulla creazione di oggetti, vedere Come vengono impostati i descrittori di sicurezza [nei nuovi oggetti directory](how-security-descriptors-are-set-on-new-directory-objects.md).

 

 