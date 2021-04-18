---
description: Recupera la versione del software per questo flusso.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: Metodo CPersistStream. GetSoftwareVersion (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0954e9a113342217dd389c64ec4fc6c04a6f767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328929"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a><span data-ttu-id="78332-103">CPersistStream. GetSoftwareVersion, metodo</span><span class="sxs-lookup"><span data-stu-id="78332-103">CPersistStream.GetSoftwareVersion method</span></span>

<span data-ttu-id="78332-104">Recupera la versione del software per questo flusso.</span><span class="sxs-lookup"><span data-stu-id="78332-104">Retrieves the software version for this stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="78332-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78332-105">Syntax</span></span>


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a><span data-ttu-id="78332-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="78332-106">Parameters</span></span>

<span data-ttu-id="78332-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="78332-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="78332-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78332-108">Return value</span></span>

<span data-ttu-id="78332-109">Restituisce un **valore DWORD** contenente il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="78332-109">Returns a **DWORD** containing the version number.</span></span> <span data-ttu-id="78332-110">Ogni volta che il formato del flusso viene modificato, è necessario modificare questa funzione per restituire un numero maggiore di quello precedente.</span><span class="sxs-lookup"><span data-stu-id="78332-110">Each time the format of the stream is changed, this function should be altered to return a larger number than before.</span></span>

## <a name="requirements"></a><span data-ttu-id="78332-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78332-111">Requirements</span></span>



| <span data-ttu-id="78332-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="78332-112">Requirement</span></span> | <span data-ttu-id="78332-113">Valore</span><span class="sxs-lookup"><span data-stu-id="78332-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78332-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78332-114">Header</span></span><br/>  | <dl> <span data-ttu-id="78332-115"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78332-115"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="78332-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="78332-116">Library</span></span><br/> | <dl> <span data-ttu-id="78332-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="78332-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78332-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78332-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78332-119">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="78332-119">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




