---
description: La funzione QueryContextAttributes (digest) fornisce informazioni sulle impostazioni correnti di un contesto di sicurezza.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Esecuzione di query sugli attributi del contesto di sicurezza digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967396"
---
# <a name="querying-digest-security-context-attributes"></a><span data-ttu-id="e85b4-103">Esecuzione di query sugli attributi del contesto di sicurezza digest</span><span class="sxs-lookup"><span data-stu-id="e85b4-103">Querying Digest Security Context Attributes</span></span>

<span data-ttu-id="e85b4-104">La funzione [**QueryContextAttributes (digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) fornisce informazioni sulle impostazioni correnti di un [*contesto di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e85b4-104">The [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) function provides information about the current settings of a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="e85b4-105">Microsoft Digest supporta l'esecuzione di query sui seguenti attributi del contesto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e85b4-105">Microsoft Digest supports querying the following security context attributes.</span></span>



| <span data-ttu-id="e85b4-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="e85b4-106">Attribute</span></span>                   | <span data-ttu-id="e85b4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e85b4-107">Description</span></span>                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e85b4-108">\_informazioni sulla \_ chiave SECPKG attr \_</span><span class="sxs-lookup"><span data-stu-id="e85b4-108">SECPKG\_ATTR\_KEY\_INFO</span></span>     | <span data-ttu-id="e85b4-109">Informazioni relative agli algoritmi di firma e crittografia in uso.</span><span class="sxs-lookup"><span data-stu-id="e85b4-109">Information relating to the signing and encryption algorithms in use.</span></span>                                                                                                                                   |
| <span data-ttu-id="e85b4-110">\_informazioni sul \_ pacchetto SECPKG attr \_</span><span class="sxs-lookup"><span data-stu-id="e85b4-110">SECPKG\_ATTR\_PACKAGE\_INFO</span></span> | <span data-ttu-id="e85b4-111">Informazioni generali relative all'Microsoft Digest, ad esempio le dimensioni massime del token consentite dal [*pacchetto di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e85b4-111">General information pertaining to Microsoft Digest, such as the maximum token size permitted by the [*security package*](../secgloss/s-gly.md).</span></span> |
| <span data-ttu-id="e85b4-112">\_dimensioni attr \_ SECPKG</span><span class="sxs-lookup"><span data-stu-id="e85b4-112">SECPKG\_ATTR\_SIZES</span></span>         | <span data-ttu-id="e85b4-113">Dimensioni massime consentite per i dati correlati al messaggio, ad esempio le firme.</span><span class="sxs-lookup"><span data-stu-id="e85b4-113">The maximum sizes permitted for message-related data such as signatures.</span></span>                                                                                                                                |



 

 

 
