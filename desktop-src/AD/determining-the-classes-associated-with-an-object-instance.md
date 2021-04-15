---
title: Determinazione delle classi associate a un'istanza dell'oggetto
description: Ogni oggetto in Active Directory Domain Services dispone di due attributi i cui valori identificano la gerarchia delle classi di oggetti di cui l'oggetto è un'istanza.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bc3fe900170e4a856d996f7e373918f242df2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470931"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a><span data-ttu-id="a4b4a-103">Determinazione delle classi associate a un'istanza dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="a4b4a-103">Determining the Classes Associated With an Object Instance</span></span>

<span data-ttu-id="a4b4a-104">Ogni oggetto in Active Directory Domain Services dispone di due attributi i cui valori identificano la gerarchia delle classi di oggetti di cui l'oggetto è un'istanza.</span><span class="sxs-lookup"><span data-stu-id="a4b4a-104">Every object in Active Directory Domain Services has two attributes whose values identify the hierarchy of object classes of which the object is an instance.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4b4a-105">Attributo</span><span class="sxs-lookup"><span data-stu-id="a4b4a-105">Attribute</span></span></th>
<th><span data-ttu-id="a4b4a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4b4a-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4b4a-107"><strong>structuralObjectClass</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-107"><strong>structuralObjectClass</strong></span></span></td>
<td><span data-ttu-id="a4b4a-108">Identifica le classi strutturali e astratte di cui l'oggetto è un'istanza.</span><span class="sxs-lookup"><span data-stu-id="a4b4a-108">Identifies the structural and abstract classes of which the object is an instance.</span></span> <span data-ttu-id="a4b4a-109">Ad esempio, i valori per un oggetto utente possono essere:</span><span class="sxs-lookup"><span data-stu-id="a4b4a-109">For example, the values for a user object can be:</span></span>
<ul>
<li><span data-ttu-id="a4b4a-110"><strong>top</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-110"><strong>top</strong></span></span></li>
<li><span data-ttu-id="a4b4a-111"><strong>persona</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-111"><strong>person</strong></span></span></li>
<li><span data-ttu-id="a4b4a-112"><strong>organizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-112"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="a4b4a-113"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-113"><strong>user</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4b4a-114"><strong>objectClass</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-114"><strong>objectClass</strong></span></span></td>
<td><span data-ttu-id="a4b4a-115">Identifica le classi incluse in <strong>StructuralObjectClass</strong>, oltre a tutte le classi ausiliarie collegate in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="a4b4a-115">Identifies the classes included in <strong>structuralObjectClass</strong>, plus any auxiliary classes that are dynamically attached.</span></span> <span data-ttu-id="a4b4a-116">Se ad esempio una &quot; &quot; classe ausiliaria del veicolo è collegata a un oggetto utente, i valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="a4b4a-116">For example, if a &quot;vehicle&quot; auxiliary class is attached to a user object, the values can be:</span></span>
<ul>
<li><span data-ttu-id="a4b4a-117"><strong>top</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-117"><strong>top</strong></span></span></li>
<li><span data-ttu-id="a4b4a-118"><strong>veicolo</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-118"><strong>vehicle</strong></span></span></li>
<li><span data-ttu-id="a4b4a-119"><strong>persona</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-119"><strong>person</strong></span></span></li>
<li><span data-ttu-id="a4b4a-120"><strong>organizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-120"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="a4b4a-121"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="a4b4a-121"><strong>user</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a4b4a-122">Tenere presente che nessuno di questi attributi include classi ausiliarie collegate staticamente con le classi di oggetti di cui l'oggetto è un'istanza.</span><span class="sxs-lookup"><span data-stu-id="a4b4a-122">Be aware that neither of these attributes include auxiliary classes that are statically linked with the object classes of which the object is an instance.</span></span> <span data-ttu-id="a4b4a-123">Ad esempio, la classe ausiliaria **securityPrincipal** è collegata in modo statico alla classe **utente** perché è inclusa nei valori **systemAuxiliaryClass** dell'oggetto **classSchema** dell'utente. non è incluso negli attributi **objectClass** o **StructuralObjectClass** delle istanze della classe User.</span><span class="sxs-lookup"><span data-stu-id="a4b4a-123">For example, the **securityPrincipal** auxiliary class is statically linked with the **user** class because it is included in the **systemAuxiliaryClass** values of the user **classSchema** object; it is not included in either the **objectClass** or **structuralObjectClass** attributes of instances of the user class.</span></span>

 

 




