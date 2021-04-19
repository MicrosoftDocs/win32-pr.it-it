---
title: Enumerazione HeaderDisplayStyle
description: Usato da IResultsViewer HeaderStyle per impostare o restituire lo stile dell'intestazione corrente.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione HeaderDisplayStyle
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327864"
---
# <a name="headerdisplaystyle-enumeration"></a><span data-ttu-id="7cd79-104">Enumerazione HeaderDisplayStyle</span><span class="sxs-lookup"><span data-stu-id="7cd79-104">HeaderDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="7cd79-105">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7cd79-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7cd79-106">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="7cd79-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7cd79-107">Usato da [**IResultsViewer:: HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) per impostare o restituire lo stile dell'intestazione corrente.</span><span class="sxs-lookup"><span data-stu-id="7cd79-107">Used by [**IResultsViewer::HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) to set or return the current header style.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd79-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cd79-108">Syntax</span></span>


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="7cd79-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="7cd79-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7cd79-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span><span class="sxs-lookup"><span data-stu-id="7cd79-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span></span>
</dt> <dd>

<span data-ttu-id="7cd79-111">Indica o imposta l'utilizzo di intestazioni complete.</span><span class="sxs-lookup"><span data-stu-id="7cd79-111">Indicates or sets the use of full headers.</span></span>

</dd> <dt>

<span data-ttu-id="7cd79-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span><span class="sxs-lookup"><span data-stu-id="7cd79-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span></span>
</dt> <dd>

<span data-ttu-id="7cd79-113">Indica o imposta l'utilizzo di intestazioni Compact.</span><span class="sxs-lookup"><span data-stu-id="7cd79-113">Indicates or sets the use of compact headers.</span></span>

</dd> <dt>

<span data-ttu-id="7cd79-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**</span><span class="sxs-lookup"><span data-stu-id="7cd79-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**</span></span>
</dt> <dd>

<span data-ttu-id="7cd79-115">Indica o imposta l'utilizzo di nessuna intestazione.</span><span class="sxs-lookup"><span data-stu-id="7cd79-115">Indicates or sets the use of no headers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7cd79-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cd79-116">Requirements</span></span>



| <span data-ttu-id="7cd79-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cd79-117">Requirement</span></span> | <span data-ttu-id="7cd79-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7cd79-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd79-119">IDL</span><span class="sxs-lookup"><span data-stu-id="7cd79-119">IDL</span></span><br/> | <dl> <span data-ttu-id="7cd79-120"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7cd79-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





