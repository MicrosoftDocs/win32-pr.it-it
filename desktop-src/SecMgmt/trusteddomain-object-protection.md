---
description: Quando viene creato un oggetto TrustedDomain, viene assegnata una protezione standard.
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: Protezione dell'oggetto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd27a01c1bcfde12fd062f2e8ae7c92a979991a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306413"
---
# <a name="trusteddomain-object-protection"></a><span data-ttu-id="a592d-103">Protezione dell'oggetto TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="a592d-103">TrustedDomain Object Protection</span></span>

<span data-ttu-id="a592d-104">Quando viene creato un oggetto [**trustedDomain**](trusteddomain-object.md) , viene assegnata una protezione standard come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a592d-104">When a [**TrustedDomain**](trusteddomain-object.md) object is created, it is assigned a standard protection as follows:</span></span>

-   <span data-ttu-id="a592d-105">Al gruppo locale internazionale viene concesso \_ l'accesso Execute generico.</span><span class="sxs-lookup"><span data-stu-id="a592d-105">The WORLD local group is granted GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="a592d-106">Al \_ gruppo locale di amministrazione locale vengono concesse le autorizzazioni Elimina, lettura generica \_ , scrittura generica \_ ed esecuzione generica \_ .</span><span class="sxs-lookup"><span data-stu-id="a592d-106">The LOCAL\_ADMIN local group is granted DELETE, GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="a592d-107">Il \_ gruppo locale di amministrazione locale viene assegnato come proprietario e gruppo primario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a592d-107">The LOCAL\_ADMIN local group is assigned as owner and primary group of the object.</span></span>

 

 



