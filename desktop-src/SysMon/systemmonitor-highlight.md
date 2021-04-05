---
title: Proprietà SystemMonitor. Highlight
description: Recupera o imposta un valore che indica se i valori dei contatori selezionati sono evidenziati nel grafico.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Evidenziare la proprietà SysMon
- Highlight Property SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà Highlight
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873845"
---
# <a name="systemmonitorhighlight-property"></a><span data-ttu-id="97e9e-106">Proprietà SystemMonitor. Highlight</span><span class="sxs-lookup"><span data-stu-id="97e9e-106">SystemMonitor.Highlight property</span></span>

<span data-ttu-id="97e9e-107">Recupera o imposta un valore che indica se i valori dei contatori selezionati sono evidenziati nel grafico.</span><span class="sxs-lookup"><span data-stu-id="97e9e-107">Retrieves or sets a value indicating whether the values of the selected counters are highlighted in the graph.</span></span>

<span data-ttu-id="97e9e-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="97e9e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="97e9e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97e9e-109">Syntax</span></span>


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a><span data-ttu-id="97e9e-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="97e9e-110">Property value</span></span>

<span data-ttu-id="97e9e-111">True indica che i valori dei contatori selezionati sono evidenziati nel grafico; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="97e9e-111">True indicates that the values of the selected counters are highlighted in the graph; otherwise, False.</span></span> <span data-ttu-id="97e9e-112">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="97e9e-112">The default value is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="97e9e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="97e9e-113">Remarks</span></span>

<span data-ttu-id="97e9e-114">Per selezionare uno o più contatori, è possibile impostare [**CounterItem. Selected**](counteritem-selected.md) su true oppure l'utente può selezionare i contatori dall'elenco dei contatori visualizzati nella legenda.</span><span class="sxs-lookup"><span data-stu-id="97e9e-114">To select one or more counters, you can set [**CounterItem.Selected**](counteritem-selected.md) to True, or the user can select the counters from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="97e9e-115">**Prima di Windows Vista:** Non è possibile selezionare i contatori a livello di codice e l'utente può selezionare un solo contatore dall'elenco dei contatori visualizzati nella legenda.</span><span class="sxs-lookup"><span data-stu-id="97e9e-115">**Prior to Windows Vista:** You cannot programmatically select counters and the user can select only one counter from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="97e9e-116">L'evidenziazione può essere nera o bianca, a seconda del valore della proprietà [**BackColor**](systemmonitor-backcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="97e9e-116">Highlighting can be black or white, depending on the value of the [**BackColor**](systemmonitor-backcolor.md) property.</span></span> <span data-ttu-id="97e9e-117">L'evidenziazione viene impostata automaticamente sul colore che fornirà un contrasto sufficiente tra il colore di evidenziazione e il colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="97e9e-117">The highlighting is automatically set to the color that will provide sufficient contrast between highlight color and the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e9e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97e9e-118">Requirements</span></span>



| <span data-ttu-id="97e9e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="97e9e-119">Requirement</span></span> | <span data-ttu-id="97e9e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="97e9e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97e9e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97e9e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="97e9e-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97e9e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="97e9e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97e9e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="97e9e-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97e9e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97e9e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="97e9e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97e9e-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="97e9e-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97e9e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97e9e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e9e-128">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="97e9e-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="97e9e-129">**CounterItem. Selected**</span><span class="sxs-lookup"><span data-stu-id="97e9e-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





