---
description: I BLOB opachi, noti anche come OPAQUEKEYBLOBs, vengono usati per archiviare le chiavi di sessione in un formato specifico del fornitore, ad esempio Schannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Tipo di BLOB opaco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401783"
---
# <a name="opaque-blob-type"></a><span data-ttu-id="d3dd9-103">Tipo di BLOB opaco</span><span class="sxs-lookup"><span data-stu-id="d3dd9-103">Opaque BLOB Type</span></span>

<span data-ttu-id="d3dd9-104">I [*BLOB opachi*](../secgloss/o-gly.md), noti anche come OPAQUEKEYBLOBs, vengono usati per archiviare le [*chiavi di sessione*](../secgloss/s-gly.md) in un formato specifico del fornitore, ad esempio [*Schannel*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d3dd9-104">[*Opaque BLOBs*](../secgloss/o-gly.md), also known as OPAQUEKEYBLOBs, are used to store [*session keys*](../secgloss/s-gly.md) in a vendor-specific format, such as [*Schannel*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="d3dd9-105">Contengono il materiale della chiave di base e tutte le informazioni [*sullo stato*](../secgloss/s-gly.md) corrente.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-105">They contain the base key material and all current [*state*](../secgloss/s-gly.md) information.</span></span> <span data-ttu-id="d3dd9-106">Sono incluse informazioni quali il [*valore salt*](../secgloss/s-gly.md), il [*vettore di inizializzazione*](../secgloss/i-gly.md)e la tabella delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-106">This includes information such as the [*salt value*](../secgloss/s-gly.md), the [*initialization vector*](../secgloss/i-gly.md), and the key table.</span></span> <span data-ttu-id="d3dd9-107">Il formato dei BLOB opachi non è pubblicato.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-107">The format of opaque BLOBs is unpublished.</span></span> <span data-ttu-id="d3dd9-108">Ogni fornitore CSP determina il proprio formato BLOB.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-108">Each CSP vendor determines its own BLOB format.</span></span>

<span data-ttu-id="d3dd9-109">Poiché una chiave viene esportata in un BLOB opaco nel formato specifico di CSP, può essere importata solo nel CSP da cui è stata originariamente esportata.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-109">Because a key is exported into an opaque BLOB in CSP-specific format, it can only be imported into the CSP from which it was originally exported.</span></span>

<span data-ttu-id="d3dd9-110">Quando sono interessati due processi, ogni [*processo*](../secgloss/p-gly.md) chiama [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-110">When two processes are involved, each [*process*](../secgloss/p-gly.md) calls [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) independently.</span></span> <span data-ttu-id="d3dd9-111">Ogni processo ottiene un handle per un contenitore di chiavi.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-111">Each process gets a handle to a key container.</span></span> <span data-ttu-id="d3dd9-112">È possibile che entrambi i processi dispongano di handle per lo stesso contenitore di chiavi.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-112">It is possible for both processes to have handles to the same key container.</span></span> <span data-ttu-id="d3dd9-113">Un processo crea le chiavi e le esporta in BLOB opachi, quindi passa i BLOB al secondo processo.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-113">One process creates the keys and exports them into opaque BLOBs, then passes the BLOBs to the second process.</span></span> <span data-ttu-id="d3dd9-114">Il secondo processo importa le chiavi dal BLOB nel relativo [*contenitore di chiavi*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d3dd9-114">The second process imports the keys from the BLOB into its [*key container*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="d3dd9-115">Se un CSP hardware non supporta l'esportazione di chiavi, il BLOB potrebbe contenere solo l'indice di un registro della chiave o qualcosa di simile.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-115">If a hardware CSP does not support exporting keys, the BLOB might only contain the index of a key register, or something similar.</span></span> <span data-ttu-id="d3dd9-116">In questo caso, il resto della procedura viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="d3dd9-116">In this case, the rest of the procedure is ignored.</span></span>

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
