---
title: PeapServerUseAllPurposeCert
description: La chiave del registro di sistema PeapServerUseAllPurposeCert determina se vengono utilizzati certificati tutti gli scopi per l'autenticazione PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104335740"
---
# <a name="peapserveruseallpurposecert"></a><span data-ttu-id="d422b-103">PeapServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="d422b-103">PeapServerUseAllPurposeCert</span></span>

<span data-ttu-id="d422b-104">La chiave del registro di sistema PeapServerUseAllPurposeCert determina se vengono utilizzati certificati tutti gli scopi per l'autenticazione PEAP.</span><span class="sxs-lookup"><span data-stu-id="d422b-104">The PeapServerUseAllPurposeCert registry key determines if all-purpose certificates are used for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d422b-105">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="d422b-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="d422b-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="d422b-106">Remarks</span></span>

<span data-ttu-id="d422b-107">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d422b-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="d422b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d422b-108">Value</span></span>        | <span data-ttu-id="d422b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d422b-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d422b-110">1</span><span class="sxs-lookup"><span data-stu-id="d422b-110">1</span></span>            | <span data-ttu-id="d422b-111">Per l'autenticazione PEAP sono selezionati i certificati per tutti gli scopi nell'archivio certificati del client o del server.</span><span class="sxs-lookup"><span data-stu-id="d422b-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="d422b-112">Altri valori</span><span class="sxs-lookup"><span data-stu-id="d422b-112">Other values</span></span> | <span data-ttu-id="d422b-113">I certificati per tutti gli scopi nell'archivio certificati del client o del server non sono selezionati per l'autenticazione PEAP.</span><span class="sxs-lookup"><span data-stu-id="d422b-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="d422b-114">Se il valore del registro di sistema non è presente, per l'autenticazione PEAP vengono selezionati i certificati per tutti gli scopi nell'archivio certificati del client o del server.</span><span class="sxs-lookup"><span data-stu-id="d422b-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d422b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d422b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d422b-116">Impostazioni del registro di sistema EAPHost</span><span class="sxs-lookup"><span data-stu-id="d422b-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




