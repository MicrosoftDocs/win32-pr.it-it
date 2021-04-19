---
description: Le chiavi di sessione sono chiavi generate per essere utilizzate in una singola sessione di comunicazione.
ms.assetid: 18bf2023-084d-400d-b60d-1ba51ce6a2bc
title: Chiavi di sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4089f9ab5a0ae6889463c1b24c2eecb376c7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317696"
---
# <a name="session-keys"></a><span data-ttu-id="a33cc-103">Chiavi di sessione</span><span class="sxs-lookup"><span data-stu-id="a33cc-103">Session Keys</span></span>

<span data-ttu-id="a33cc-104">Le [*chiavi di sessione*](../secgloss/s-gly.md) sono chiavi generate per essere utilizzate in una singola sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="a33cc-104">[*Session keys*](../secgloss/s-gly.md) are keys that are generated to be used in a single communication session.</span></span> <span data-ttu-id="a33cc-105">Le chiavi di sessione vengono modificate di frequente e vengono scartate quando non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="a33cc-105">Session keys are frequently changed and are discarded when they are no longer needed.</span></span> <span data-ttu-id="a33cc-106">Ad esempio, TLS usa una chiave di sessione separata per ogni connessione e S/MIME usa una chiave di sessione separata per ogni messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="a33cc-106">For example, TLS uses a separate session key for each connection and S/MIME uses a separate session key for each email message.</span></span> <span data-ttu-id="a33cc-107">Viene in genere usata una [*chiave simmetrica*](../secgloss/s-gly.md) come chiave della sessione.</span><span class="sxs-lookup"><span data-stu-id="a33cc-107">Typically a [*symmetric key*](../secgloss/s-gly.md) is used as the session key.</span></span>

<span data-ttu-id="a33cc-108">Le chiavi della sessione sono volatili.</span><span class="sxs-lookup"><span data-stu-id="a33cc-108">Session keys are volatile.</span></span> <span data-ttu-id="a33cc-109">Le applicazioni possono salvare queste chiavi per un uso successivo o per la trasmissione ad altri utenti.</span><span class="sxs-lookup"><span data-stu-id="a33cc-109">Applications can save these keys for later use or for transmission to other users.</span></span> <span data-ttu-id="a33cc-110">Per altre informazioni, vedere [archiviazione delle chiavi crittografiche ed Exchange](cryptographic-key-storage-and-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a33cc-110">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md).</span></span>

 

 
