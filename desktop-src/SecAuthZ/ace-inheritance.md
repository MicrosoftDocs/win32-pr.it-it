---
description: Un ACL di oggetti può contenere voci ACE ereditate dal relativo contenitore padre.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Ereditarietà ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967236"
---
# <a name="ace-inheritance"></a><span data-ttu-id="b8eb6-103">Ereditarietà ACE</span><span class="sxs-lookup"><span data-stu-id="b8eb6-103">ACE Inheritance</span></span>

<span data-ttu-id="b8eb6-104">L'ACL di un oggetto può contenere voci ACE ereditate dal relativo contenitore padre.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-104">An object's ACL can contain ACEs that it inherited from its parent container.</span></span> <span data-ttu-id="b8eb6-105">Una sottochiave del registro di sistema, ad esempio, può ereditare Ace dalla chiave precedente nella gerarchia del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-105">For example, a registry subkey can inherit ACEs from the key above it in the registry hierarchy.</span></span> <span data-ttu-id="b8eb6-106">Analogamente, un file in un file system NTFS può ereditare voci ACE dalla directory che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-106">Likewise, a file in an NTFS file system can inherit ACEs from the directory that contains it.</span></span>

<span data-ttu-id="b8eb6-107">La struttura dell' [**\_ intestazione ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) di una voce ACE contiene un set di flag di ereditarietà che controllano l'ereditarietà della voce ACE e l'effetto di una voce ACE sull'oggetto a cui è collegato.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-107">The [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure of an ACE contains a set of inheritance flags that control ACE inheritance and the effect of an ACE on the object to which it is attached.</span></span> <span data-ttu-id="b8eb6-108">Il sistema interpreta i flag di ereditarietà e altre informazioni sull'ereditarietà in base alle [regole dell'ereditarietà Ace](ace-inheritance-rules.md).</span><span class="sxs-lookup"><span data-stu-id="b8eb6-108">The system interprets the inheritance flags and other inheritance information according to the [rules of ACE inheritance](ace-inheritance-rules.md).</span></span>

<span data-ttu-id="b8eb6-109">Queste regole sono state migliorate con le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8eb6-109">These rules have been enhanced with the following features:</span></span>

-   <span data-ttu-id="b8eb6-110">Supporto per la [propagazione automatica di ACE ereditabili](automatic-propagation-of-inheritable-aces.md).</span><span class="sxs-lookup"><span data-stu-id="b8eb6-110">Support for [automatic propagation of inheritable ACEs](automatic-propagation-of-inheritable-aces.md).</span></span>
-   <span data-ttu-id="b8eb6-111">Flag che distingue le voci ACE ereditate e le voci ACE che sono state applicate direttamente a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-111">A flag that differentiates between inherited ACEs and ACEs that were directly applied to an object.</span></span>
-   <span data-ttu-id="b8eb6-112">Voci ACE specifiche dell'oggetto che consentono di specificare il tipo di oggetto figlio che può ereditare la voce ACE.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-112">Object-specific ACEs that allow you to specify the type of child object that can inherit the ACE.</span></span>
-   <span data-ttu-id="b8eb6-113">La possibilità di impedire a un DACL o un SACL di ereditare le voci ACE mediante l'impostazione dei bit protetti da SE \_ DACL \_ o se \_ SACL \_ nei bit di controllo del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) , ad eccezione di Ace attributo della risorsa di sistema \_ \_ \_ e \_ ACE con ID criteri con ambito di sistema \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b8eb6-113">The ability to prevent a DACL or SACL from inheriting ACEs by setting the SE\_DACL\_PROTECTED or SE\_SACL\_PROTECTED bits in the [*security descriptor's*](/windows/desktop/SecGloss/s-gly) control bits except for SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE and SYSTEM\_SCOPED\_POLICY\_ID\_ACE.</span></span>

 

 
