---
title: Controllo di accesso e creazione di oggetti
description: Il server di Active Directory non riuscirà a creare un oggetto figlio se il chiamante non dispone del \_ \_ dominio di creazione del dominio per la \_ creazione di un \_ elemento figlio per quel tipo di oggetto nel contenitore padre.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- Active Directory per la creazione di oggetti e controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ac54c1fe71a1821d3a02db383ca95606ae360d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117510"
---
# <a name="access-control-and-object-creation"></a>Controllo di accesso e creazione di oggetti

Il server di Active Directory non riuscirà a creare un oggetto figlio se il chiamante non dispone del dominio di creazione del dominio per la creazione di un **\_ \_ \_ \_ elemento figlio** per quel tipo di oggetto nel contenitore padre. Per determinare i tipi di oggetti figlio che il chiamante può creare in un oggetto directory, leggere l'attributo **allowedChildClassesEffective** dell'oggetto.

Quando si usa il metodo [**IADsContainer:: create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) per creare un oggetto figlio, l'oggetto non viene reso persistente fino a quando non viene chiamato [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) sul nuovo oggetto. Tra le chiamate **create** e **SetInfo** , il thread di creazione può inserire i valori in qualsiasi proprietà del nuovo oggetto. Dopo la chiamata a **SetInfo** , il thread di creazione non dispone necessariamente dei diritti di accesso per impostare le proprietà del nuovo oggetto. Per assicurarsi che il chiamante disponga di questi diritti, specificare un descrittore di sicurezza esplicito durante la creazione. L'elenco DACL deve avere una voce ACE che fornisce al chiamante i diritti di accesso necessari per l'oggetto.

Per ulteriori informazioni sul controllo di accesso e la creazione di oggetti, vedere [la pagina relativa alla modalità di impostazione dei descrittori di sicurezza per i nuovi oggetti directory](how-security-descriptors-are-set-on-new-directory-objects.md).

 

 