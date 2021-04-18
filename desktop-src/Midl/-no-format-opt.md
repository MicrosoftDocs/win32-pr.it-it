---
title: /no_format_opt opzione
description: Il \_ cambio di formato/No \_ opz cambia il modo in cui MIDL ottimizza i descrittori di tipi e procedure.
ms.assetid: 721ac828-7b47-4991-8bce-f9babf6c77a8
keywords:
- /no_format_opt switch MIDL
topic_type:
- apiref
api_name:
- /no_format_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d6e54b963c9637c4f5a583fc9d8f44a0f2880e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299229"
---
# <a name="no_format_opt-switch"></a><span data-ttu-id="9baff-104">\_ \_ opzione opz Format/no</span><span class="sxs-lookup"><span data-stu-id="9baff-104">/no\_format\_opt switch</span></span>

<span data-ttu-id="9baff-105">Il cambio di **\_ formato/No \_ opz** cambia il modo in cui MIDL ottimizza i descrittori di tipi e procedure.</span><span class="sxs-lookup"><span data-stu-id="9baff-105">The **/no\_format\_opt** switch changes the way MIDL optimizes type and procedure descriptors.</span></span>

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a><span data-ttu-id="9baff-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="9baff-106">Switch Options</span></span>

<span data-ttu-id="9baff-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="9baff-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9baff-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9baff-108">Remarks</span></span>

<span data-ttu-id="9baff-109">Per impostazione predefinita, MIDL Elimina i descrittori di tipo e di stored procedure duplicati per ridurre le dimensioni del codice stub generato.</span><span class="sxs-lookup"><span data-stu-id="9baff-109">By default, MIDL eliminates duplicate type and procedure descriptors in order to reduce the size of the generated stub code.</span></span> <span data-ttu-id="9baff-110">L'uso dell'opzione **/No \_ Format \_ opt** disattiva questo comportamento di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="9baff-110">Using the **/no\_format\_opt** switch turns off this optimizing behavior.</span></span>

## <a name="examples"></a><span data-ttu-id="9baff-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="9baff-111">Examples</span></span>

<span data-ttu-id="9baff-112">**MIDL/No \_ Format \_ opz Lean. idl**</span><span class="sxs-lookup"><span data-stu-id="9baff-112">**midl /no\_format\_opt mylean.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="9baff-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9baff-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9baff-114">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="9baff-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="9baff-115">**/OI**</span><span class="sxs-lookup"><span data-stu-id="9baff-115">**/Oi**</span></span>](-oi.md)
</dt> </dl>

 

 




