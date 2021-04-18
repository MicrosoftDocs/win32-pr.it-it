---
description: Gestione di Unicode in un'applicazione IME-Aware
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Gestione di Unicode in un'applicazione IME-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319500"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a><span data-ttu-id="602c8-103">Gestione di Unicode in un'applicazione IME-Aware</span><span class="sxs-lookup"><span data-stu-id="602c8-103">Handling Unicode in an IME-Aware Application</span></span>

<span data-ttu-id="602c8-104">Per IMM e la relativa gestione di Unicode sono necessari due problemi.</span><span class="sxs-lookup"><span data-stu-id="602c8-104">Two issues are involved with the IMM and its handling of Unicode.</span></span> <span data-ttu-id="602c8-105">Il primo problema è che le versioni Unicode delle funzioni di IMM recuperano la dimensione di un buffer in byte invece di caratteri Unicode a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="602c8-105">The first issue is that the Unicode versions of IMM functions retrieve the size of a buffer in bytes instead of 16-bit Unicode characters.</span></span> <span data-ttu-id="602c8-106">Il secondo problema è che IMM recupera in genere i caratteri Unicode, anziché i caratteri DBCS, nei messaggi [**WM \_ char**](../inputdev/wm-char.md) e [**WM \_ IME \_ char**](wm-ime-char.md) .</span><span class="sxs-lookup"><span data-stu-id="602c8-106">The second issue is that the IMM normally retrieves Unicode characters (instead of DBCS characters) in the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages.</span></span>

<span data-ttu-id="602c8-107">Windows supporta un'interfaccia Unicode per IMM, oltre all'interfaccia ANSI supportata originariamente.</span><span class="sxs-lookup"><span data-stu-id="602c8-107">Windows supports a Unicode interface for the IMM, in addition to the ANSI interface originally supported.</span></span>

<span data-ttu-id="602c8-108">Le applicazioni devono usare [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) per fare in modo che i messaggi di tipo char [**WM \_**](../inputdev/wm-char.md) e [**WM \_ \_ IME**](wm-ime-char.md) recuperino i caratteri Unicode anziché i caratteri DBCS nel parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="602c8-108">Your applications should use [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) to cause the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages to retrieve Unicode characters instead of DBCS characters in the *wParam* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="602c8-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="602c8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="602c8-110">Uso di gestione metodi di input</span><span class="sxs-lookup"><span data-stu-id="602c8-110">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
