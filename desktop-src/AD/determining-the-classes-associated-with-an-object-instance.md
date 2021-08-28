---
title: Determinazione delle classi associate a un'istanza di oggetto
description: Ogni oggetto in Active Directory Domain Services ha due attributi i cui valori identificano la gerarchia delle classi di oggetti di cui l'oggetto è un'istanza.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af65b5e1abf7f0bc68ae115cb409d2cdb556e08
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471497"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Determinazione delle classi associate a un'istanza di oggetto

Ogni oggetto in Active Directory Domain Services ha due attributi i cui valori identificano la gerarchia delle classi di oggetti di cui l'oggetto è un'istanza.




| Attributo | Descrizione | 
|-----------|-------------|
| <strong>structuralObjectClass</strong> | Identifica le classi strutturali e astratte di cui l'oggetto è un'istanza. Ad esempio, i valori per un oggetto utente possono essere:<ul><li><strong>top</strong></li><li><strong>Persona</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 
| <strong>Objectclass</strong> | Identifica le classi incluse in <strong>structuralObjectClass</strong>e tutte le classi ausiliarie collegate dinamicamente. Ad esempio, se una classe ausiliaria "veicolo" è collegata a un oggetto utente, i valori possono essere:<ul><li><strong>top</strong></li><li><strong>Veicolo</strong></li><li><strong>Persona</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 




 

Tenere presente che nessuno di questi attributi include classi ausiliarie collegate in modo statico alle classi di oggetti di cui l'oggetto è un'istanza. Ad esempio, la classe ausiliaria **securityPrincipal** è  collegata in modo statico alla classe utente perché è inclusa nei valori **systemAuxiliaryClass** dell'oggetto **user classSchema.** non è incluso negli attributi **objectClass** o **structuralObjectClass** delle istanze della classe utente.

 

 




