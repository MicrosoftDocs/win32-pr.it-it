---
description: Il metodo IsAudioStreamEnabled recupera un valore che indica se il flusso audio specificato è abilitato nel titolo corrente.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Metodo IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520394"
---
# <a name="isaudiostreamenabled-method"></a><span data-ttu-id="4e3c5-103">Metodo IsAudioStreamEnabled</span><span class="sxs-lookup"><span data-stu-id="4e3c5-103">IsAudioStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="4e3c5-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4e3c5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4e3c5-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="4e3c5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4e3c5-106">Il `IsAudioStreamEnabled` metodo recupera un valore che indica se il flusso audio specificato è abilitato nel titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="4e3c5-106">The `IsAudioStreamEnabled` method retrieves a value indicating whether the specified audio stream is enabled in the current title.</span></span>

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="4e3c5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e3c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e3c5-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="4e3c5-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="4e3c5-109">Specifica il flusso audio come valore intero compreso tra 0 e 7.</span><span class="sxs-lookup"><span data-stu-id="4e3c5-109">Specifies the audio stream as an Integer value from 0 through 7.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e3c5-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e3c5-110">Return Value</span></span>

<span data-ttu-id="4e3c5-111">Restituisce un valore booleano che indica se il flusso audio specificato è disponibile per il titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="4e3c5-111">Returns a Boolean value indicating whether the specified audio stream is available for the current title.</span></span> <span data-ttu-id="4e3c5-112">True indica che è disponibile.</span><span class="sxs-lookup"><span data-stu-id="4e3c5-112">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e3c5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e3c5-113">Remarks</span></span>

<span data-ttu-id="4e3c5-114">Sebbene un disco possa contenere fino a otto flussi audio indipendenti, ogni flusso non è necessariamente disponibile per ogni titolo.</span><span class="sxs-lookup"><span data-stu-id="4e3c5-114">Although a disc can contain up to eight independent audio streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="4e3c5-115">Un titolo di film principale, ad esempio, potrebbe avere tre flussi audio per l'inglese, spagnolo e giapponese, ma il titolo "attractions" potrebbe avere un solo flusso audio in inglese.</span><span class="sxs-lookup"><span data-stu-id="4e3c5-115">For example, a main movie title might have three audio streams for English, Spanish, and Japanese, but the "Coming Attractions" title might have only one audio stream in English.</span></span> <span data-ttu-id="4e3c5-116">Verificare sempre che un flusso sia disponibile per un titolo prima di impostare la proprietà [**CurrentAudioStream**](currentaudiostream-property.md) .</span><span class="sxs-lookup"><span data-stu-id="4e3c5-116">Always verify that a stream is available for a title before setting the [**CurrentAudioStream**](currentaudiostream-property.md) property.</span></span>

 

 



