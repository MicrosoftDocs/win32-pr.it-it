---
title: Struttura _VIDEOINFOHEADER
description: La \_ struttura VIDEOINFOHEADER contiene informazioni su un flusso video e include una \_ struttura BITMAPINFOHEADER che definisce il formato di un singolo frame.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- Struttura di _VIDEOINFOHEADER Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324227"
---
# <a name="_videoinfoheader-structure"></a><span data-ttu-id="42b7a-104">\_Struttura VIDEOINFOHEADER</span><span class="sxs-lookup"><span data-stu-id="42b7a-104">\_VIDEOINFOHEADER structure</span></span>

<span data-ttu-id="42b7a-105">La struttura **\_ VIDEOINFOHEADER** contiene informazioni su un flusso video e include una struttura **\_ BITMAPINFOHEADER** che definisce il formato di un singolo frame.</span><span class="sxs-lookup"><span data-stu-id="42b7a-105">The **\_VIDEOINFOHEADER** structure contains information about a video stream and includes a **\_BITMAPINFOHEADER** structure that defines the format of an individual frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b7a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42b7a-106">Syntax</span></span>


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="42b7a-107">Members</span><span class="sxs-lookup"><span data-stu-id="42b7a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="42b7a-108">**rcSource**</span><span class="sxs-lookup"><span data-stu-id="42b7a-108">**rcSource**</span></span>
</dt> <dd>

<span data-ttu-id="42b7a-109">Struttura **Rect** che specifica la finestra del video di origine.</span><span class="sxs-lookup"><span data-stu-id="42b7a-109">**RECT** structure that specifies the source video window.</span></span>

</dd> <dt>

<span data-ttu-id="42b7a-110">**rcTarget**</span><span class="sxs-lookup"><span data-stu-id="42b7a-110">**rcTarget**</span></span>
</dt> <dd>

<span data-ttu-id="42b7a-111">Struttura **Rect** che specifica la finestra video di destinazione.</span><span class="sxs-lookup"><span data-stu-id="42b7a-111">**RECT** structure that specifies the destination video window.</span></span>

</dd> <dt>

<span data-ttu-id="42b7a-112">**dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="42b7a-112">**dwBitRate**</span></span>
</dt> <dd>

<span data-ttu-id="42b7a-113">Valore **DWORD** che specifica la velocità dati approssimativa del flusso video, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="42b7a-113">**DWORD** value that specifies the video stream's approximate data rate, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="42b7a-114">**dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="42b7a-114">**dwBitErrorRate**</span></span>
</dt> <dd>

<span data-ttu-id="42b7a-115">Valore **DWORD** che specifica la frequenza di errore dei dati del flusso video, in errori di bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="42b7a-115">**DWORD** value that specifies the video stream's data error rate, in bit errors per second.</span></span>

</dd> <dt>

<span data-ttu-id="42b7a-116">**AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="42b7a-116">**AvgTimePerFrame**</span></span>
</dt> <dd>

<span data-ttu-id="42b7a-117">Informazioni di **riferimento \_** Valore di ora che specifica il tempo medio di visualizzazione del fotogramma video, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="42b7a-117">**REFERENCE\_TIME** value that specifies the video frame's average display time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="42b7a-118">**bmiHeader**</span><span class="sxs-lookup"><span data-stu-id="42b7a-118">**bmiHeader**</span></span>
</dt> <dd>

<span data-ttu-id="42b7a-119">Struttura **\_ BITMAPINFOHEADER** Win32 che contiene le informazioni relative al colore e alla dimensione per la bitmap dell'immagine video.</span><span class="sxs-lookup"><span data-stu-id="42b7a-119">Win32 **\_BITMAPINFOHEADER** structure that contains color and dimension information for the video image bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42b7a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42b7a-120">Requirements</span></span>



| <span data-ttu-id="42b7a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="42b7a-121">Requirement</span></span> | <span data-ttu-id="42b7a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="42b7a-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="42b7a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42b7a-123">Header</span></span><br/> | <dl> <span data-ttu-id="42b7a-124"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42b7a-124"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42b7a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42b7a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b7a-126">**\_BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="42b7a-126">**\_BITMAPINFOHEADER**</span></span>](-bitmapinfoheader.md)
</dt> <dt>

[<span data-ttu-id="42b7a-127">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="42b7a-127">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





