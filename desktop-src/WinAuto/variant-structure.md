---
title: Struttura VARIANT
description: La maggior parte delle funzioni di Microsoft Active Accessibility e delle proprietà e dei metodi IAccessible accetta una struttura VARIANT come parametro. In pratica, la struttura VARIANT è un contenitore per un'Unione di grandi dimensioni che contiene molti tipi di dati.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117979"
---
# <a name="variant-structure"></a><span data-ttu-id="2451c-104">Struttura VARIANT</span><span class="sxs-lookup"><span data-stu-id="2451c-104">VARIANT Structure</span></span>

<span data-ttu-id="2451c-105">La maggior parte delle funzioni di Microsoft Active Accessibility e delle proprietà e dei metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) accetta una struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) come parametro.</span><span class="sxs-lookup"><span data-stu-id="2451c-105">Most of the Microsoft Active Accessibility functions and the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods take a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure as a parameter.</span></span> <span data-ttu-id="2451c-106">In pratica, la struttura **Variant** è un contenitore per un'Unione di grandi dimensioni che contiene molti tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="2451c-106">Essentially, the **VARIANT** structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="2451c-107">Il valore nel primo membro della struttura, **VT**, descrive quale dei membri di Unione è valido.</span><span class="sxs-lookup"><span data-stu-id="2451c-107">The value in the first member of the structure, **vt**, describes which of the union members is valid.</span></span> <span data-ttu-id="2451c-108">Sebbene la struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) supporti molti tipi di dati diversi, Microsoft Active Accessibility utilizza solo i tipi seguenti.</span><span class="sxs-lookup"><span data-stu-id="2451c-108">Although the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure supports many different data types, Microsoft Active Accessibility uses only the following types.</span></span>



| <span data-ttu-id="2451c-109">Valore VT</span><span class="sxs-lookup"><span data-stu-id="2451c-109">vt Value</span></span>     | <span data-ttu-id="2451c-110">Nome del membro del valore corrispondente</span><span class="sxs-lookup"><span data-stu-id="2451c-110">Corresponding value member name</span></span> |
|--------------|---------------------------------|
| <span data-ttu-id="2451c-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2451c-111">VT\_I4</span></span>       | <span data-ttu-id="2451c-112">**lVal**</span><span class="sxs-lookup"><span data-stu-id="2451c-112">**lVal**</span></span>                        |
| <span data-ttu-id="2451c-113">\_invio VT</span><span class="sxs-lookup"><span data-stu-id="2451c-113">VT\_DISPATCH</span></span> | <span data-ttu-id="2451c-114">**pdispVal**</span><span class="sxs-lookup"><span data-stu-id="2451c-114">**pdispVal**</span></span>                    |
| <span data-ttu-id="2451c-115">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="2451c-115">VT\_BSTR</span></span>     | <span data-ttu-id="2451c-116">**bstrVal**</span><span class="sxs-lookup"><span data-stu-id="2451c-116">**bstrVal**</span></span>                     |
| <span data-ttu-id="2451c-117">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="2451c-117">VT\_EMPTY</span></span>    | <span data-ttu-id="2451c-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2451c-118">none</span></span>                            |



 

<span data-ttu-id="2451c-119">Quando si ricevono informazioni in una struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , controllare il membro **VT** per individuare il membro che contiene dati validi.</span><span class="sxs-lookup"><span data-stu-id="2451c-119">When you receive information in a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure, check the **vt** member to find out which member contains valid data.</span></span> <span data-ttu-id="2451c-120">Analogamente, quando si inviano informazioni utilizzando una struttura **Variant** , impostare sempre **VT** per riflettere il membro dell'Unione che contiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="2451c-120">Similarly, when you send information using a **VARIANT** structure, always set **vt** to reflect the union member that contains the information.</span></span>

<span data-ttu-id="2451c-121">Prima di utilizzare la struttura, inizializzarla chiamando la funzione [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="2451c-121">Before using the structure, initialize it by calling the [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM) function.</span></span> <span data-ttu-id="2451c-122">Al termine della struttura, cancellarlo prima che la memoria che contiene la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) venga liberata chiamando [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span><span class="sxs-lookup"><span data-stu-id="2451c-122">When finished with the structure, clear it before the memory that contains the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) is freed by calling [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span></span>

 

 