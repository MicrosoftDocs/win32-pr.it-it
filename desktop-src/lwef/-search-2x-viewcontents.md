---
title: Enumerazione ViewContents
description: Utilizzato dal contenuto IResultsViewer per indicare o impostare il modo in cui viene visualizzato il set restituito della query corrente.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione ViewContents
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333634"
---
# <a name="viewcontents-enumeration"></a><span data-ttu-id="4974f-104">Enumerazione ViewContents</span><span class="sxs-lookup"><span data-stu-id="4974f-104">ViewContents enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="4974f-105">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4974f-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4974f-106">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="4974f-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="4974f-107">Usato da [**IResultsViewer:: Contents**](-search-2x-iresultsviewer-contents.md) per indicare o impostare il modo in cui viene visualizzato il set restituito della query corrente.</span><span class="sxs-lookup"><span data-stu-id="4974f-107">Used by [**IResultsViewer::Contents**](-search-2x-iresultsviewer-contents.md) to indicate or set how the current query return set is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4974f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4974f-108">Syntax</span></span>


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a><span data-ttu-id="4974f-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="4974f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4974f-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span><span class="sxs-lookup"><span data-stu-id="4974f-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="4974f-111">Indica il tipo di contenuto visualizzato nella visualizzazione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="4974f-111">Indicates the type of contents being displayed in the results view.</span></span>

</dd> <dt>

<span data-ttu-id="4974f-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span><span class="sxs-lookup"><span data-stu-id="4974f-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="4974f-113">Indica che il tipo di contenuto visualizzato nella visualizzazione risultati è attualmente impostato sulla visualizzazione Shell.</span><span class="sxs-lookup"><span data-stu-id="4974f-113">Indicates the type of contents being displayed in the results view is currently set to the Shell view.</span></span>

</dd> <dt>

<span data-ttu-id="4974f-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span><span class="sxs-lookup"><span data-stu-id="4974f-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="4974f-115">Indica che il tipo di contenuto visualizzato nella visualizzazione dei risultati è attualmente impostato sulla visualizzazione del browser.</span><span class="sxs-lookup"><span data-stu-id="4974f-115">Indicates the type of contents being displayed in the results view is currently set to the browser view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4974f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4974f-116">Requirements</span></span>



| <span data-ttu-id="4974f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4974f-117">Requirement</span></span> | <span data-ttu-id="4974f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4974f-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4974f-119">IDL</span><span class="sxs-lookup"><span data-stu-id="4974f-119">IDL</span></span><br/> | <dl> <span data-ttu-id="4974f-120"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4974f-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





