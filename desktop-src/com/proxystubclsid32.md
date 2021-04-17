---
title: ProxyStubClsid32
description: Esegue il mapping di un IID a un CLSID in DLL proxy a 32 bit.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- Valore ProxyStubClsid32 del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339367"
---
# <a name="proxystubclsid32"></a><span data-ttu-id="7a87b-104">ProxyStubClsid32</span><span class="sxs-lookup"><span data-stu-id="7a87b-104">ProxyStubClsid32</span></span>

<span data-ttu-id="7a87b-105">Esegue il mapping di un IID a un CLSID in DLL proxy a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7a87b-105">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7a87b-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="7a87b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="7a87b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a87b-107">Remarks</span></span>

<span data-ttu-id="7a87b-108">Si tratta di un valore **reg \_ SZ** che specifica il CLSID per l'IID.</span><span class="sxs-lookup"><span data-stu-id="7a87b-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="7a87b-109">Si tratta di una voce obbligatoria perché il mapping da IID a CLSID può essere diverso per le interfacce a 16 bit e a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7a87b-109">This is a required entry since the IID-to-CLSID mapping may be different for 16-bit and 32-bit interfaces.</span></span> <span data-ttu-id="7a87b-110">Il mapping da IID a CLSID dipende dal modo in cui i proxy di interfaccia vengono inseriti in un set di DLL proxy.</span><span class="sxs-lookup"><span data-stu-id="7a87b-110">The IID-to-CLSID mapping depends on the way the interface proxies are packaged into a set of proxy DLLs.</span></span>

<span data-ttu-id="7a87b-111">Se si aggiungono interfacce, è necessario utilizzare questa voce per registrarle (sistemi a 32 bit) in modo che OLE possa trovare il codice remoto appropriato per stabilire la comunicazione interprocesso.</span><span class="sxs-lookup"><span data-stu-id="7a87b-111">If you add interfaces, you must use this entry to register them (32-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a87b-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a87b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a87b-113">**IMarshal**</span><span class="sxs-lookup"><span data-stu-id="7a87b-113">**IMarshal**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[<span data-ttu-id="7a87b-114">**Interfaccia**</span><span class="sxs-lookup"><span data-stu-id="7a87b-114">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="7a87b-115">**ProxyStubClsid**</span><span class="sxs-lookup"><span data-stu-id="7a87b-115">**ProxyStubClsid**</span></span>](proxystubclsid.md)
</dt> </dl>

 

 