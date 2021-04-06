---
title: ProxyStubClsid
description: Esegue il mapping di un IID a un CLSID nelle DLL proxy a 16 bit.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Valore ProxyStubClsid del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045119"
---
# <a name="proxystubclsid"></a><span data-ttu-id="60971-104">ProxyStubClsid</span><span class="sxs-lookup"><span data-stu-id="60971-104">ProxyStubClsid</span></span>

<span data-ttu-id="60971-105">Esegue il mapping di un IID a un CLSID nelle DLL proxy a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="60971-105">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="60971-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="60971-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="60971-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="60971-107">Remarks</span></span>

<span data-ttu-id="60971-108">Si tratta di un valore **reg \_ SZ** che specifica il CLSID per l'IID.</span><span class="sxs-lookup"><span data-stu-id="60971-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="60971-109">Se si aggiungono interfacce, è necessario utilizzare questa voce per registrarle (sistemi a 16 bit) in modo che OLE possa trovare il codice remoto appropriato per stabilire la comunicazione interprocesso.</span><span class="sxs-lookup"><span data-stu-id="60971-109">If you add interfaces, you must use this entry to register them (16-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60971-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60971-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60971-111">**Interfaccia**</span><span class="sxs-lookup"><span data-stu-id="60971-111">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="60971-112">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="60971-112">**ProxyStubClsid32**</span></span>](proxystubclsid32.md)
</dt> </dl>

 

 




