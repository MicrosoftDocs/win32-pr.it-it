---
title: ObjectCategory e objectClass
description: Entrambi gli attributi objectCategory e objectClass possono fare riferimento a una determinata classe di schema di un oggetto directory.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- ObjectCategory e objectClass ADSI
- attributi ASI, ricerca di attributi objectCategory e objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3833f8cf26cb2272fbe1e7c1063322f39a8c0147e4b22382d26067f90e72e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839221"
---
# <a name="objectcategory-vs-objectclass"></a>ObjectCategory e objectClass

Entrambi gli **attributi objectCategory** **e objectClass** possono fare riferimento a una determinata classe di schema di un oggetto directory. Esiste tuttavia una distinzione importante nella semantica tra i due. "objectClass=joy" si riferisce a tali oggetti directory in cui "joy" rappresenta qualsiasi classe nella gerarchia di classi di oggetti. "objectCategory=joy", d'altra parte, fa riferimento agli oggetti directory in cui "joy" identifica una classe specifica nella gerarchia delle classi di oggetti.

**objectClass** può assumere più valori, mentre **objectCategory** accetta un singolo valore. Per questo scopo, **objectCategory** è più adatto per la corrispondenza dei tipi di oggetti in una ricerca di directory. ADSI usa questo criterio come criterio di corrispondenza predefinito. Le ricerche che usano **un oggettoClass** non sono scalabili in database di grandi dimensioni. ADSI supporta le sintassi "(objectCategory=SomeDN)" e "(objectCategory=Ldap \_ Display \_ Name of \_ \_ Class)".

L'eccezione a tutto questo è che il filtro di ricerca LDAP "(objectClass= )" non specifica una ricerca nella classe di oggetti, ma semplicemente verifica la \* presenza degli oggetti.

 

 




