---
title: VersionIndependentProgID
description: Associa un ProgID a un CLSID. Questo valore viene utilizzato per determinare la versione più recente di un'applicazione dell'oggetto.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- VersionIndependentProgID chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045361"
---
# <a name="versionindependentprogid"></a><span data-ttu-id="3bed6-105">VersionIndependentProgID</span><span class="sxs-lookup"><span data-stu-id="3bed6-105">VersionIndependentProgID</span></span>

<span data-ttu-id="3bed6-106">Associa un ProgID a un CLSID.</span><span class="sxs-lookup"><span data-stu-id="3bed6-106">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="3bed6-107">Questo valore viene utilizzato per determinare la versione più recente di un'applicazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3bed6-107">This value is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3bed6-108">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="3bed6-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a><span data-ttu-id="3bed6-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bed6-109">Remarks</span></span>

<span data-ttu-id="3bed6-110">Si tratta di un valore **reg \_ SZ** che specifica la versione più recente dell'applicazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3bed6-110">This is a **REG\_SZ** value that specifies the latest version of the object application.</span></span>

<span data-ttu-id="3bed6-111">Il ProgID indipendente dalla versione viene archiviato e gestito esclusivamente dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3bed6-111">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="3bed6-112">Quando viene specificato il ProgID indipendente dalla versione, la funzione [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) restituisce il CLSID della versione corrente.</span><span class="sxs-lookup"><span data-stu-id="3bed6-112">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="3bed6-113">È possibile usare [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) per eseguire la conversione tra queste due rappresentazioni.</span><span class="sxs-lookup"><span data-stu-id="3bed6-113">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

 

 




