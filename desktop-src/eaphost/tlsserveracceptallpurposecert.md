---
title: TlsServerAcceptAllPurposeCert
description: La chiave del registro di sistema TlsServerAcceptAllPurposeCert determina se i certificati per l'autenticazione EAP-TLS sono accettati per tutti gli scopi.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299297"
---
# <a name="tlsserveracceptallpurposecert"></a><span data-ttu-id="f39fc-103">TlsServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="f39fc-103">TlsServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="f39fc-104">La chiave del registro di sistema TlsServerAcceptAllPurposeCert determina se i certificati per l'autenticazione EAP-TLS sono accettati per tutti gli scopi.</span><span class="sxs-lookup"><span data-stu-id="f39fc-104">The TlsServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f39fc-105">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f39fc-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="f39fc-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="f39fc-106">Remarks</span></span>

<span data-ttu-id="f39fc-107">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f39fc-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="f39fc-108">Valore</span><span class="sxs-lookup"><span data-stu-id="f39fc-108">Value</span></span>        | <span data-ttu-id="f39fc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f39fc-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f39fc-110">1</span><span class="sxs-lookup"><span data-stu-id="f39fc-110">1</span></span>            | <span data-ttu-id="f39fc-111">Server e client accettano i certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="f39fc-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="f39fc-112">Altri valori</span><span class="sxs-lookup"><span data-stu-id="f39fc-112">Other values</span></span> | <span data-ttu-id="f39fc-113">Server e client non accettano certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="f39fc-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="f39fc-114">Se il valore del registro di sistema non è presente, il server e il client accettano i certificati tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="f39fc-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f39fc-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f39fc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f39fc-116">Impostazioni del registro di sistema EAPHost</span><span class="sxs-lookup"><span data-stu-id="f39fc-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




