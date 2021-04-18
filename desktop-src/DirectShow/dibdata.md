---
description: La struttura DIBDATA contiene informazioni su una bitmap indipendente dal dispositivo (DIB) GDI.
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Struttura DIBDATA (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330659"
---
# <a name="dibdata-structure"></a><span data-ttu-id="5060f-103">Struttura DIBDATA</span><span class="sxs-lookup"><span data-stu-id="5060f-103">DIBDATA structure</span></span>

<span data-ttu-id="5060f-104">La `DIBDATA` struttura contiene informazioni su una bitmap indipendente dal dispositivo (DIB) GDI.</span><span class="sxs-lookup"><span data-stu-id="5060f-104">The `DIBDATA` structure contains information about a GDI device-independent bitmap (DIB).</span></span>

## <a name="syntax"></a><span data-ttu-id="5060f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5060f-105">Syntax</span></span>


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a><span data-ttu-id="5060f-106">Members</span><span class="sxs-lookup"><span data-stu-id="5060f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5060f-107">**PaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="5060f-107">**PaletteVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-108">Questo membro deve essere incrementato ogni volta che la tavolozza viene modificata.</span><span class="sxs-lookup"><span data-stu-id="5060f-108">This member should be incremented whenever the palette changes.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-109">**DibSection**</span><span class="sxs-lookup"><span data-stu-id="5060f-109">**DibSection**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-110">Struttura **DIBSection** che contiene informazioni sulla DIB.</span><span class="sxs-lookup"><span data-stu-id="5060f-110">**DIBSECTION** structure that contains information about the DIB.</span></span> <span data-ttu-id="5060f-111">Per informazioni dettagliate, vedere la documentazione di GDI.</span><span class="sxs-lookup"><span data-stu-id="5060f-111">See the GDI documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-112">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="5060f-112">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-113">Handle per la bitmap.</span><span class="sxs-lookup"><span data-stu-id="5060f-113">Handle to the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-114">**hMapping**</span><span class="sxs-lookup"><span data-stu-id="5060f-114">**hMapping**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-115">Handle per un oggetto mapping di file utilizzato per condividere la memoria tra GDI e un oggetto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="5060f-115">Handle to a file-mapping object that is used to share memory between GDI and a [**CImageSample**](cimagesample.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-116">**pBase**</span><span class="sxs-lookup"><span data-stu-id="5060f-116">**pBase**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-117">Indirizzo della bitmap.</span><span class="sxs-lookup"><span data-stu-id="5060f-117">Address of the bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5060f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5060f-118">Requirements</span></span>



| <span data-ttu-id="5060f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5060f-119">Requirement</span></span> | <span data-ttu-id="5060f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5060f-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5060f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5060f-121">Header</span></span><br/> | <dl> <span data-ttu-id="5060f-122"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5060f-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl> |



 

 




