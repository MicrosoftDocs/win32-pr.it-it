---
title: Decidere cosa trovare
description: Prima di eseguire la ricerca in una directory, valutare il modo in cui la ricerca viene eseguita in base al proprio approccio. I dati e le proprietà da restituire influiscono sul punto in cui si esegue l'associazione per avviare una ricerca, la profondità della ricerca, il filtro di query e le prestazioni di ricerca.
ms.assetid: 788fa12c-9086-4d8b-bd2e-e96a494a26ad
ms.tgt_platform: multiple
keywords:
- criteri di ricerca Active Directory
- decidere quali elementi trovare Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818b0f9be56830a836453c5e52ceadd52928a522
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044136"
---
# <a name="deciding-what-to-find"></a>Decidere cosa trovare

Prima di eseguire la ricerca in una directory, valutare il modo in cui la ricerca viene eseguita in base al proprio approccio. I dati e le proprietà da restituire influiscono sul punto in cui si esegue l'associazione per avviare una ricerca, la profondità della ricerca, il filtro di query e le prestazioni di ricerca.

Ad esempio, se si desidera cercare tutti gli oggetti utente con il cognome Smith:



| Area                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posizione in cui eseguire la ricerca            | Un contenitore o unità organizzativa (OU) specifico all'interno di un dominio, un dominio specifico, un albero di dominio specifico o l'intera foresta. Se si esegue la ricerca di oggetti all'interno di un contenitore o di un dominio specifico, la query di ricerca offrirà prestazioni migliori associando direttamente al contenitore o al dominio anziché eseguire una ricerca di sottoalbero in un albero di dominio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Tipo di ricerca             | Se si verifica l'esistenza di o si recuperano le proprietà di un particolare oggetto con un nome distinto (DN) già noto, è consigliabile eseguire una ricerca di base che cerca solo l'oggetto associato.<br/> Se si sa che un oggetto è un discendente diretto di un determinato contenitore, eseguire l'associazione a tale contenitore ed eseguire una ricerca a un livello (gli oggetti **attributeSchema** e **classSchema** nel contenitore dello schema e gli oggetti estesi nel contenitore dei diritti estesi sono ottimi esempi).<br/> Se non si conosce esattamente il punto in cui si trova l'oggetto o se si desidera eseguire una ricerca nell'oggetto associato e in tutti gli oggetti figlio sotto di esso nella gerarchia di directory, eseguire una ricerca di sottoalbero.<br/>                                                       |
| Usare gli indici laddove possibile | Infine, se si cerca una classe specifica di oggetto, è necessario che il filtro di query includa espressioni che valutano le proprietà definite per la classe.<br/> Per cercare oggetti gruppo, includere l'espressione (objectCategory = Group) nel filtro. Per cercare gli oggetti utente, specificare (& (objectClass = user) (objectCategory = person)) poiché la classe computer deriva dalla classe User, quindi (objectClass = user) restituirà sia utenti che computer e anche perché sia gli oggetti contatto sia gli oggetti utente hanno un **objectCategory** di persona, quindi (objectCategory = person) restituiranno sia utenti che contatti.<br/> Per altre informazioni, vedere [classe di oggetti e categoria di oggetti](object-class-and-object-category.md) e [attributi indicizzati](indexed-attributes.md).<br/> |



 

 

 





