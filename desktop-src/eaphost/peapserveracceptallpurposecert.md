---
title: PeapServerAcceptAllPurposeCert
description: La chiave del registro di sistema PeapServerAcceptAllPurposeCert determina se per l'autenticazione PEAP sono accettati certificati tutti gli scopi.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299313"
---
# <a name="peapserveracceptallpurposecert"></a><span data-ttu-id="511a7-103">PeapServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="511a7-103">PeapServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="511a7-104">La chiave del registro di sistema PeapServerAcceptAllPurposeCert determina se per l'autenticazione PEAP sono accettati certificati tutti gli scopi.</span><span class="sxs-lookup"><span data-stu-id="511a7-104">The PeapServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="511a7-105">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="511a7-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="511a7-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="511a7-106">Remarks</span></span>

<span data-ttu-id="511a7-107">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="511a7-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="511a7-108">Valore</span><span class="sxs-lookup"><span data-stu-id="511a7-108">Value</span></span>        | <span data-ttu-id="511a7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="511a7-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="511a7-110">1</span><span class="sxs-lookup"><span data-stu-id="511a7-110">1</span></span>            | <span data-ttu-id="511a7-111">Server e client accettano i certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="511a7-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="511a7-112">Altri valori</span><span class="sxs-lookup"><span data-stu-id="511a7-112">Other values</span></span> | <span data-ttu-id="511a7-113">Server e client non accettano certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="511a7-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="511a7-114">Se il valore del registro di sistema non è presente, il server e il client accettano i certificati tutti gli scopi inviati dall'altra parte per l'autenticazione PEAP.</span><span class="sxs-lookup"><span data-stu-id="511a7-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="511a7-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="511a7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="511a7-116">Impostazioni del registro di sistema EAPHost</span><span class="sxs-lookup"><span data-stu-id="511a7-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




