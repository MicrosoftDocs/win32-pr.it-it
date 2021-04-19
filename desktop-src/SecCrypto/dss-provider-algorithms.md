---
description: La tabella seguente elenca gli algoritmi supportati dal provider di crittografia Microsoft DSS.
ms.assetid: 2a7aecf8-e242-4087-83ee-aaa637a9ec71
title: Algoritmi del provider DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0bd9346da7a9ab1490e2646d9d2559c07359b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311924"
---
# <a name="dss-provider-algorithms"></a><span data-ttu-id="fa513-103">Algoritmi del provider DSS</span><span class="sxs-lookup"><span data-stu-id="fa513-103">DSS Provider Algorithms</span></span>

<span data-ttu-id="fa513-104">La tabella seguente elenca gli algoritmi supportati dal provider di crittografia Microsoft DSS.</span><span class="sxs-lookup"><span data-stu-id="fa513-104">The following table lists the algorithms supported by the Microsoft DSS Cryptographic Provider.</span></span>



| <span data-ttu-id="fa513-105">ID algoritmo</span><span class="sxs-lookup"><span data-stu-id="fa513-105">Algorithm ID</span></span>    | <span data-ttu-id="fa513-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa513-106">Description</span></span>                                 | <span data-ttu-id="fa513-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa513-107">Comments</span></span>                                                                                                        |
|-----------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa513-108">\_MD5 CALG</span><span class="sxs-lookup"><span data-stu-id="fa513-108">CALG\_MD5</span></span>       | <span data-ttu-id="fa513-109">Algoritmo di hash MD5.</span><span class="sxs-lookup"><span data-stu-id="fa513-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="fa513-110">Fornito solo per l'hashing.</span><span class="sxs-lookup"><span data-stu-id="fa513-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="fa513-111">\_Sha CALG</span><span class="sxs-lookup"><span data-stu-id="fa513-111">CALG\_SHA</span></span>       | <span data-ttu-id="fa513-112">Algoritmo di hash SHA.</span><span class="sxs-lookup"><span data-stu-id="fa513-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="fa513-113">Deve essere usato per le firme DSS.</span><span class="sxs-lookup"><span data-stu-id="fa513-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="fa513-114">CALG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="fa513-114">CALG\_SHA1</span></span>      | <span data-ttu-id="fa513-115">Uguale a CALG \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="fa513-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="fa513-116">Nessun commento.</span><span class="sxs-lookup"><span data-stu-id="fa513-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="fa513-117">\_firma CALG DSS \_</span><span class="sxs-lookup"><span data-stu-id="fa513-117">CALG\_DSS\_SIGN</span></span> | <span data-ttu-id="fa513-118">Algoritmo di firma della chiave pubblica/privata DSS.</span><span class="sxs-lookup"><span data-stu-id="fa513-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="fa513-119">Lunghezza della chiave: è possibile impostare 512 bit su 1.024 bit in incrementi di 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fa513-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="fa513-120">Lunghezza chiave predefinita: 1.024 bit.</span><span class="sxs-lookup"><span data-stu-id="fa513-120">Default key length: 1,024 bits.</span></span><br/> |



 

 

 




