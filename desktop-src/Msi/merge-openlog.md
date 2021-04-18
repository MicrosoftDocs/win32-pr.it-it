---
description: Il Metodo OpenLog dell'oggetto merge apre un file di log che riceve i messaggi di stato e di errore. Se il file di log esiste già, il programma di installazione aggiunge nuovi messaggi. Se il file di log non esiste, il programma di installazione crea un file di log.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Metodo merge. OpenLog (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333980"
---
# <a name="mergeopenlog-method"></a><span data-ttu-id="a8911-105">Merge. OpenLog, metodo</span><span class="sxs-lookup"><span data-stu-id="a8911-105">Merge.OpenLog method</span></span>

<span data-ttu-id="a8911-106">Il metodo **OpenLog** dell'oggetto [**merge**](merge-object.md) apre un file di log che riceve i messaggi di stato e di errore.</span><span class="sxs-lookup"><span data-stu-id="a8911-106">The **OpenLog** method of the [**Merge**](merge-object.md) object opens a log file that receives progress and error messages.</span></span> <span data-ttu-id="a8911-107">Se il file di log esiste già, il programma di installazione aggiunge nuovi messaggi.</span><span class="sxs-lookup"><span data-stu-id="a8911-107">If the log file already exists, the installer appends new messages.</span></span> <span data-ttu-id="a8911-108">Se il file di log non esiste, il programma di installazione crea un file di log.</span><span class="sxs-lookup"><span data-stu-id="a8911-108">If the log file does not exist, the installer creates a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8911-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8911-109">Syntax</span></span>


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a><span data-ttu-id="a8911-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8911-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8911-111">*Filename*</span><span class="sxs-lookup"><span data-stu-id="a8911-111">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="a8911-112">Nome file completo che punta a un file da aprire o creare.</span><span class="sxs-lookup"><span data-stu-id="a8911-112">Fully qualified file name pointing to a file to open or create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8911-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8911-113">Return value</span></span>

<span data-ttu-id="a8911-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a8911-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8911-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8911-115">Remarks</span></span>

<span data-ttu-id="a8911-116">I client possono inviare i propri messaggi a questo file di log tramite il metodo [**log**](merge-log.md) .</span><span class="sxs-lookup"><span data-stu-id="a8911-116">Clients may send their own messages to this log file through the [**Log**](merge-log.md) method.</span></span>

### <a name="c"></a><span data-ttu-id="a8911-117">C++</span><span class="sxs-lookup"><span data-stu-id="a8911-117">C++</span></span>

<span data-ttu-id="a8911-118">Vedere funzione [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) .</span><span class="sxs-lookup"><span data-stu-id="a8911-118">See [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8911-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8911-119">Requirements</span></span>



| <span data-ttu-id="a8911-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8911-120">Requirement</span></span> | <span data-ttu-id="a8911-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a8911-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8911-122">Versione</span><span class="sxs-lookup"><span data-stu-id="a8911-122">Version</span></span><br/> | <span data-ttu-id="a8911-123">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a8911-123">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="a8911-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8911-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a8911-125"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8911-125"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8911-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a8911-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="a8911-127"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8911-127"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
