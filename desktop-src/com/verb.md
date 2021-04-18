---
title: Verbo
description: Specifica i verbi da registrare per un'applicazione.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Chiave del registro di sistema verb COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300496"
---
# <a name="verb"></a><span data-ttu-id="d2932-104">Verbo</span><span class="sxs-lookup"><span data-stu-id="d2932-104">Verb</span></span>

<span data-ttu-id="d2932-105">Specifica i verbi da registrare per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2932-105">Specifies the verbs to be registered for an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d2932-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="d2932-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a><span data-ttu-id="d2932-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2932-107">Remarks</span></span>

<span data-ttu-id="d2932-108">Ogni verbo è un **valore \_ reg SZ** nel formato "*nome*, *\_ flag di menu*, *\_ flag verbo*".</span><span class="sxs-lookup"><span data-stu-id="d2932-108">Each verb is a **REG\_SZ** value of the form "*name*, *menu\_flag*, *verb\_flag*".</span></span> <span data-ttu-id="d2932-109">I verbi devono essere numerati consecutivamente.</span><span class="sxs-lookup"><span data-stu-id="d2932-109">Verbs must be numbered consecutively.</span></span>

<span data-ttu-id="d2932-110">Il *nome* descrive il modo in cui il verbo viene accodato da una chiamata di funzione [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) .</span><span class="sxs-lookup"><span data-stu-id="d2932-110">The *name* describes how the verb is appended by an [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function call.</span></span> <span data-ttu-id="d2932-111">Ad esempio, "&Play".</span><span class="sxs-lookup"><span data-stu-id="d2932-111">For example, "&Play".</span></span>

<span data-ttu-id="d2932-112">Il valore del *\_ flag di menu* indica il modo in cui il verbo dovrebbe essere visualizzato nel menu.</span><span class="sxs-lookup"><span data-stu-id="d2932-112">The *menu\_flag* value indicates how the verb should appear in the menu.</span></span> <span data-ttu-id="d2932-113">Sono supportati tutti i flag supportati da [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , ad eccezione di MF \_ bitmap, MF \_ OWNERDRAW e MF \_ popup.</span><span class="sxs-lookup"><span data-stu-id="d2932-113">All flags supported by [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) are supported, except for MF\_BITMAP, MF\_OWNERDRAW, and MF\_POPUP.</span></span>

<span data-ttu-id="d2932-114">Il valore del *\_ flag verb* descrive gli attributi dei verbi.</span><span class="sxs-lookup"><span data-stu-id="d2932-114">The *verb\_flag* value describes attributes of the verbs.</span></span> <span data-ttu-id="d2932-115">Usare uno dei valori di [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)o 0.</span><span class="sxs-lookup"><span data-stu-id="d2932-115">Use one of the values from [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib), or 0.</span></span>

<span data-ttu-id="d2932-116">Per ulteriori informazioni, vedere [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)e [**IOleObject:: EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span><span class="sxs-lookup"><span data-stu-id="d2932-116">For more information, see [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb), and [**IOleObject::EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2932-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2932-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2932-118">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="d2932-118">**AppendMenu**</span></span>](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="d2932-119">**OLEVERB**</span><span class="sxs-lookup"><span data-stu-id="d2932-119">**OLEVERB**</span></span>](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[<span data-ttu-id="d2932-120">**OLEVERBATTRIB**</span><span class="sxs-lookup"><span data-stu-id="d2932-120">**OLEVERBATTRIB**</span></span>](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 