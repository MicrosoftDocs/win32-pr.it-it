---
description: Un descrittore di sicurezza funzionale valido contiene informazioni sulla sicurezza in formato binario.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Stringhe del descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb875bee4d35267b578193ca7cd08420722400a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129902"
---
# <a name="security-descriptor-strings"></a><span data-ttu-id="076e3-103">Stringhe del descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="076e3-103">Security Descriptor Strings</span></span>

<span data-ttu-id="076e3-104">Un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) funzionale valido contiene informazioni sulla sicurezza in formato binario.</span><span class="sxs-lookup"><span data-stu-id="076e3-104">A valid functional [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains security information in binary format.</span></span> <span data-ttu-id="076e3-105">L'API Windows fornisce funzioni per la conversione di descrittori di sicurezza binari da e verso stringhe di testo.</span><span class="sxs-lookup"><span data-stu-id="076e3-105">The Windows API provides functions for converting binary security descriptors to and from text strings.</span></span> <span data-ttu-id="076e3-106">I descrittori di sicurezza in formato stringa non sono funzionali, ma possono essere utili per archiviare o trasferire informazioni sul descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="076e3-106">Security descriptors in string format are not functional, but they can be useful for storing or transporting security descriptor information.</span></span>

<span data-ttu-id="076e3-107">Per convertire un descrittore di sicurezza in un formato stringa, chiamare la funzione [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) .</span><span class="sxs-lookup"><span data-stu-id="076e3-107">To convert a security descriptor to a string format, call the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) function.</span></span> <span data-ttu-id="076e3-108">Per convertire di nuovo un descrittore di sicurezza in formato stringa in un descrittore di sicurezza funzionale valido, chiamare la funzione [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) .</span><span class="sxs-lookup"><span data-stu-id="076e3-108">To convert a string-format security descriptor back to a valid functional security descriptor, call the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function.</span></span>

<span data-ttu-id="076e3-109">Per ulteriori informazioni, vedere [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="076e3-109">For more information, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

 

 
