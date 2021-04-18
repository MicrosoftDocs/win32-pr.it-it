---
description: Il motore di protocollo Schannel esegue l'handshake e l'autenticazione in un processo sicuro e la crittografia/messaggi in blocco al passaggio del processo dell'applicazione.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Superamento dei limiti del processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046bc6f53d609ec22ed37edd08d6967cc4ae73e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306464"
---
# <a name="crossing-process-boundaries"></a><span data-ttu-id="a599a-103">Superamento dei limiti del processo</span><span class="sxs-lookup"><span data-stu-id="a599a-103">Crossing Process Boundaries</span></span>

<span data-ttu-id="a599a-104">Il motore di protocollo [*Schannel*](../secgloss/s-gly.md) esegue l'handshake e l'autenticazione in un [*processo*](../secgloss/p-gly.md) sicuro e la crittografia/messaggi in blocco al passaggio del processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a599a-104">The [*Schannel*](../secgloss/s-gly.md) protocol engine performs the handshaking and authentication in a secure [*process*](../secgloss/p-gly.md) and the bulk encryption/message passing in the application process.</span></span> <span data-ttu-id="a599a-105">Ciò significa che le [*chiavi di crittografia bulk*](../secgloss/b-gly.md) e le chiavi [*Mac*](../secgloss/m-gly.md) devono essere copiate da un processo a un altro.</span><span class="sxs-lookup"><span data-stu-id="a599a-105">This means that the [*bulk encryption keys*](../secgloss/b-gly.md) and [*MAC*](../secgloss/m-gly.md) keys must be copied from one process to another.</span></span> <span data-ttu-id="a599a-106">Per copiare le chiavi da un processo a un altro, usare le funzioni [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) e [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a599a-106">To copy the keys from one process to another, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) functions as follows:</span></span>

1.  <span data-ttu-id="a599a-107">Il processo sicuro esporta ogni chiave in un [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) usando [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), quindi Elimina la chiave usando [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span><span class="sxs-lookup"><span data-stu-id="a599a-107">The secure process exports each key into an [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) using [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), then destroys the key using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span> <span data-ttu-id="a599a-108">Si noti che se la chiave viene archiviata in hardware, il CSP deve riconoscere questo e non deve tentare di eliminare definitivamente la chiave.</span><span class="sxs-lookup"><span data-stu-id="a599a-108">Note that if the key is stored in hardware, the CSP must recognize this and must not attempt to destroy the key.</span></span>
2.  <span data-ttu-id="a599a-109">Il processo protetto passa il OPAQUEKEYBLOBs al processo dell'applicazione in un modo che esula dall'ambito di questo documento.</span><span class="sxs-lookup"><span data-stu-id="a599a-109">The secure process passes the OPAQUEKEYBLOBs to the application process in a manner beyond the scope of this document.</span></span>
3.  <span data-ttu-id="a599a-110">Il processo dell'applicazione importa ogni OPAQUEKEYBLOB di backup nel CSP usando [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="a599a-110">The application process imports each OPAQUEKEYBLOB back into the CSP using [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="a599a-111">A questo punto, la chiave deve trovarsi esattamente nello stesso [*stato*](../secgloss/s-gly.md) in cui è stata esportata.</span><span class="sxs-lookup"><span data-stu-id="a599a-111">At this point, the key must be in exactly the same [*state*](../secgloss/s-gly.md) as when it was exported.</span></span>

 

 
