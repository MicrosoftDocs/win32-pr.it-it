---
title: OP_JOINPROV3_PART
description: Definizione di OP_JOINPROV3_PART IDL
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104399877"
---
# <a name="op_joinprov3_part-structure"></a><span data-ttu-id="e5fa0-103">Struttura OP_JOINPROV3_PART</span><span class="sxs-lookup"><span data-stu-id="e5fa0-103">OP_JOINPROV3_PART structure</span></span>

<span data-ttu-id="e5fa0-104">Contiene informazioni aggiuntive utilizzate per la configurazione di un client aggiunto a un dominio.</span><span class="sxs-lookup"><span data-stu-id="e5fa0-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5fa0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5fa0-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a><span data-ttu-id="e5fa0-106">Members</span><span class="sxs-lookup"><span data-stu-id="e5fa0-106">Members</span></span>

### <a name="rid"></a><span data-ttu-id="e5fa0-107">Sbarazzarsi</span><span class="sxs-lookup"><span data-stu-id="e5fa0-107">Rid</span></span>

<span data-ttu-id="e5fa0-108">Deve essere impostato sull'identificatore relativo del SID dell'account del computer</span><span class="sxs-lookup"><span data-stu-id="e5fa0-108">Must be set to the Relative Identifier of the machine account’s SID</span></span>

### <a name="lpsid"></a><span data-ttu-id="e5fa0-109">lpSid</span><span class="sxs-lookup"><span data-stu-id="e5fa0-109">lpSid</span></span>

<span data-ttu-id="e5fa0-110">Deve essere impostato sul SID dell'account del computer in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="e5fa0-110">Must be set to the SID of the machine account in string form.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5fa0-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5fa0-111">See also</span></span>

[<span data-ttu-id="e5fa0-112">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="e5fa0-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
