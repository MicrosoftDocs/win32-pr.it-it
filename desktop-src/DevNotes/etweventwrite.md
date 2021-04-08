---
description: 'Altre informazioni su: funzione EtwEventWrite'
title: EtwEventWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 149f611dfb298749befca805509e05fa2dec497a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049236"
---
# <a name="etweventwrite-function"></a><span data-ttu-id="7b948-103">EtwEventWrite (funzione)</span><span class="sxs-lookup"><span data-stu-id="7b948-103">EtwEventWrite function</span></span>

<span data-ttu-id="7b948-104">[La funzione EtwEventWrite e le strutture restituite sono interne al sistema operativo e soggette a modifiche da una versione di Windows a un'altra.]</span><span class="sxs-lookup"><span data-stu-id="7b948-104">[The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="7b948-105">Scrive un evento di base in una sessione.</span><span class="sxs-lookup"><span data-stu-id="7b948-105">Writes a basic event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b948-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b948-106">Syntax</span></span>

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="7b948-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b948-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b948-108">*RegHandle*</span><span class="sxs-lookup"><span data-stu-id="7b948-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="7b948-109">RegHandle per il provider.</span><span class="sxs-lookup"><span data-stu-id="7b948-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="7b948-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="7b948-110">*EventDescriptor*</span></span>
</dt> <dd>

<span data-ttu-id="7b948-111">Descrittore dell'evento da registrare.</span><span class="sxs-lookup"><span data-stu-id="7b948-111">Event descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="7b948-112">*UserDataCount*</span><span class="sxs-lookup"><span data-stu-id="7b948-112">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="7b948-113">Numero di elementi di dati utente.</span><span class="sxs-lookup"><span data-stu-id="7b948-113">Number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="7b948-114">*UserData*</span><span class="sxs-lookup"><span data-stu-id="7b948-114">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="7b948-115">Puntatore a una matrice di elementi di dati utente.</span><span class="sxs-lookup"><span data-stu-id="7b948-115">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b948-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b948-116">Return value</span></span>

<span data-ttu-id="7b948-117">Codice di errore Win32.</span><span class="sxs-lookup"><span data-stu-id="7b948-117">A Win32 error code.</span></span>


## <a name="remarks"></a><span data-ttu-id="7b948-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b948-118">Remarks</span></span>

<span data-ttu-id="7b948-119">La funzione EtwEventWrite e le strutture restituite sono interne al sistema operativo e sono soggette a modifiche da una versione di Windows a un'altra.</span><span class="sxs-lookup"><span data-stu-id="7b948-119">The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="7b948-120">Per mantenere la compatibilità dell'applicazione, è preferibile usare invece le funzioni pubbliche.</span><span class="sxs-lookup"><span data-stu-id="7b948-120">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b948-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b948-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7b948-122">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="7b948-122">**Target Platform**</span></span> | <span data-ttu-id="7b948-123">Windows</span><span class="sxs-lookup"><span data-stu-id="7b948-123">Windows</span></span> |
| <span data-ttu-id="7b948-124">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="7b948-124">**Header**</span></span> | <span data-ttu-id="7b948-125">ntetw. h</span><span class="sxs-lookup"><span data-stu-id="7b948-125">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="7b948-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b948-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b948-127">EventWrite</span><span class="sxs-lookup"><span data-stu-id="7b948-127">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="7b948-128">EventWriteEx</span><span class="sxs-lookup"><span data-stu-id="7b948-128">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
