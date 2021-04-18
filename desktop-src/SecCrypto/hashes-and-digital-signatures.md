---
description: Con le funzioni hash e firma digitale, un utente può firmare digitalmente i dati in modo che qualsiasi altro utente possa verificare che i dati non siano stati modificati dopo la firma. È anche possibile verificare l'identità dell'utente che ha firmato i dati.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hash e firme digitali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc2894cbf53834551afef375fb5056df89675a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316164"
---
# <a name="hashes-and-digital-signatures"></a><span data-ttu-id="20c17-104">Hash e firme digitali</span><span class="sxs-lookup"><span data-stu-id="20c17-104">Hashes and Digital Signatures</span></span>

<span data-ttu-id="20c17-105">Con le [funzioni hash e firma digitale](cryptography-functions.md), un utente può firmare digitalmente i dati in modo che qualsiasi altro utente possa verificare che i dati non siano stati modificati dopo la firma.</span><span class="sxs-lookup"><span data-stu-id="20c17-105">With [Hash and Digital Signature Functions](cryptography-functions.md), a user can digitally sign data so that any other user can verify that the data has not been changed since it was signed.</span></span> <span data-ttu-id="20c17-106">È anche possibile verificare l'identità dell'utente che ha firmato i dati.</span><span class="sxs-lookup"><span data-stu-id="20c17-106">The identity of the user who signed the data can also be verified.</span></span>

<span data-ttu-id="20c17-107">Una [*firma digitale*](../secgloss/d-gly.md) è costituita da una piccola quantità di dati binari, in genere inferiore a 256 byte.</span><span class="sxs-lookup"><span data-stu-id="20c17-107">A [*digital signature*](../secgloss/d-gly.md) consists of a small amount of binary data, typically less than 256 bytes.</span></span> <span data-ttu-id="20c17-108">Questa firma può essere inclusa nel messaggio firmato o archiviata separatamente, a seconda della modalità di implementazione di una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="20c17-108">This signature can be bundled with the signed message or stored separately, depending on how a particular application has been implemented.</span></span>

<span data-ttu-id="20c17-109">Microsoft Strong Cryptographic Provider crea firme digitali conformi a RSA [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1.</span><span class="sxs-lookup"><span data-stu-id="20c17-109">The Microsoft Strong Cryptographic Provider creates digital signatures that conform to the RSA [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1.</span></span>

 

 
