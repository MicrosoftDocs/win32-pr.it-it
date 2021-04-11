---
description: "Quando un'applicazione esegue un'operazione IPropertyStorage:: WriteMultiple su qualsiasi proprietà WIA (Windows Image Acquisition) scrivibile, il driver WIA esegue una convalida sul nuovo valore della proprietà."
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Convalida della proprietà WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226134"
---
# <a name="wia-property-validation"></a><span data-ttu-id="2ed17-103">Convalida della proprietà WIA</span><span class="sxs-lookup"><span data-stu-id="2ed17-103">WIA Property Validation</span></span>

<span data-ttu-id="2ed17-104">Quando un'applicazione esegue un'operazione [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) su qualsiasi proprietà WIA (Windows Image Acquisition) scrivibile, il driver WIA esegue una convalida sul nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="2ed17-104">When an application performs an [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation on any writeable Windows Image Acquisition (WIA) property, the WIA driver performs a validation on the new property value.</span></span> <span data-ttu-id="2ed17-105">La scrittura di una proprietà può avere effetti collaterali che modificano altri valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="2ed17-105">Writing one property may have side affects that change other property values.</span></span> <span data-ttu-id="2ed17-106">È necessario che l'applicazione legga tutti i valori delle proprietà dopo un'operazione di scrittura per determinare che tutte le proprietà sono impostate sui valori desiderati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2ed17-106">It is up to the application to read all property values after a write operation to determine that all properties are set to values the application desires.</span></span>

<span data-ttu-id="2ed17-107">È possibile scrivere più proprietà contemporaneamente usando l'operazione [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) .</span><span class="sxs-lookup"><span data-stu-id="2ed17-107">Multiple properties can be written simultaneously using the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation.</span></span> <span data-ttu-id="2ed17-108">In alcuni casi è possibile che alcune assegnazioni di proprietà siano in conflitto.</span><span class="sxs-lookup"><span data-stu-id="2ed17-108">There may be cases where some property assignments conflict.</span></span> <span data-ttu-id="2ed17-109">In questi casi, la priorità usata per risolvere i conflitti è la seguente:</span><span class="sxs-lookup"><span data-stu-id="2ed17-109">In such cases, the priority used to resolve conflicts is as follows:</span></span>

1.  <span data-ttu-id="2ed17-110">\_finalità del cur degli indirizzi IP WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="2ed17-110">WIA\_IPS\_CUR\_INTENT</span></span>
2.  <span data-ttu-id="2ed17-111">tipo di dati \_ IPA WIA \_</span><span class="sxs-lookup"><span data-stu-id="2ed17-111">WIA\_IPA\_DATATYPE</span></span>
3.  <span data-ttu-id="2ed17-112">\_profondità IPA \_ WIA</span><span class="sxs-lookup"><span data-stu-id="2ed17-112">WIA\_IPA\_DEPTH</span></span>
4.  <span data-ttu-id="2ed17-113">\_indirizzi IP WIA \_ XRES</span><span class="sxs-lookup"><span data-stu-id="2ed17-113">WIA\_IPS\_XRES</span></span>
5.  <span data-ttu-id="2ed17-114">\_indirizzi IP WIA \_ YRES</span><span class="sxs-lookup"><span data-stu-id="2ed17-114">WIA\_IPS\_YRES</span></span>
6.  <span data-ttu-id="2ed17-115">\_indirizzi IP WIA \_ XPos</span><span class="sxs-lookup"><span data-stu-id="2ed17-115">WIA\_IPS\_XPOS</span></span>
7.  <span data-ttu-id="2ed17-116">\_indirizzi IP WIA \_ YPos</span><span class="sxs-lookup"><span data-stu-id="2ed17-116">WIA\_IPS\_YPOS</span></span>
8.  <span data-ttu-id="2ed17-117">\_indirizzi IP WIA \_ stampa</span><span class="sxs-lookup"><span data-stu-id="2ed17-117">WIA\_IPS\_XEXTENT</span></span>
9.  <span data-ttu-id="2ed17-118">\_indirizzi IP WIA \_ YEXTENT</span><span class="sxs-lookup"><span data-stu-id="2ed17-118">WIA\_IPS\_YEXTENT</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ed17-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ed17-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed17-120">**IWiaPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="2ed17-120">**IWiaPropertyStorage**</span></span>](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
