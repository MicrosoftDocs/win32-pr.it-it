---
title: Proprietà CounterItem. Color
description: Recupera o imposta il colore utilizzato per rappresentare il valore del contatore.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Proprietà Color SysMon
- Proprietà Color SysMon, classe CounterItem
- Classe CounterItem SysMon, proprietà Color
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741919"
---
# <a name="counteritemcolor-property"></a><span data-ttu-id="0b6c0-106">Proprietà CounterItem. Color</span><span class="sxs-lookup"><span data-stu-id="0b6c0-106">CounterItem.Color property</span></span>

<span data-ttu-id="0b6c0-107">Recupera o imposta il colore utilizzato per rappresentare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-107">Retrieves or sets the color used to graph the counter value.</span></span>

<span data-ttu-id="0b6c0-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b6c0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b6c0-109">Syntax</span></span>


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a><span data-ttu-id="0b6c0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0b6c0-110">Property value</span></span>

<span data-ttu-id="0b6c0-111">Colore utilizzato per rappresentare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-111">Color used to graph the counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b6c0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b6c0-112">Remarks</span></span>

<span data-ttu-id="0b6c0-113">Se non si specifica il colore da usare, SYSMON seleziona i colori per i primi sedici contatori.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-113">If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="0b6c0-114">Se si specificano più di sedici contatori, SYSMON riutilizzerà gli stessi colori dei primi sedici contatori.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-114">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="0b6c0-115">Per distinguere i contatori gli uni dagli altri, SYSMON modifica lo [**stile di linea**](counteritem-linestyle.md) usato per ogni multiplo di sedici contatori fino ai primi 80 contatori.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-115">To help distinguish the counters from one another, SYSMON changes the [**line style**](counteritem-linestyle.md) used for each multiple of sixteen counters up to the first 80 counters.</span></span> <span data-ttu-id="0b6c0-116">Ad esempio, i primi sedici contatori utilizzano uno stile di linea a tinta unita, i successivi sedici utilizzano uno stile di linea tratteggiata e così via.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-116">For example, the first sixteen counters use a solid line style, the next sixteen use a dash line style, and so on.</span></span> <span data-ttu-id="0b6c0-117">SYSMON imposta quindi la [**lunghezza della riga**](counteritem-width.md) su 2 per i contatori 81-96 e su 3 per i contatori 96-112.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-117">SYSMON then sets the [**line width**](counteritem-width.md) to 2 for counters 81 - 96 and to 3 for counters 96 - 112.</span></span> <span data-ttu-id="0b6c0-118">Se la raccolta contiene più di 112 contatori, i contatori conterranno valori di colore, stile linea e larghezza duplicati.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-118">If the collection contains more than 112 counters, the counters will contain duplicate color, line style, and width values.</span></span>

<span data-ttu-id="0b6c0-119">**Prima di Windows Vista:** Se non si specifica il colore da usare, SYSMON seleziona i colori per i primi sedici contatori.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-119">**Prior to Windows Vista:** If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="0b6c0-120">Se si specificano più di sedici contatori, SYSMON riutilizzerà gli stessi colori dei primi sedici contatori.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-120">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="0b6c0-121">Per distinguere i contatori gli uni dagli altri, SYSMON aumenta la [**lunghezza della linea**](counteritem-width.md) dei primi tre contatori che ricevono la stessa assegnazione di colore.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-121">To help distinguish the counters from one another, SYSMON increases the [**line width**](counteritem-width.md) of the first three counters that receive the same color assignment.</span></span> <span data-ttu-id="0b6c0-122">Se più di tre contatori utilizzano lo stesso colore, SYSMON sceglie in modo casuale la lunghezza della riga da utilizzare per il contatore.</span><span class="sxs-lookup"><span data-stu-id="0b6c0-122">If more than three counters use the same color, SYSMON randomly chooses the line width to use for the counter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6c0-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b6c0-123">Requirements</span></span>



| <span data-ttu-id="0b6c0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b6c0-124">Requirement</span></span> | <span data-ttu-id="0b6c0-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0b6c0-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6c0-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b6c0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0b6c0-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0b6c0-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0b6c0-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b6c0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0b6c0-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0b6c0-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b6c0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0b6c0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b6c0-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="0b6c0-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b6c0-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b6c0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6c0-133">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="0b6c0-133">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





