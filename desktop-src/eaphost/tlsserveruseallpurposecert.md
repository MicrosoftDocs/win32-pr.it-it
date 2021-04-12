---
title: TlsServerUseAllPurposeCert
description: La chiave del registro di sistema TlsServerUseAllPurposeCert determina se vengono usati certificati tutti gli scopi per l'autenticazione EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104335711"
---
# <a name="tlsserveruseallpurposecert"></a><span data-ttu-id="0df62-103">TlsServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="0df62-103">TlsServerUseAllPurposeCert</span></span>

<span data-ttu-id="0df62-104">La chiave del registro di sistema TlsServerUseAllPurposeCert determina se vengono usati certificati tutti gli scopi per l'autenticazione EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="0df62-104">The TlsServerUseAllPurposeCert registry key determines if all-purpose certificates are used for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0df62-105">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0df62-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="0df62-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="0df62-106">Remarks</span></span>

<span data-ttu-id="0df62-107">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0df62-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="0df62-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0df62-108">Value</span></span>        | <span data-ttu-id="0df62-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0df62-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0df62-110">1</span><span class="sxs-lookup"><span data-stu-id="0df62-110">1</span></span>            | <span data-ttu-id="0df62-111">Per l'autenticazione PEAP sono selezionati i certificati per tutti gli scopi nell'archivio certificati del client o del server.</span><span class="sxs-lookup"><span data-stu-id="0df62-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="0df62-112">Altri valori</span><span class="sxs-lookup"><span data-stu-id="0df62-112">Other values</span></span> | <span data-ttu-id="0df62-113">I certificati per tutti gli scopi nell'archivio certificati del client o del server non sono selezionati per l'autenticazione PEAP.</span><span class="sxs-lookup"><span data-stu-id="0df62-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="0df62-114">Se il valore del registro di sistema non è presente, per l'autenticazione EAP-TLS vengono selezionati i certificati tutti gli scopi nell'archivio certificati del client o del server.</span><span class="sxs-lookup"><span data-stu-id="0df62-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0df62-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0df62-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0df62-116">Impostazioni del registro di sistema EAPHost</span><span class="sxs-lookup"><span data-stu-id="0df62-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




