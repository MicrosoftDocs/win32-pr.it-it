---
title: Ricerca del contenuto del dominio
description: Prima di illustrare la posizione di associazione per iniziare una ricerca di oggetti in un dominio, è utile comprendere la modalità di archiviazione dei dati in Active Directory Domain Services.
ms.assetid: fd0b4556-465b-4338-87cb-375450590c44
ms.tgt_platform: multiple
keywords:
- contenuto del dominio Active Directory
- ricerca di contenuti del dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c18cd879e950fd9c467f6674092947d430d8f87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044097"
---
# <a name="searching-domain-contents"></a>Ricerca del contenuto del dominio

Prima di illustrare la posizione di associazione per iniziare una ricerca di oggetti in un dominio, è utile comprendere la modalità di archiviazione dei dati in Active Directory Domain Services.

Se si dispone di una foresta con più di un dominio, Active Directory Domain Services non archivia tutti i dati oggetto in un singolo controller di dominio, per motivi di prestazioni, scalabilità e affidabilità. Un controller di dominio contiene tutte le informazioni sul dominio di cui è membro (dispone di una replica completa del dominio). Tuttavia, un controller di dominio non tiene le informazioni complete su nessun altro dominio.

Se si esegue l'associazione all'oggetto dominio con la ricerca dei riferimenti disabilitata, è possibile cercare qualsiasi oggetto in tale dominio e solo tale dominio. Per ulteriori informazioni sull'inseguimento dei riferimenti, vedere [riferimenti](referrals.md). Una ricerca può recuperare qualsiasi proprietà e può usare un filtro di query contenente qualsiasi proprietà.

In una foresta, i domini vengono disposti in modo gerarchico come alberi di dominio. Un albero di dominio può essere costituito da un solo dominio o da un dominio con uno o più domini figlio. Questi domini figlio, a loro volta, possono avere domini figlio al di sotto di essi. Un albero di dominio è anche uno spazio dei nomi contiguo. Uno spazio dei nomi contiguo significa che i domini figlio rappresentano una continuazione della gerarchia di denominazione. Ad esempio, un dominio fabrikam.com (o DC = Fabrikam, DC = COM) può avere un dominio figlio denominato divisione (mydivision.fabrikam.com o DC = didivision, DC = Fabrikam, DC = COM), che a sua volta potrebbe avere un dominio figlio denominato Mydev (mydev.mydivision.fabrikam.com o DC = Mydev, DC = didivision, DC = Fabrikam, DC = COM).

Se si esegue l'associazione a un oggetto di dominio (con la ricerca dei riferimenti attivata) per un dominio all'interno di un albero di dominio, si cercherà tale dominio e l'intera gerarchia al suo interno. La ricerca può recuperare qualsiasi proprietà e può usare un filtro di query contenente qualsiasi proprietà.

Se un controller di dominio contiene una replica completa del solo dominio, è possibile eseguire una ricerca di sottoalbero in un albero di dominio. Un dominio include riferimenti ai relativi domini figlio. Quando un controller di dominio elabora una richiesta di ricerca del sottoalbero rispetto al proprio dominio, il controller di dominio cerca tale dominio e quindi restituisce i riferimenti a ognuno dei relativi domini figlio al client. Un riferimento è il modo in cui un server di directory comunica che non contiene le informazioni necessarie per completare una richiesta, ad esempio una query, ma che contiene un riferimento a un server che può contenere le informazioni necessarie. Nel caso di una ricerca del sottoalbero di un albero di dominio, viene restituito un riferimento per ogni dominio figlio diretto, in modo che la ricerca possa essere continuata in un controller di dominio in ogni dominio figlio. Se la ricerca dei riferimenti è attivata, la libreria client LDAP (Wldap32.dll) usa tali riferimenti per eseguire il binding a un controller di dominio in ogni dominio figlio e continuare la ricerca. Se il rinvio è disattivato, il client LDAP non risolve i riferimenti e la ricerca viene completata.

Una ricerca di sottoalbero in un albero di dominio con l'indisponibilità di riferimento attivata può richiedere molto tempo se è presente una connessione lenta ai controller di dominio per i domini figlio. Se si desidera eseguire la ricerca solo in un singolo dominio, è necessario disattivare il riferimento per evitare di dover cercare inutilmente i domini figlio.

 

 




