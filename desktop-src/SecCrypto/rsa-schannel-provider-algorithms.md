---
description: Gli algoritmi potrebbero essere supportati dal provider di crittografia Microsoft RSA/SChannel.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: Algoritmi del provider RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307667"
---
# <a name="rsaschannel-provider-algorithms"></a><span data-ttu-id="25b75-103">Algoritmi del provider RSA/SChannel</span><span class="sxs-lookup"><span data-stu-id="25b75-103">RSA/Schannel Provider Algorithms</span></span>

<span data-ttu-id="25b75-104">Gli algoritmi seguenti potrebbero essere supportati da Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) Cryptographic Provider.</span><span class="sxs-lookup"><span data-stu-id="25b75-104">The following algorithms might be supported by the Microsoft [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider.</span></span>



| <span data-ttu-id="25b75-105">ID algoritmo</span><span class="sxs-lookup"><span data-stu-id="25b75-105">Algorithm ID</span></span>    | <span data-ttu-id="25b75-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25b75-106">Description</span></span>                                                                                                                         | <span data-ttu-id="25b75-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="25b75-107">Comments</span></span>                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25b75-108">CALG \_ RSA \_ KEYX</span><span class="sxs-lookup"><span data-stu-id="25b75-108">CALG\_RSA\_KEYX</span></span> | <span data-ttu-id="25b75-109">[ *Algoritmo di scambio delle chiavi* chiave pubblica RSA](../secgloss/k-gly.md)</span><span class="sxs-lookup"><span data-stu-id="25b75-109">RSA public key [*key exchange algorithm*](../secgloss/k-gly.md)</span></span> | <span data-ttu-id="25b75-110">Lunghezza della chiave: è possibile impostare 384 bit su 16.384 bit in incrementi di 8 bit.</span><span class="sxs-lookup"><span data-stu-id="25b75-110">Key length: Can be set, 384 bits to 16,384 bits in 8 bit increments.</span></span> <span data-ttu-id="25b75-111">Lunghezza chiave predefinita: 1.024 bit.</span><span class="sxs-lookup"><span data-stu-id="25b75-111">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="25b75-112">\_MD5 CALG</span><span class="sxs-lookup"><span data-stu-id="25b75-112">CALG\_MD5</span></span>       | <span data-ttu-id="25b75-113">Algoritmo di hash MD5.</span><span class="sxs-lookup"><span data-stu-id="25b75-113">MD5 hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="25b75-114">Fornito solo per l'hashing.</span><span class="sxs-lookup"><span data-stu-id="25b75-114">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="25b75-115">\_Sha CALG</span><span class="sxs-lookup"><span data-stu-id="25b75-115">CALG\_SHA</span></span>       | <span data-ttu-id="25b75-116">Algoritmo di hash SHA.</span><span class="sxs-lookup"><span data-stu-id="25b75-116">SHA hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="25b75-117">Deve essere usato per le firme DSS.</span><span class="sxs-lookup"><span data-stu-id="25b75-117">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="25b75-118">CALG \_ RC2</span><span class="sxs-lookup"><span data-stu-id="25b75-118">CALG\_RC2</span></span>       | <span data-ttu-id="25b75-119">Algoritmo di crittografia a blocchi RC2.</span><span class="sxs-lookup"><span data-stu-id="25b75-119">RC2 block encryption algorithm.</span></span>                                                                                                     | <span data-ttu-id="25b75-120">Lunghezza della chiave: da 40 a 88 bit</span><span class="sxs-lookup"><span data-stu-id="25b75-120">Key length: 40 to 88 bits</span></span>                                                                                       |
| <span data-ttu-id="25b75-121">CALG \_ RC4</span><span class="sxs-lookup"><span data-stu-id="25b75-121">CALG\_RC4</span></span>       | <span data-ttu-id="25b75-122">Algoritmo di crittografia del flusso RC4.</span><span class="sxs-lookup"><span data-stu-id="25b75-122">RC4 stream encryption algorithm.</span></span>                                                                                                    | <span data-ttu-id="25b75-123">Lunghezza della chiave: da 40 a 88 bit</span><span class="sxs-lookup"><span data-stu-id="25b75-123">Key length: 40 to 88 bits</span></span>                                                                                       |



 

 

 
