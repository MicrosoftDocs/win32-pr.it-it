---
description: DACL per un nuovo oggetto
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: DACL per un nuovo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01d1ec8e92d4d56f977d4454b9a67df0a9bd489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130250"
---
# <a name="dacl-for-a-new-object"></a><span data-ttu-id="560cb-103">DACL per un nuovo oggetto</span><span class="sxs-lookup"><span data-stu-id="560cb-103">DACL for a New Object</span></span>

<span data-ttu-id="560cb-104">Il sistema utilizza l'algoritmo seguente per compilare un DACL per la maggior parte dei tipi di nuovi oggetti a protezione diretta:</span><span class="sxs-lookup"><span data-stu-id="560cb-104">The system uses the following algorithm to build a DACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="560cb-105">Il DACL dell'oggetto è l'elenco DACL del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) specificato dal creatore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="560cb-105">The object's DACL is the DACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="560cb-106">Il sistema unisce eventuali ACE ereditabili nell'elenco DACL specificato, a meno che non \_ \_ sia impostato il bit protetto con DACL se nei bit del controllo del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="560cb-106">The system merges any inheritable ACEs into the specified DACL unless the SE\_DACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span>
2.  <span data-ttu-id="560cb-107">Se il creatore non specifica un descrittore di sicurezza, il sistema compila l'elenco DACL dell'oggetto da voci ACE ereditabili.</span><span class="sxs-lookup"><span data-stu-id="560cb-107">If the creator does not specify a security descriptor, the system builds the object's DACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="560cb-108">Se non è specificato alcun descrittore di sicurezza e non sono presenti ACE ereditabili, il DACL dell'oggetto è l'elenco DACL predefinito del token [*primario*](/windows/desktop/SecGloss/p-gly) o di [*rappresentazione*](/windows/desktop/SecGloss/i-gly) del creatore.</span><span class="sxs-lookup"><span data-stu-id="560cb-108">If no security descriptor is specified and there are no inheritable ACEs, the object's DACL is the default DACL from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creator.</span></span>
4.  <span data-ttu-id="560cb-109">Se non è presente alcun DACL specificato, ereditato o predefinito, il sistema crea l'oggetto senza DACL, che consente a tutti gli utenti di accedere completamente all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="560cb-109">If there is no specified, inherited, or default DACL, the system creates the object with no DACL, which allows everyone full access to the object.</span></span>

<span data-ttu-id="560cb-110">Il sistema utilizza un algoritmo diverso per compilare un DACL per un nuovo oggetto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="560cb-110">The system uses a different algorithm to build a DACL for a new Active Directory object.</span></span> <span data-ttu-id="560cb-111">Per ulteriori informazioni, vedere [la pagina relativa alla modalità di impostazione dei descrittori di sicurezza per i nuovi oggetti directory](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="560cb-111">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
