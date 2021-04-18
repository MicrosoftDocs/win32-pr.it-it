---
title: Enumerazione ResultsDisplayStyle
description: Usato da IResultsViewer ResultsStyle per impostare o determinare la modalità di visualizzazione dei risultati.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione ResultsDisplayStyle
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d564e0a7bb8a10b44e2957f26aa20a07afa535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331697"
---
# <a name="resultsdisplaystyle-enumeration"></a><span data-ttu-id="d3dca-104">Enumerazione ResultsDisplayStyle</span><span class="sxs-lookup"><span data-stu-id="d3dca-104">ResultsDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="d3dca-105">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d3dca-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d3dca-106">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d3dca-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d3dca-107">Usato da [**IResultsViewer:: ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) per impostare o determinare la modalità di visualizzazione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="d3dca-107">Used by [**IResultsViewer::ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) to set or determine how results are displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3dca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3dca-108">Syntax</span></span>


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="d3dca-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="d3dca-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d3dca-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span><span class="sxs-lookup"><span data-stu-id="d3dca-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="d3dca-111">Indica che i risultati vengono visualizzati come icone piccole.</span><span class="sxs-lookup"><span data-stu-id="d3dca-111">Indicates Results are displayed as small icons.</span></span>

</dd> <dt>

<span data-ttu-id="d3dca-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span><span class="sxs-lookup"><span data-stu-id="d3dca-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="d3dca-113">Indica che i risultati vengono visualizzati come icone grandi.</span><span class="sxs-lookup"><span data-stu-id="d3dca-113">Indicates Results are displayed as large icons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3dca-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3dca-114">Requirements</span></span>



| <span data-ttu-id="d3dca-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3dca-115">Requirement</span></span> | <span data-ttu-id="d3dca-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d3dca-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3dca-117">IDL</span><span class="sxs-lookup"><span data-stu-id="d3dca-117">IDL</span></span><br/> | <dl> <span data-ttu-id="d3dca-118"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3dca-118"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





