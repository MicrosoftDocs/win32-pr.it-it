---
title: OverrideEAPCertificateSelection
description: La chiave del registro di sistema OverrideEAPCertificateSelection determina se il client eseguirà l'override del comportamento predefinito per la selezione del certificato della smart card e fornirà all'utente più certificati tra cui scegliere.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857854"
---
# <a name="overrideeapcertificateselection"></a><span data-ttu-id="d7b0b-103">OverrideEAPCertificateSelection</span><span class="sxs-lookup"><span data-stu-id="d7b0b-103">OverrideEAPCertificateSelection</span></span>

<span data-ttu-id="d7b0b-104">La chiave del registro di sistema OverrideEAPCertificateSelection determina se il client eseguirà l'override del comportamento predefinito per la selezione del certificato della smart card e fornirà all'utente più certificati tra cui scegliere.</span><span class="sxs-lookup"><span data-stu-id="d7b0b-104">The OverrideEAPCertificateSelection registry key determines whether the client will override the default smart card certificate selection behavior and provide the user with more certificates to choose from.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d7b0b-105">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="d7b0b-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a><span data-ttu-id="d7b0b-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7b0b-106">Remarks</span></span>

<span data-ttu-id="d7b0b-107">Si tratta di un valore **\_ binario REG** .</span><span class="sxs-lookup"><span data-stu-id="d7b0b-107">This is a **REG\_BINARY** value.</span></span>



| <span data-ttu-id="d7b0b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d7b0b-108">Value</span></span> | <span data-ttu-id="d7b0b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7b0b-109">Description</span></span>                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b0b-110">0x000</span><span class="sxs-lookup"><span data-stu-id="d7b0b-110">0x000</span></span> | <span data-ttu-id="d7b0b-111">Non eseguire l'override del comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="d7b0b-111">Do not override the default behavior.</span></span>                                                                                                                                                                |
| <span data-ttu-id="d7b0b-112">0x001</span><span class="sxs-lookup"><span data-stu-id="d7b0b-112">0x001</span></span> | <span data-ttu-id="d7b0b-113">Scegliere l'ultimo certificato collegato dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="d7b0b-113">Choose the last attached certificate from the smart card.</span></span>                                                                                                                                            |
| <span data-ttu-id="d7b0b-114">0x010</span><span class="sxs-lookup"><span data-stu-id="d7b0b-114">0x010</span></span> | <span data-ttu-id="d7b0b-115">Mostra tutti i certificati nell'interfaccia utente di selezione dei certificati dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="d7b0b-115">Shows all certificates in the certificate selection UI from the smart card.</span></span>                                                                                                                          |
| <span data-ttu-id="d7b0b-116">0x100</span><span class="sxs-lookup"><span data-stu-id="d7b0b-116">0x100</span></span> | <span data-ttu-id="d7b0b-117">Mostra tutti i certificati nell'interfaccia utente di selezione del certificato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d7b0b-117">Shows all certificates in the certificate selection UI from the registry.</span></span>                                                                                                                            |
| <span data-ttu-id="d7b0b-118">0x101</span><span class="sxs-lookup"><span data-stu-id="d7b0b-118">0x101</span></span> | <span data-ttu-id="d7b0b-119">Mostra tutti i certificati nell'interfaccia utente di selezione del certificato dal registro di sistema e l'ultimo certificato collegato dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="d7b0b-119">Shows all certificates in the certificate selection UI from the registry and the last attached certificate from the smart card.</span></span> <span data-ttu-id="d7b0b-120">Mostra l'ultimo certificato collegato dalla smart card selezionato.</span><span class="sxs-lookup"><span data-stu-id="d7b0b-120">Shows the last attached certificate from the smart card as selected.</span></span> |
| <span data-ttu-id="d7b0b-121">0x110</span><span class="sxs-lookup"><span data-stu-id="d7b0b-121">0x110</span></span> | <span data-ttu-id="d7b0b-122">Mostra tutti i certificati nell'interfaccia utente di selezione del certificato dal registro di sistema e dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="d7b0b-122">Shows all certificates in the certificate selection UI from the registry and the smart card.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="d7b0b-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7b0b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7b0b-124">Impostazioni del registro di sistema EAPHost</span><span class="sxs-lookup"><span data-stu-id="d7b0b-124">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




