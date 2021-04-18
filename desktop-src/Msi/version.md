---
description: Il tipo di dati Version è una stringa di testo contenente una stringa di versione valida.
ms.assetid: 0b19a7fb-7390-47a7-83ca-6b86ab871197
title: Versione (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f7d5e8106f75a147de0ac05ac1434b3b81ae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305622"
---
# <a name="version-windows-installer"></a><span data-ttu-id="2b69d-103">Versione (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="2b69d-103">Version (Windows Installer)</span></span>

<span data-ttu-id="2b69d-104">Il tipo di dati Version è una stringa di testo contenente una stringa di versione valida.</span><span class="sxs-lookup"><span data-stu-id="2b69d-104">The Version data type is a text string containing a valid version string.</span></span> <span data-ttu-id="2b69d-105">Il formato di una stringa di versione è</span><span class="sxs-lookup"><span data-stu-id="2b69d-105">A version string has the format</span></span>

``` syntax
xxxxx.xxxxx.xxxxx.xxxxx
```

<span data-ttu-id="2b69d-106">dove *x* è una cifra.</span><span class="sxs-lookup"><span data-stu-id="2b69d-106">where *x* is a digit.</span></span>

<span data-ttu-id="2b69d-107">La stringa di versione massima accettabile è 65535.65535.65535.65535.</span><span class="sxs-lookup"><span data-stu-id="2b69d-107">The maximum acceptable version string is 65535.65535.65535.65535.</span></span>

<span data-ttu-id="2b69d-108">Di seguito sono riportati alcuni esempi di stringhe di versione valide:</span><span class="sxs-lookup"><span data-stu-id="2b69d-108">The following are examples of valid version strings:</span></span>

-   <span data-ttu-id="2b69d-109">1</span><span class="sxs-lookup"><span data-stu-id="2b69d-109">1</span></span>
-   <span data-ttu-id="2b69d-110">1,0</span><span class="sxs-lookup"><span data-stu-id="2b69d-110">1.0</span></span>
-   <span data-ttu-id="2b69d-111">1,00</span><span class="sxs-lookup"><span data-stu-id="2b69d-111">1.00</span></span>
-   <span data-ttu-id="2b69d-112">10,00</span><span class="sxs-lookup"><span data-stu-id="2b69d-112">10.00</span></span>
-   <span data-ttu-id="2b69d-113">1.00.1</span><span class="sxs-lookup"><span data-stu-id="2b69d-113">1.00.1</span></span>
-   <span data-ttu-id="2b69d-114">1.0.1</span><span class="sxs-lookup"><span data-stu-id="2b69d-114">1.0.1</span></span>
-   <span data-ttu-id="2b69d-115">1.00.10</span><span class="sxs-lookup"><span data-stu-id="2b69d-115">1.00.10</span></span>
-   <span data-ttu-id="2b69d-116">1.00.100</span><span class="sxs-lookup"><span data-stu-id="2b69d-116">1.00.100</span></span>
-   <span data-ttu-id="2b69d-117">1.0.1000.0</span><span class="sxs-lookup"><span data-stu-id="2b69d-117">1.0.1000.0</span></span>

 

 



