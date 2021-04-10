---
description: Operatori di moltiplicazione.
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: operatori operator *
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15cdb9d189d110621461c1623b4fd20eaa9e7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130582"
---
# <a name="operator--operators"></a><span data-ttu-id="1a5c3-103">\*operatori operator</span><span class="sxs-lookup"><span data-stu-id="1a5c3-103">operator \* operators</span></span>

<span data-ttu-id="1a5c3-104">Operatori di moltiplicazione</span><span class="sxs-lookup"><span data-stu-id="1a5c3-104">Multiplication operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="1a5c3-105">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="1a5c3-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1a5c3-106">Operatore</span><span class="sxs-lookup"><span data-stu-id="1a5c3-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1a5c3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a5c3-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c3-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR:: operator \* (float, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c3-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR::operator \* (float,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c3-109">Moltiplicare un valore a virgola mobile in base a un'istanza di <code>XMVECTOR</code> , restituendo il risultato a una nuova istanza di <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="1a5c3-109">Multiply a floating point value by an instance of <code>XMVECTOR</code>, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="1a5c3-110"><code>operator \*</code>Moltiplica un valore a virgola mobile rispetto a ogni componente di un'istanza del <a href="xmvector-data-type.md"><strong>tipo di dati XMVECTOR</strong></a>, restituendo una nuova <code>XMVECTOR</code> istanza i cui componenti contengono il risultato.</span><span class="sxs-lookup"><span data-stu-id="1a5c3-110">The <code>operator \*</code> multiplies a floating point value against each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a>, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1a5c3-111">Questo operatore è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="1a5c3-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c3-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR:: operator \* (XMVECTOR, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c3-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c3-113">Moltiplicare un'istanza di <code>XMVECTOR</code> per un valore a virgola mobile, restituendo il risultato a una nuova istanza di <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="1a5c3-113">Multiply an instance of <code>XMVECTOR</code> by a floating point value, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="1a5c3-114"><code>operator \*</code>Moltiplica ogni componente di un'istanza del tipo di <a href="xmvector-data-type.md"><strong>dati XMVECTOR</strong></a> in base a un valore a virgola mobile, restituendo una nuova <code>XMVECTOR</code> istanza i cui componenti contengono il risultato.</span><span class="sxs-lookup"><span data-stu-id="1a5c3-114">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a floating point value, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1a5c3-115">Questo operatore è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="1a5c3-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c3-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR:: operator \* (XMVECTOR, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c3-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c3-117">Moltiplica un'istanza di <code>XMVECTOR</code> per una seconda istanza, restituendo il risultato in una terza istanza.</span><span class="sxs-lookup"><span data-stu-id="1a5c3-117">Multiplies one instance of <code>XMVECTOR</code> by a second instance, returning the result in a third instance.</span></span> <br/> <span data-ttu-id="1a5c3-118"><code>operator \*</code>Moltiplica ogni componente di un'istanza del tipo di <a href="xmvector-data-type.md"><strong>dati XMVECTOR</strong></a> in base al componente corrispondente in una seconda istanza di <code>XMVECTOR</code> , restituendo una nuova <code>XMVECTOR</code> istanza di contenente il risultato.</span><span class="sxs-lookup"><span data-stu-id="1a5c3-118">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second instance of <code>XMVECTOR</code>, returning a new <code>XMVECTOR</code> instance containing the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1a5c3-119">Questo operatore è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="1a5c3-119">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="1a5c3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a5c3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a5c3-121">Operatori XMVECTOR</span><span class="sxs-lookup"><span data-stu-id="1a5c3-121">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="1a5c3-122">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1a5c3-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a5c3-123">**Tipo di dati XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="1a5c3-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
