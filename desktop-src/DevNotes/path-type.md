---
description: Rappresenta il tipo di percorso usato come argomento.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: Enumerazione PATH_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522953"
---
# <a name="path_type-enumeration"></a><span data-ttu-id="ad396-103">Enumerazione del tipo di percorso \_</span><span class="sxs-lookup"><span data-stu-id="ad396-103">PATH\_TYPE enumeration</span></span>

<span data-ttu-id="ad396-104">Rappresenta il tipo di percorso usato come argomento.</span><span class="sxs-lookup"><span data-stu-id="ad396-104">Represents the type of path being used as an argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad396-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad396-105">Syntax</span></span>


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ad396-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="ad396-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ad396-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**\_percorso DOS**</span><span class="sxs-lookup"><span data-stu-id="ad396-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**DOS\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="ad396-108">Percorso standard.</span><span class="sxs-lookup"><span data-stu-id="ad396-108">Standard path.</span></span>

</dd> <dt>

<span data-ttu-id="ad396-109"><span id="NT_PATH"></span><span id="nt_path"></span>**\_percorso NT**</span><span class="sxs-lookup"><span data-stu-id="ad396-109"><span id="NT_PATH"></span><span id="nt_path"></span>**NT\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="ad396-110">Percorso interno.</span><span class="sxs-lookup"><span data-stu-id="ad396-110">Internal path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad396-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad396-111">Requirements</span></span>



| <span data-ttu-id="ad396-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad396-112">Requirement</span></span> | <span data-ttu-id="ad396-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ad396-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad396-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad396-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ad396-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad396-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ad396-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad396-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ad396-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ad396-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad396-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad396-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad396-119">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="ad396-119">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> <dt>

[<span data-ttu-id="ad396-120">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="ad396-120">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




