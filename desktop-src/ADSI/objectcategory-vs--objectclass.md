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
# <a name="objectcategory-vs-objectclass"></a><span data-ttu-id="52db2-105">objectCategory rispetto a objectClass</span><span class="sxs-lookup"><span data-stu-id="52db2-105">objectCategory vs. objectClass</span></span>

<span data-ttu-id="52db2-106">Entrambi gli attributi **objectCategory** e **objectClass** possono fare riferimento a una determinata classe di schema di un oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="52db2-106">Both the **objectCategory** and **objectClass** attributes can refer to a given schema class of a directory object.</span></span> <span data-ttu-id="52db2-107">Tuttavia, esiste una differenza importante nella semantica tra i due.</span><span class="sxs-lookup"><span data-stu-id="52db2-107">However, there is an important distinction in semantics between the two.</span></span> <span data-ttu-id="52db2-108">"objectClass = Joy" si riferisce a tali oggetti directory in cui "Joy" rappresenta qualsiasi classe nella gerarchia di classi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="52db2-108">"objectClass=joy" refers to such directory objects in which "joy" represents any class in the object class hierarchy.</span></span> <span data-ttu-id="52db2-109">"objectCategory = Joy", d'altra parte, si riferisce agli oggetti directory in cui "Joy" identifica una classe specifica nella gerarchia di classi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="52db2-109">"objectCategory=joy", on the other hand, refers to those directory objects in which "joy" identifies a specific class in the object class hierarchy.</span></span>

<span data-ttu-id="52db2-110">**objectClass** può assumere più valori, mentre **objectCategory** accetta un solo valore.</span><span class="sxs-lookup"><span data-stu-id="52db2-110">**objectClass** can take multiple values whereas **objectCategory** takes a single value.</span></span> <span data-ttu-id="52db2-111">Per questo motivo, **objectCategory** è più adatto per la corrispondenza dei tipi di oggetti in una ricerca di directory.</span><span class="sxs-lookup"><span data-stu-id="52db2-111">Because of this, **objectCategory** is better suited for type matching of objects in a directory search.</span></span> <span data-ttu-id="52db2-112">ADSI viene utilizzato come criterio di corrispondenza predefinito.</span><span class="sxs-lookup"><span data-stu-id="52db2-112">ADSI uses this as the default matching criterion.</span></span> <span data-ttu-id="52db2-113">Le ricerche con un **objectClass** non sono scalabili per database di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="52db2-113">Searches using one **objectClass** are not scalable to large databases.</span></span> <span data-ttu-id="52db2-114">ADSI supporta le sintassi "(objectCategory = SomeDN)" e "(objectCategory \_ = \_ nome visualizzato LDAP \_ della \_ classe)".</span><span class="sxs-lookup"><span data-stu-id="52db2-114">ADSI supports "(objectCategory=SomeDN)" and "(objectCategory=Ldap\_Display\_Name\_of\_Class)" syntaxes.</span></span>

<span data-ttu-id="52db2-115">L'unica eccezione è rappresentata dal fatto che il filtro di ricerca LDAP "(objectClass = \* )" non specifica una ricerca sulla classe di oggetti, ma verifica solo la presenza degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="52db2-115">The exception to all of this is that the LDAP search filter "(objectClass=\*)" does not specify a search on object class, but merely tests for the presence of the objects.</span></span>

 

 




