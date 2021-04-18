---
description: Operatori di assegnazione di moltiplicazione.
ms.assetid: 4d25cef1-8b39-42db-80df-c749940feb0b
title: operatori operator * =
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 486e85ae8f541c802e50c38d29cd16beb746b587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309186"
---
# <a name="operator--operators"></a><span data-ttu-id="69b58-103">Operators \* = operatori</span><span class="sxs-lookup"><span data-stu-id="69b58-103">operator \*= operators</span></span>

<span data-ttu-id="69b58-104">Operatori di assegnazione di moltiplicazione</span><span class="sxs-lookup"><span data-stu-id="69b58-104">Multiplication assignment operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="69b58-105">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="69b58-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="69b58-106">Operatore</span><span class="sxs-lookup"><span data-stu-id="69b58-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="69b58-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69b58-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="69b58-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR:: operator \* = (XMVECTOR&, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="69b58-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="69b58-109">Consente di moltiplicare un' <code>XMVECTOR</code> istanza per un valore a virgola mobile e restituisce un riferimento all'istanza aggiornata.</span><span class="sxs-lookup"><span data-stu-id="69b58-109">Multiplies an <code>XMVECTOR</code> instance by a floating point value and returns a reference to the updated instance.</span></span> <br/> <span data-ttu-id="69b58-110"><code>operator \*=</code>Moltiplica ogni componente dell'istanza corrente del <a href="xmvector-data-type.md"><strong>tipo di dati XMVECTOR</strong></a> in base a un valore a virgola mobile specificato, restituendo un riferimento all'istanza corrente aggiornata.</span><span class="sxs-lookup"><span data-stu-id="69b58-110">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a specified floating point value, returning a reference to the updated current instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="69b58-111">Questo operatore è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="69b58-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="69b58-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR:: operator \* = (XMVECTOR&, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="69b58-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="69b58-113">Moltiplica un' <code>XMVECTOR</code> istanza per una seconda istanza, restituendo un riferimento all'istanza iniziale aggiornata.</span><span class="sxs-lookup"><span data-stu-id="69b58-113">Multiplies one <code>XMVECTOR</code> instance by a second instance, returning a reference to the updated initial instance.</span></span> <br/> <span data-ttu-id="69b58-114"><code>operator \*=</code>Moltiplica ogni componente dell'istanza corrente del <a href="xmvector-data-type.md"><strong>tipo di dati XMVECTOR</strong></a> per il componente corrispondente in una seconda istanza specificata di <code>XMVECTOR</code> , restituendo un riferimento all'istanza iniziale aggiornata.</span><span class="sxs-lookup"><span data-stu-id="69b58-114">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second specified instance of <code>XMVECTOR</code>, returning a reference to the updated initial instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="69b58-115">Questo operatore è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="69b58-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="69b58-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69b58-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b58-117">Operatori XMVECTOR</span><span class="sxs-lookup"><span data-stu-id="69b58-117">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="69b58-118">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="69b58-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="69b58-119">**Tipo di dati XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="69b58-119">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
