---
description: Il metodo IsSubpictureStreamEnabled recupera un valore che indica se il flusso di sottoimmagine specificato è abilitato nel titolo corrente.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Metodo IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876869"
---
# <a name="issubpicturestreamenabled-method"></a><span data-ttu-id="f9ef8-103">Metodo IsSubpictureStreamEnabled</span><span class="sxs-lookup"><span data-stu-id="f9ef8-103">IsSubpictureStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="f9ef8-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f9ef8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f9ef8-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="f9ef8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f9ef8-106">Il `IsSubpictureStreamEnabled` metodo recupera un valore che indica se il flusso di sottoimmagine specificato è abilitato nel titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="f9ef8-106">The `IsSubpictureStreamEnabled` method retrieves a value indicating whether the specified subpicture stream is enabled in the current title.</span></span>

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="f9ef8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9ef8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9ef8-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="f9ef8-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="f9ef8-109">Specifica il flusso di sottoimmagine come intero.</span><span class="sxs-lookup"><span data-stu-id="f9ef8-109">Specifies the subpicture stream as an Integer.</span></span>



| <span data-ttu-id="f9ef8-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ef8-110">Value</span></span>   | <span data-ttu-id="f9ef8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9ef8-111">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="f9ef8-112">da 0 a 31</span><span class="sxs-lookup"><span data-stu-id="f9ef8-112">0 to 31</span></span> | <span data-ttu-id="f9ef8-113">flusso di sottoimmagine</span><span class="sxs-lookup"><span data-stu-id="f9ef8-113">subpicture stream</span></span>        |
| <span data-ttu-id="f9ef8-114">63</span><span class="sxs-lookup"><span data-stu-id="f9ef8-114">63</span></span>      | <span data-ttu-id="f9ef8-115">flusso a bitrate ridotto disattivato</span><span class="sxs-lookup"><span data-stu-id="f9ef8-115">muted low-bitrate stream</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9ef8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9ef8-116">Return Value</span></span>

<span data-ttu-id="f9ef8-117">Restituisce un valore booleano che indica se il flusso audio specificato è disponibile nel titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="f9ef8-117">Returns a Boolean value indicating whether the specified audio stream is available in the current title.</span></span> <span data-ttu-id="f9ef8-118">True indica che è disponibile.</span><span class="sxs-lookup"><span data-stu-id="f9ef8-118">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9ef8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9ef8-119">Remarks</span></span>

<span data-ttu-id="f9ef8-120">Sebbene un disco possa contenere fino a 32 di flussi di immagini, ogni flusso non è necessariamente disponibile per ogni titolo.</span><span class="sxs-lookup"><span data-stu-id="f9ef8-120">Although a disc can contain up to 32 subpicture streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="f9ef8-121">Verificare sempre che un flusso sia disponibile per un titolo prima di impostare la proprietà [**CurrentSubpictureStream**](currentsubpicturestream-property.md) .</span><span class="sxs-lookup"><span data-stu-id="f9ef8-121">Always verify that a stream is available for a title before setting the [**CurrentSubpictureStream**](currentsubpicturestream-property.md) property.</span></span>

 

 



