---
description: Definisce una cache della metrica del tipo di carattere Uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317142"
---
# <a name="script_cache"></a><span data-ttu-id="22b43-103">\_cache script</span><span class="sxs-lookup"><span data-stu-id="22b43-103">SCRIPT\_CACHE</span></span>

<span data-ttu-id="22b43-104">Definisce una cache della metrica del tipo di carattere Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="22b43-104">Defines a Uniscribe font metric cache.</span></span>


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a><span data-ttu-id="22b43-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="22b43-105">Remarks</span></span>

<span data-ttu-id="22b43-106">Si tratta di una struttura opaca.</span><span class="sxs-lookup"><span data-stu-id="22b43-106">This is an opaque structure.</span></span> <span data-ttu-id="22b43-107">L'applicazione deve allocare e mantenere una \_ variabile di cache di script per ogni stile di carattere usato.</span><span class="sxs-lookup"><span data-stu-id="22b43-107">The application must allocate and retain one SCRIPT\_CACHE variable for each character style used.</span></span> <span data-ttu-id="22b43-108">La variabile deve essere inizializzata su **null**.</span><span class="sxs-lookup"><span data-stu-id="22b43-108">The variable must be initialized to **NULL**.</span></span>

<span data-ttu-id="22b43-109">Molte funzioni di script accettano una combinazione di un handle di contesto di dispositivo hardware e una \_ variabile della cache di script.</span><span class="sxs-lookup"><span data-stu-id="22b43-109">Many script functions take a combination of a hardware device context handle and a SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="22b43-110">Uniscribe tenta prima di tutto di accedere ai dati del tipo di carattere tramite la \_ variabile cache script.</span><span class="sxs-lookup"><span data-stu-id="22b43-110">Uniscribe first attempts to access font data by using the SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="22b43-111">Controlla solo il contesto del dispositivo hardware se i dati necessari non sono già memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="22b43-111">It only inspects the hardware device context if the required data is not already cached.</span></span>

<span data-ttu-id="22b43-112">L'handle di contesto del dispositivo hardware può essere passato a Uniscribe come **null**.</span><span class="sxs-lookup"><span data-stu-id="22b43-112">The hardware device context handle can be passed to Uniscribe as **NULL**.</span></span> <span data-ttu-id="22b43-113">Se i dati richiesti da Uniscribe sono già memorizzati nella cache, il contesto di dispositivo non è accessibile e l'operazione continua normalmente.</span><span class="sxs-lookup"><span data-stu-id="22b43-113">If data required by Uniscribe is already cached, the device context is not accessed, and the operation continues normally.</span></span>

<span data-ttu-id="22b43-114">Se il contesto di dispositivo viene passato come **null** e Uniscribe deve accedervi per qualsiasi motivo, Uniscribe restituisce il codice di errore E \_ in sospeso.</span><span class="sxs-lookup"><span data-stu-id="22b43-114">If the device context is passed as **NULL** and Uniscribe needs to access it for any reason, Uniscribe returns the error code E\_PENDING.</span></span> <span data-ttu-id="22b43-115">Questo codice viene restituito rapidamente, consentendo all'applicazione di evitare lunghe chiamate [**SelezionaOggetto**](/windows/win32/api/wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="22b43-115">This code is returned quickly, allowing the application to avoid time-consuming [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) calls.</span></span>

## <a name="examples"></a><span data-ttu-id="22b43-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="22b43-116">Examples</span></span>

<span data-ttu-id="22b43-117">L'esempio seguente si applica a tutte le funzioni che accettano una \_ variabile della cache script e un handle facoltativo per un contesto di dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="22b43-117">The following example applies to all functions that take a SCRIPT\_CACHE variable and an optional handle to a hardware device context.</span></span>


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a><span data-ttu-id="22b43-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22b43-118">Requirements</span></span>



| <span data-ttu-id="22b43-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="22b43-119">Requirement</span></span> | <span data-ttu-id="22b43-120">Valore</span><span class="sxs-lookup"><span data-stu-id="22b43-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22b43-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22b43-121">Minimum supported client</span></span><br/> | <span data-ttu-id="22b43-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22b43-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="22b43-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22b43-123">Minimum supported server</span></span><br/> | <span data-ttu-id="22b43-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22b43-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="22b43-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22b43-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="22b43-126"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b43-126"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22b43-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22b43-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b43-128">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="22b43-128">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="22b43-129">Strutture Uniscribe</span><span class="sxs-lookup"><span data-stu-id="22b43-129">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="22b43-130">Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="22b43-130">Caching</span></span>](caching.md)
</dt> </dl>

 

 
