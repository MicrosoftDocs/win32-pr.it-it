---
title: add timeout
description: Aggiunge un timeout globale al servizio HTTP.sys.
ms.assetid: c59a64e2-36aa-4428-b727-df21f5632d0d
keywords:
- Aggiungi timeout HTTP
topic_type:
- apiref
api_name:
- add timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2637cb5db663ea36b15eb382a16b02b166e98f88
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104398097"
---
# <a name="add-timeout"></a><span data-ttu-id="d87bc-104">add timeout</span><span class="sxs-lookup"><span data-stu-id="d87bc-104">add timeout</span></span>

<span data-ttu-id="d87bc-105">Aggiunge un timeout globale al servizio HTTP.sys.</span><span class="sxs-lookup"><span data-stu-id="d87bc-105">Adds a global timeout to the HTTP.sys service.</span></span>

``` syntax
add timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
            [value=]u-short

 
```

## <a name="parameters"></a><span data-ttu-id="d87bc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d87bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d87bc-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {IdleConnectionTimeout \| HeaderWaitTimeout}**</span><span class="sxs-lookup"><span data-stu-id="d87bc-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype=\]{idleconnectiontimeout\|headerwaittimeout}**</span></span>
</dt> <dd>

<span data-ttu-id="d87bc-108">Specifica il tipo di timeout per l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="d87bc-108">Specifies the type of timeout for setting.</span></span>

</dd> <dt>

<span data-ttu-id="d87bc-109"><span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>\**\[valore = \] \* \* \* u-Short*</span><span class="sxs-lookup"><span data-stu-id="d87bc-109"><span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>\**\[value=\]\*\*\*u-short*</span></span>
</dt> <dd>

<span data-ttu-id="d87bc-110">Specifica il valore del timeout (in secondi).</span><span class="sxs-lookup"><span data-stu-id="d87bc-110">Specifies the value of the timeout (in seconds).</span></span> <span data-ttu-id="d87bc-111">Se il valore è esadecimale, aggiungere il prefisso 0x.</span><span class="sxs-lookup"><span data-stu-id="d87bc-111">If value is hexadecimal, then add the prefix 0x.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d87bc-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="d87bc-112">Examples</span></span>

<span data-ttu-id="d87bc-113">**add timeout timeouttype=idleconnectiontimeout value=120**</span><span class="sxs-lookup"><span data-stu-id="d87bc-113">**add timeout timeouttype=idleconnectiontimeout value=120**</span></span>

<span data-ttu-id="d87bc-114">**add timeout timeouttype=headerwaittimeout value=0x40**</span><span class="sxs-lookup"><span data-stu-id="d87bc-114">**add timeout timeouttype=headerwaittimeout value=0x40**</span></span>

 

 




