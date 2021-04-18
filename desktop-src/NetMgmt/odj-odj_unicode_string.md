---
title: ODJ_UNICODE_STRING
description: Definizione di ODJ_UNICODE_STRING IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "106300653"
---
# <a name="odj_unicode_string-structure"></a><span data-ttu-id="46280-103">Struttura ODJ_UNICODE_STRING</span><span class="sxs-lookup"><span data-stu-id="46280-103">ODJ_UNICODE_STRING structure</span></span>

<span data-ttu-id="46280-104">Contiene una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="46280-104">Contains a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="46280-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46280-105">Syntax</span></span>

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a><span data-ttu-id="46280-106">Members</span><span class="sxs-lookup"><span data-stu-id="46280-106">Members</span></span>

### <a name="length"></a><span data-ttu-id="46280-107">Length</span><span class="sxs-lookup"><span data-stu-id="46280-107">Length</span></span>

<span data-ttu-id="46280-108">Deve essere impostato sul numero di byte nel buffer contenente la stringa, escluso il carattere di terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="46280-108">Must be set to the number of bytes in Buffer containing the string, not including the NULL terminator.</span></span>

### <a name="maximumlength"></a><span data-ttu-id="46280-109">MaximumLength</span><span class="sxs-lookup"><span data-stu-id="46280-109">MaximumLength</span></span>

<span data-ttu-id="46280-110">DEVE essere impostato sul numero totale di byte nel buffer, escluso il carattere di terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="46280-110">This MUST be set to the total number of bytes in Buffer, not including the NULL terminator.</span></span>

### <a name="buffer"></a><span data-ttu-id="46280-111">Buffer</span><span class="sxs-lookup"><span data-stu-id="46280-111">Buffer</span></span>

<span data-ttu-id="46280-112">Deve essere una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="46280-112">Must be a Unicode string.</span></span>

## <a name="see-also"></a><span data-ttu-id="46280-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46280-113">See also</span></span>

[<span data-ttu-id="46280-114">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="46280-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
