---
description: I tipi di dati seguenti vengono utilizzati da funzioni di crittografia, interfacce e oggetti.
ms.assetid: 9d6a065d-c765-4d17-9f4c-38a984439278
title: Tipi di dati di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84c6f21faa25e1ccc478c178a3f21458ff589ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306451"
---
# <a name="cryptography-data-types"></a><span data-ttu-id="fab14-103">Tipi di dati di crittografia</span><span class="sxs-lookup"><span data-stu-id="fab14-103">Cryptography Data Types</span></span>

<span data-ttu-id="fab14-104">I tipi di dati seguenti vengono utilizzati da funzioni di crittografia, interfacce e oggetti.</span><span class="sxs-lookup"><span data-stu-id="fab14-104">The following data types are used by cryptography functions, interfaces, and objects.</span></span>



| <span data-ttu-id="fab14-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fab14-105">Data type</span></span>                                                                      | <span data-ttu-id="fab14-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fab14-106">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fab14-107">**\_ID ALG**</span><span class="sxs-lookup"><span data-stu-id="fab14-107">**ALG\_ID**</span></span>](alg-id.md)                                                      | <span data-ttu-id="fab14-108">Specifica gli identificatori dell'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="fab14-108">Specifies algorithm identifiers.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="fab14-109">**\_ \_ risposta OCSP del server HCERT \_**</span><span class="sxs-lookup"><span data-stu-id="fab14-109">**HCERT\_SERVER\_OCSP\_RESPONSE**</span></span>](hcert-server-ocsp-response.md)            | <span data-ttu-id="fab14-110">Rappresenta un handle per una risposta OCSP associata a una catena di certificati del server.</span><span class="sxs-lookup"><span data-stu-id="fab14-110">Represents a handle to an OCSP response associated with a server certificate chain.</span></span>                                                                                                              |
| [<span data-ttu-id="fab14-111">**HCRYPTHASH**</span><span class="sxs-lookup"><span data-stu-id="fab14-111">**HCRYPTHASH**</span></span>](hcrypthash.md)                                               | <span data-ttu-id="fab14-112">Specifica gli handle per un [*oggetto hash*](../secgloss/h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fab14-112">Specifies handles to a [*hash object*](../secgloss/h-gly.md).</span></span>                                                                                      |
| [<span data-ttu-id="fab14-113">**HCRYPTKEY**</span><span class="sxs-lookup"><span data-stu-id="fab14-113">**HCRYPTKEY**</span></span>](hcryptkey.md)                                                 | <span data-ttu-id="fab14-114">Specifica gli handle per le chiavi crittografiche.</span><span class="sxs-lookup"><span data-stu-id="fab14-114">Specifies handles to cryptographic keys.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="fab14-115">**HCRYPTOIDFUNCADDR**</span><span class="sxs-lookup"><span data-stu-id="fab14-115">**HCRYPTOIDFUNCADDR**</span></span>](hcryptoidfuncaddr.md)                                 | <span data-ttu-id="fab14-116">Rappresenta un handle per una funzione che può essere installata utilizzando un [*identificatore di oggetto*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="fab14-116">Represents a handle to a function that can be installed by using an [*object identifier*](../secgloss/o-gly.md) (OID).</span></span>                 |
| [<span data-ttu-id="fab14-117">**HCRYPTOIDFUNCSET**</span><span class="sxs-lookup"><span data-stu-id="fab14-117">**HCRYPTOIDFUNCSET**</span></span>](hcryptoidfuncset.md)                                   | <span data-ttu-id="fab14-118">Rappresenta un handle per un set di funzioni che possono essere installate utilizzando un OID.</span><span class="sxs-lookup"><span data-stu-id="fab14-118">Represents a handle to a set of functions that can be installed by using an OID.</span></span>                                                                                                                 |
| [<span data-ttu-id="fab14-119">**\_legacy HCRYPTPROV**</span><span class="sxs-lookup"><span data-stu-id="fab14-119">**HCRYPTPROV\_LEGACY**</span></span>](hcryptprov-legacy.md)                                | <span data-ttu-id="fab14-120">Utilizzato per sostituire il tipo di dati [**HCRYPTPROV**](hcryptprov.md) in cui il tipo di dati **HCRYPTPROV** non viene più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="fab14-120">Used to replace the [**HCRYPTPROV**](hcryptprov.md) data type where the **HCRYPTPROV** data type is no longer used.</span></span>                                                                             |
| [<span data-ttu-id="fab14-121">**\_handle di chiave HCRYPTPROV o \_ NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fab14-121">**HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE**</span></span>](hcryptprov-or-ncrypt-key-handle.md) | <span data-ttu-id="fab14-122">Specifica un handle per un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) CryptoAPI o un CSP CNG.</span><span class="sxs-lookup"><span data-stu-id="fab14-122">Specifies a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> |
| [<span data-ttu-id="fab14-123">**HCRYPTPROV**</span><span class="sxs-lookup"><span data-stu-id="fab14-123">**HCRYPTPROV**</span></span>](hcryptprov.md)                                               | <span data-ttu-id="fab14-124">Specifica un handle per un CSP CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="fab14-124">Specifies a handle to a CryptoAPI CSP.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="fab14-125">**\_handle KEYSVCC**</span><span class="sxs-lookup"><span data-stu-id="fab14-125">**KEYSVCC\_HANDLE**</span></span>](keysvcc-handle.md)                                      | <span data-ttu-id="fab14-126">Specifica gli handle per il servizio chiavi.</span><span class="sxs-lookup"><span data-stu-id="fab14-126">Specifies handles to the key service.</span></span>                                                                                                                                                            |



 

 

 
