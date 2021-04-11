---
title: objectCategory rispetto a objectClass
description: Entrambi gli attributi objectCategory e objectClass possono fare riferimento a una determinata classe di schema di un oggetto directory.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory e objectClass ADSI
- attributi ASI, ricerca sugli attributi objectCategory e objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044061"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory rispetto a objectClass

Entrambi gli attributi **objectCategory** e **objectClass** possono fare riferimento a una determinata classe di schema di un oggetto directory. Tuttavia, esiste una differenza importante nella semantica tra i due. "objectClass = Joy" si riferisce a tali oggetti directory in cui "Joy" rappresenta qualsiasi classe nella gerarchia di classi di oggetti. "objectCategory = Joy", d'altra parte, si riferisce agli oggetti directory in cui "Joy" identifica una classe specifica nella gerarchia di classi di oggetti.

**objectClass** può assumere più valori, mentre **objectCategory** accetta un solo valore. Per questo motivo, **objectCategory** è più adatto per la corrispondenza dei tipi di oggetti in una ricerca di directory. ADSI viene utilizzato come criterio di corrispondenza predefinito. Le ricerche con un **objectClass** non sono scalabili per database di grandi dimensioni. ADSI supporta le sintassi "(objectCategory = SomeDN)" e "(objectCategory \_ = \_ nome visualizzato LDAP \_ della \_ classe)".

L'unica eccezione è rappresentata dal fatto che il filtro di ricerca LDAP "(objectClass = \* )" non specifica una ricerca sulla classe di oggetti, ma verifica solo la presenza degli oggetti.

 

 




