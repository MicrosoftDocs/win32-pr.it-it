---
description: Viene illustrato il linguaggio SDDL (Security Descriptor Definition Language).
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: Linguaggio di definizione del descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9de9d3535efe5c33ac633a9dbd295405d74b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879657"
---
# <a name="security-descriptor-definition-language"></a><span data-ttu-id="c6233-103">Linguaggio di definizione del descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="c6233-103">Security Descriptor Definition Language</span></span>

<span data-ttu-id="c6233-104">Il linguaggio SDDL (Security Descriptor Definition Language) definisce il formato stringa usato dalle funzioni [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) per descrivere un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) come stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="c6233-104">The security descriptor definition language (SDDL) defines the string format that the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use to describe a [*security descriptor*](/windows/desktop/SecGloss/s-gly) as a text string.</span></span> <span data-ttu-id="c6233-105">Il linguaggio definisce inoltre gli elementi stringa per la descrizione delle informazioni nei componenti di un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c6233-105">The language also defines string elements for describing information in the components of a security descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="c6233-106">Le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) condizionale (ACE) hanno un formato SDDL diverso rispetto ad altri tipi ACE.</span><span class="sxs-lookup"><span data-stu-id="c6233-106">Conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) have a different SDDL format than other ACE types.</span></span> <span data-ttu-id="c6233-107">Per le voci ACE, vedere [stringhe ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="c6233-107">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="c6233-108">Per le voci ACE condizionali, vedere [Security Descriptor Definition Language per le ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="c6233-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c6233-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6233-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6233-110">Formato stringa descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="c6233-110">Security Descriptor String Format</span></span>](security-descriptor-string-format.md)
</dt> <dt>

[<span data-ttu-id="c6233-111">Linguaggio di definizione del descrittore di sicurezza per le voci</span><span class="sxs-lookup"><span data-stu-id="c6233-111">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="c6233-112">Stringhe ACE</span><span class="sxs-lookup"><span data-stu-id="c6233-112">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="c6233-113">Stringhe SID</span><span class="sxs-lookup"><span data-stu-id="c6233-113">SID Strings</span></span>](sid-strings.md)
</dt> <dt>

<span data-ttu-id="c6233-114">[\[MS-DTYP \] : Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="c6233-114">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

 

 
