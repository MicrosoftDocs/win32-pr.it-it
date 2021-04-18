---
title: Interfaccia (COM)
description: Voce facoltativa che specifica tutti gli ID di interfaccia (IID) supportati dalla classe associata.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Chiave del registro di sistema Interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300881"
---
# <a name="interface-com"></a><span data-ttu-id="c5903-104">Interfaccia (COM)</span><span class="sxs-lookup"><span data-stu-id="c5903-104">Interface (COM)</span></span>

<span data-ttu-id="c5903-105">Voce facoltativa che specifica tutti gli ID di interfaccia (IID) supportati dalla classe associata.</span><span class="sxs-lookup"><span data-stu-id="c5903-105">An optional entry that specifies all interface IDs (IIDs) supported by the associated class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c5903-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c5903-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a><span data-ttu-id="c5903-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5903-107">Remarks</span></span>

<span data-ttu-id="c5903-108">Se un nome di interfaccia non è presente nell'elenco, l'interfaccia non può mai essere supportata da un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="c5903-108">If an interface name is not present in this list, the interface can never be supported by an instance of this class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5903-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5903-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5903-110">Chiave interfaccia</span><span class="sxs-lookup"><span data-stu-id="c5903-110">Interface Key</span></span>](interface-key.md)
</dt> </dl>

 

 




