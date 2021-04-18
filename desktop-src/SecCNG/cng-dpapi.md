---
description: Microsoft ha introdotto Data Protection Application Programming Interface (DPAPI) in Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: DPAPI CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305851"
---
# <a name="cng-dpapi"></a><span data-ttu-id="b0007-103">DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="b0007-103">CNG DPAPI</span></span>

<span data-ttu-id="b0007-104">Microsoft ha introdotto Data Protection Application Programming Interface (DPAPI) in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b0007-104">Microsoft introduced the data protection application programming interface (DPAPI) in Windows 2000.</span></span> <span data-ttu-id="b0007-105">L'API è costituita da due funzioni, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="b0007-105">The API consists of two functions, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span> <span data-ttu-id="b0007-106">DPAPI è parte di CryptoAPI ed è destinato agli sviluppatori che conoscevano molto poco l'uso della crittografia.</span><span class="sxs-lookup"><span data-stu-id="b0007-106">DPAPI is part of CryptoAPI and was intended for developers who knew very little about using cryptography.</span></span> <span data-ttu-id="b0007-107">Le due funzioni possono essere utilizzate per crittografare e decrittografare i dati statici in un singolo computer.</span><span class="sxs-lookup"><span data-stu-id="b0007-107">The two functions could be used to encrypt and decrypt static data on a single computer.</span></span>

<span data-ttu-id="b0007-108">Il cloud computing, tuttavia, richiede spesso che il contenuto crittografato in un computer venga decrittografato in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="b0007-108">Cloud computing, however, often requires that content encrypted on one computer be decrypted on another.</span></span> <span data-ttu-id="b0007-109">Pertanto, a partire da Windows 8, Microsoft ha esteso l'idea di usare un'API relativamente semplice per includere scenari cloud.</span><span class="sxs-lookup"><span data-stu-id="b0007-109">Therefore, beginning with Windows 8, Microsoft extended the idea of using a relatively straightforward API to encompass cloud scenarios.</span></span> <span data-ttu-id="b0007-110">Questa nuova API, denominata DPAPI-NG, consente di condividere in modo sicuro i segreti (chiavi, password, materiale della chiave) e i messaggi protetti in un set di entità che possono essere usate per rimuovere la protezione in computer diversi dopo l'autenticazione e l'autorizzazione corrette.</span><span class="sxs-lookup"><span data-stu-id="b0007-110">This new API, called DPAPI-NG, enables you to securely share secrets (keys, passwords, key material) and messages by protecting them to a set of principals that can be used to unprotect them on different computers after proper authentication and authorization.</span></span> <span data-ttu-id="b0007-111">Attualmente sono supportate le entità seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0007-111">The following principals are currently supported:</span></span>

-   <span data-ttu-id="b0007-112">Gruppo in una foresta Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b0007-112">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="b0007-113">Credenziali Web.</span><span class="sxs-lookup"><span data-stu-id="b0007-113">Web credentials.</span></span>

<span data-ttu-id="b0007-114">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="b0007-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b0007-115">Provider di protezione</span><span class="sxs-lookup"><span data-stu-id="b0007-115">Protection Providers</span></span>](protection-providers.md)
-   [<span data-ttu-id="b0007-116">Descrittori di protezione</span><span class="sxs-lookup"><span data-stu-id="b0007-116">Protection Descriptors</span></span>](protection-descriptors.md)
-   [<span data-ttu-id="b0007-117">Formato dati protetto</span><span class="sxs-lookup"><span data-stu-id="b0007-117">Protected Data Format</span></span>](protected-data-format.md)

<span data-ttu-id="b0007-118">DPAPI-NG si basa su Cryptography Next Generation (CNG) e include le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0007-118">DPAPI-NG is built on top of Cryptography Next Generation (CNG) and includes the following functions:</span></span>

-   [<span data-ttu-id="b0007-119">**NCryptCreateProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b0007-119">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [<span data-ttu-id="b0007-120">**NCryptCloseProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b0007-120">**NCryptCloseProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [<span data-ttu-id="b0007-121">**NCryptProtectSecret**</span><span class="sxs-lookup"><span data-stu-id="b0007-121">**NCryptProtectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [<span data-ttu-id="b0007-122">**NCryptQueryProtectionDescriptorName**</span><span class="sxs-lookup"><span data-stu-id="b0007-122">**NCryptQueryProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [<span data-ttu-id="b0007-123">**NCryptRegisterProtectionDescriptorName**</span><span class="sxs-lookup"><span data-stu-id="b0007-123">**NCryptRegisterProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [<span data-ttu-id="b0007-124">**NCryptStreamClose**</span><span class="sxs-lookup"><span data-stu-id="b0007-124">**NCryptStreamClose**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [<span data-ttu-id="b0007-125">**NCryptStreamOpenToProtect**</span><span class="sxs-lookup"><span data-stu-id="b0007-125">**NCryptStreamOpenToProtect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [<span data-ttu-id="b0007-126">**NCryptStreamOpenToUnprotect**</span><span class="sxs-lookup"><span data-stu-id="b0007-126">**NCryptStreamOpenToUnprotect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [<span data-ttu-id="b0007-127">**NCryptStreamUpdate**</span><span class="sxs-lookup"><span data-stu-id="b0007-127">**NCryptStreamUpdate**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [<span data-ttu-id="b0007-128">**NCryptUnprotectSecret**</span><span class="sxs-lookup"><span data-stu-id="b0007-128">**NCryptUnprotectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
