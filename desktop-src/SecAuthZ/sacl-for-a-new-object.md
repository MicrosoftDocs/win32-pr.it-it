---
description: SACL per un nuovo oggetto
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL per un nuovo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308139"
---
# <a name="sacl-for-a-new-object"></a><span data-ttu-id="6e805-103">SACL per un nuovo oggetto</span><span class="sxs-lookup"><span data-stu-id="6e805-103">SACL for a New Object</span></span>

<span data-ttu-id="6e805-104">Il sistema utilizza l'algoritmo seguente per compilare un SACL per la maggior parte dei tipi di nuovi oggetti a protezione diretta:</span><span class="sxs-lookup"><span data-stu-id="6e805-104">The system uses the following algorithm to build a SACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="6e805-105">Il SACL dell'oggetto è l'elenco SACL del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) specificato dal creatore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6e805-105">The object's SACL is the SACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="6e805-106">Il sistema unisce tutte le voci ACE ereditabili nell'elenco SACL specificato, a meno che non \_ \_ sia impostato il bit protetto di se nei bit di controllo del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6e805-106">The system merges any inheritable ACEs into the specified SACL unless the SE\_SACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span> <span data-ttu-id="6e805-107">\_Le voci \_ ACE degli attributi delle risorse di sistema \_ e \_ \_ \_ le voci ACE con ambito di sistema di \_ un oggetto padre verranno unite a un nuovo oggetto anche se \_ \_ è impostato il bit protetto se SACL.</span><span class="sxs-lookup"><span data-stu-id="6e805-107">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs and SYSTEM\_SCOPED\_POLICY\_ID\_ACEs from a parent object will be merged to a new object even if the SE\_SACL\_PROTECTED bit is set.</span></span>
2.  <span data-ttu-id="6e805-108">Se il creatore non specifica un descrittore di sicurezza, il sistema compila il SACL dell'oggetto da ACE ereditabili.</span><span class="sxs-lookup"><span data-stu-id="6e805-108">If the creator does not specify a security descriptor, the system builds the object's SACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="6e805-109">Se non esiste alcun SACL specificato o ereditato, l'oggetto non dispone di SACL.</span><span class="sxs-lookup"><span data-stu-id="6e805-109">If there is no specified or inherited SACL, the object has no SACL.</span></span>

<span data-ttu-id="6e805-110">Per specificare un SACL per un nuovo oggetto, il creatore dell'oggetto deve avere il privilegio SE il \_ nome di sicurezza è \_ abilitato. [](privileges.md)</span><span class="sxs-lookup"><span data-stu-id="6e805-110">To specify a SACL for a new object, the object's creator must have the SE\_SECURITY\_NAME [privilege](privileges.md) enabled.</span></span> <span data-ttu-id="6e805-111">Se il SACL specificato per un nuovo oggetto contiene solo \_ ACE attributo risorsa di sistema \_ \_ , il privilegio se il \_ nome di sicurezza \_ non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e805-111">If the specified SACL for a new object contain only SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs, then the SE\_SECURITY\_NAME privilege is not required.</span></span> <span data-ttu-id="6e805-112">Il creatore non necessita di questo privilegio se il SACL dell'oggetto viene compilato dalle voci ACE ereditate.</span><span class="sxs-lookup"><span data-stu-id="6e805-112">The creator does not need this privilege if the object's SACL is built from inherited ACEs.</span></span>

<span data-ttu-id="6e805-113">Il sistema utilizza un algoritmo diverso per compilare un SACL per un nuovo oggetto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6e805-113">The system uses a different algorithm to build a SACL for a new Active Directory object.</span></span> <span data-ttu-id="6e805-114">Per ulteriori informazioni, vedere [la pagina relativa alla modalità di impostazione dei descrittori di sicurezza per i nuovi oggetti directory](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="6e805-114">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
