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
# <a name="security-descriptor-definition-language"></a>Linguaggio di definizione del descrittore di sicurezza

Il linguaggio SDDL (Security Descriptor Definition Language) definisce il formato stringa usato dalle funzioni [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) per descrivere un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) come stringa di testo. Il linguaggio definisce inoltre gli elementi stringa per la descrizione delle informazioni nei componenti di un descrittore di sicurezza.

> [!Note]  
> Le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) condizionale (ACE) hanno un formato SDDL diverso rispetto ad altri tipi ACE. Per le voci ACE, vedere [stringhe ACE](ace-strings.md). Per le voci ACE condizionali, vedere [Security Descriptor Definition Language per le ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato stringa descrittore di sicurezza](security-descriptor-string-format.md)
</dt> <dt>

[Linguaggio di definizione del descrittore di sicurezza per le voci](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[Stringhe ACE](ace-strings.md)
</dt> <dt>

[Stringhe SID](sid-strings.md)
</dt> <dt>

[\[MS-DTYP \] : Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

 

 
