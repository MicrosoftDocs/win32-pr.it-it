---
title: valore booleano (WMI)
description: '\_Parametro bool di VT che accetta il valore di Variant \_ TRUE (&\# 8211; 1) o Variant \_ false (0).'
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316574"
---
# <a name="boolean-wmi"></a><span data-ttu-id="ea28b-103">valore booleano (WMI)</span><span class="sxs-lookup"><span data-stu-id="ea28b-103">boolean (WMI)</span></span>

<span data-ttu-id="ea28b-104">Il tipo di dati Boolean è un \_ parametro di VT bool che accetta il valore di Variant \_ true (-1) o Variant \_ false (0).</span><span class="sxs-lookup"><span data-stu-id="ea28b-104">The boolean data type is a VT\_BOOL parameter that takes on the value of VARIANT\_TRUE (–1) or VARIANT\_FALSE (0).</span></span> <span data-ttu-id="ea28b-105">Nella tabella seguente sono elencate le differenze tra le rappresentazioni a livello di codice di Logical **true** in C/C++ e il tipo di automazione.</span><span class="sxs-lookup"><span data-stu-id="ea28b-105">The following table lists the difference between the programmatic representations of logical **TRUE** in C/C++ and the Automation type.</span></span>

| <span data-ttu-id="ea28b-106">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="ea28b-106">Language</span></span>   | <span data-ttu-id="ea28b-107">Valore</span><span class="sxs-lookup"><span data-stu-id="ea28b-107">Value</span></span>         | <span data-ttu-id="ea28b-108">Valore numerico</span><span class="sxs-lookup"><span data-stu-id="ea28b-108">Numerical value</span></span> |
|------------|---------------|-----------------|
| <span data-ttu-id="ea28b-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="ea28b-109">C/C++</span></span>      | <span data-ttu-id="ea28b-110">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ea28b-110">**TRUE**</span></span>      | <span data-ttu-id="ea28b-111">1</span><span class="sxs-lookup"><span data-stu-id="ea28b-111">1</span></span>               |
| <span data-ttu-id="ea28b-112">Automazione</span><span class="sxs-lookup"><span data-stu-id="ea28b-112">Automation</span></span> | <span data-ttu-id="ea28b-113">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="ea28b-113">VARIANT\_TRUE</span></span> | <span data-ttu-id="ea28b-114">–1</span><span class="sxs-lookup"><span data-stu-id="ea28b-114">–1</span></span>              |

<span data-ttu-id="ea28b-115">Entrambi i tipi sono diversi da zero e pertanto non sono **false**, ma hanno rappresentazioni diverse per **true**.</span><span class="sxs-lookup"><span data-stu-id="ea28b-115">Both types are nonzero and therefore not **FALSE**, but have different representations for **TRUE**.</span></span>
