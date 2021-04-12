---
title: opzione/oldtlb
description: L'opzione/oldtlb indica al compilatore MIDL di generare una libreria dei tipi in formato obsoleto.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- /oldtlb switch MIDL
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398910"
---
# <a name="oldtlb-switch"></a><span data-ttu-id="6582c-104">opzione/oldtlb</span><span class="sxs-lookup"><span data-stu-id="6582c-104">/oldtlb switch</span></span>

<span data-ttu-id="6582c-105">L'opzione **/oldtlb** indica al compilatore MIDL di generare una libreria dei tipi in formato obsoleto.</span><span class="sxs-lookup"><span data-stu-id="6582c-105">The **/oldtlb** switch directs the MIDL compiler to generate an old-format type library.</span></span>

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a><span data-ttu-id="6582c-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="6582c-106">Switch Options</span></span>

<span data-ttu-id="6582c-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="6582c-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="6582c-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="6582c-108">Remarks</span></span>

<span data-ttu-id="6582c-109">L'opzione **/oldtlb** esegue l'override del valore predefinito e indica al compilatore MIDL di generare librerie dei tipi obsolete anche nelle versioni correnti di Windows usando [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) anziché [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span><span class="sxs-lookup"><span data-stu-id="6582c-109">The **/oldtlb** switch overrides the default and directs the MIDL compiler to generate old-format type libraries even on current versions of Windows by using [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) instead of [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span></span>

## <a name="examples"></a><span data-ttu-id="6582c-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="6582c-110">Examples</span></span>

<span data-ttu-id="6582c-111">**MIDL/oldtlb nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="6582c-111">**midl /oldtlb filename.idl**</span></span>

<span data-ttu-id="6582c-112">**MIDL/oldtlb myoldodl. FAD**</span><span class="sxs-lookup"><span data-stu-id="6582c-112">**midl /oldtlb myoldodl.odl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6582c-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6582c-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6582c-114">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="6582c-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6582c-115">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="6582c-115">**/newtlb**</span></span>](-newtlb.md)
</dt> </dl>

 

 