---
description: Il metodo UOPValid recupera un valore che indica se l'operazione utente specificata (UOP) è attualmente valida.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Metodo UOPValid (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326627"
---
# <a name="uopvalid-method"></a><span data-ttu-id="be52b-103">Metodo UOPValid</span><span class="sxs-lookup"><span data-stu-id="be52b-103">UOPValid Method</span></span>

> [!Note]  
> <span data-ttu-id="be52b-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="be52b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="be52b-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="be52b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="be52b-106">Il `UOPValid` metodo recupera un valore che indica se l'operazione utente specificata (UOP) è attualmente valida.</span><span class="sxs-lookup"><span data-stu-id="be52b-106">The `UOPValid` method retrieves a value that indicates whether the specified user operation (UOP) is currently valid.</span></span>

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a><span data-ttu-id="be52b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="be52b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be52b-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span><span class="sxs-lookup"><span data-stu-id="be52b-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span></span>
</dt> <dd>

<span data-ttu-id="be52b-109">Specifica l'operazione dell'utente (UOP) come Integer.</span><span class="sxs-lookup"><span data-stu-id="be52b-109">Specifies the user operation (UOP) as an Integer.</span></span>



| <span data-ttu-id="be52b-110">Valore</span><span class="sxs-lookup"><span data-stu-id="be52b-110">Value</span></span> | <span data-ttu-id="be52b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be52b-111">Description</span></span>                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be52b-112">0</span><span class="sxs-lookup"><span data-stu-id="be52b-112">0</span></span>     | <span data-ttu-id="be52b-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span><span class="sxs-lookup"><span data-stu-id="be52b-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span></span>                                                                                      |
| <span data-ttu-id="be52b-114">1</span><span class="sxs-lookup"><span data-stu-id="be52b-114">1</span></span>     | [<span data-ttu-id="be52b-115">**PlayChapter**</span><span class="sxs-lookup"><span data-stu-id="be52b-115">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="be52b-116">2</span><span class="sxs-lookup"><span data-stu-id="be52b-116">2</span></span>     | [<span data-ttu-id="be52b-117">**PlayTitle**</span><span class="sxs-lookup"><span data-stu-id="be52b-117">**PlayTitle**</span></span>](playtitle-method.md)                                                                                                                                                                                    |
| <span data-ttu-id="be52b-118">3</span><span class="sxs-lookup"><span data-stu-id="be52b-118">3</span></span>     | [<span data-ttu-id="be52b-119">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="be52b-119">**Stop**</span></span>](stop-method.md)                                                                                                                                                                                              |
| <span data-ttu-id="be52b-120">4</span><span class="sxs-lookup"><span data-stu-id="be52b-120">4</span></span>     | [<span data-ttu-id="be52b-121">**ReturnFromSubmenu**</span><span class="sxs-lookup"><span data-stu-id="be52b-121">**ReturnFromSubmenu**</span></span>](returnfromsubmenu-method.md)                                                                                                                                                                    |
| <span data-ttu-id="be52b-122">5</span><span class="sxs-lookup"><span data-stu-id="be52b-122">5</span></span>     | [<span data-ttu-id="be52b-123">**PlayChapter**</span><span class="sxs-lookup"><span data-stu-id="be52b-123">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="be52b-124">6</span><span class="sxs-lookup"><span data-stu-id="be52b-124">6</span></span>     | <span data-ttu-id="be52b-125">[**PlayPrevChapter**](playprevchapter-method.md), [ **ReplayChapter**](replaychapter-method.md)</span><span class="sxs-lookup"><span data-stu-id="be52b-125">[**PlayPrevChapter**](playprevchapter-method.md), [**ReplayChapter**](replaychapter-method.md)</span></span>                                                                                                                         |
| <span data-ttu-id="be52b-126">7</span><span class="sxs-lookup"><span data-stu-id="be52b-126">7</span></span>     | [<span data-ttu-id="be52b-127">**PlayNextChapter**</span><span class="sxs-lookup"><span data-stu-id="be52b-127">**PlayNextChapter**</span></span>](playnextchapter-method.md)                                                                                                                                                                        |
| <span data-ttu-id="be52b-128">8</span><span class="sxs-lookup"><span data-stu-id="be52b-128">8</span></span>     | [<span data-ttu-id="be52b-129">**PlayForwards**</span><span class="sxs-lookup"><span data-stu-id="be52b-129">**PlayForwards**</span></span>](playforwards-method.md)                                                                                                                                                                              |
| <span data-ttu-id="be52b-130">9</span><span class="sxs-lookup"><span data-stu-id="be52b-130">9</span></span>     | [<span data-ttu-id="be52b-131">**PlayBackwards**</span><span class="sxs-lookup"><span data-stu-id="be52b-131">**PlayBackwards**</span></span>](playbackwards-method.md)                                                                                                                                                                            |
| <span data-ttu-id="be52b-132">10</span><span class="sxs-lookup"><span data-stu-id="be52b-132">10</span></span>    | <span data-ttu-id="be52b-133">[**ShowMenu**](showmenu-method.md) con un valore di parametro di 2 ( \_ titolo del menu DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="be52b-133">[**ShowMenu**](showmenu-method.md) with a parameter value of 2 (DVD\_MENU\_Title)</span></span>                                                                                                                                       |
| <span data-ttu-id="be52b-134">11</span><span class="sxs-lookup"><span data-stu-id="be52b-134">11</span></span>    | <span data-ttu-id="be52b-135">[**ShowMenu**](showmenu-method.md) con un valore del parametro 3 ( \_ radice del menu DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="be52b-135">[**ShowMenu**](showmenu-method.md) with a parameter value of 3 (DVD\_MENU\_Root)</span></span>                                                                                                                                        |
| <span data-ttu-id="be52b-136">12</span><span class="sxs-lookup"><span data-stu-id="be52b-136">12</span></span>    | <span data-ttu-id="be52b-137">[**ShowMenu**](showmenu-method.md) con un valore di parametro 4 ( \_ menu di scelta rapida del menu DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="be52b-137">[**ShowMenu**](showmenu-method.md) with a parameter value of 4 (DVD\_MENU\_Subpicture)</span></span>                                                                                                                                  |
| <span data-ttu-id="be52b-138">13</span><span class="sxs-lookup"><span data-stu-id="be52b-138">13</span></span>    | <span data-ttu-id="be52b-139">[**ShowMenu**](showmenu-method.md) con valore parametro 5 ( \_ audio menu DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="be52b-139">[**ShowMenu**](showmenu-method.md) with a parameter value of 5 (DVD\_MENU\_Audio)</span></span>                                                                                                                                       |
| <span data-ttu-id="be52b-140">14</span><span class="sxs-lookup"><span data-stu-id="be52b-140">14</span></span>    | <span data-ttu-id="be52b-141">[**ShowMenu**](showmenu-method.md) con un valore di parametro di 6 ( \_ angolo del menu DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="be52b-141">[**ShowMenu**](showmenu-method.md) with a parameter value of 6 (DVD\_MENU\_Angle)</span></span>                                                                                                                                       |
| <span data-ttu-id="be52b-142">15</span><span class="sxs-lookup"><span data-stu-id="be52b-142">15</span></span>    | <span data-ttu-id="be52b-143">[**ShowMenu**](showmenu-method.md) con un valore di parametro pari a 7 \_ ( \_ capitolo menu DVD)</span><span class="sxs-lookup"><span data-stu-id="be52b-143">[**ShowMenu**](showmenu-method.md) with a parameter value of 7 (DVD\_MENU\_Chapter)</span></span>                                                                                                                                     |
| <span data-ttu-id="be52b-144">16</span><span class="sxs-lookup"><span data-stu-id="be52b-144">16</span></span>    | [<span data-ttu-id="be52b-145">**Riprendi**</span><span class="sxs-lookup"><span data-stu-id="be52b-145">**Resume**</span></span>](resume-method.md)                                                                                                                                                                                          |
| <span data-ttu-id="be52b-146">17</span><span class="sxs-lookup"><span data-stu-id="be52b-146">17</span></span>    | <span data-ttu-id="be52b-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span><span class="sxs-lookup"><span data-stu-id="be52b-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span></span> |
| <span data-ttu-id="be52b-148">18</span><span class="sxs-lookup"><span data-stu-id="be52b-148">18</span></span>    | [<span data-ttu-id="be52b-149">**StillOff**</span><span class="sxs-lookup"><span data-stu-id="be52b-149">**StillOff**</span></span>](stilloff-method.md)                                                                                                                                                                                      |
| <span data-ttu-id="be52b-150">19</span><span class="sxs-lookup"><span data-stu-id="be52b-150">19</span></span>    | [<span data-ttu-id="be52b-151">**Sospendere**</span><span class="sxs-lookup"><span data-stu-id="be52b-151">**Pause**</span></span>](pause-method.md)                                                                                                                                                                                            |
| <span data-ttu-id="be52b-152">20</span><span class="sxs-lookup"><span data-stu-id="be52b-152">20</span></span>    | [<span data-ttu-id="be52b-153">**CurrentAudioStream**</span><span class="sxs-lookup"><span data-stu-id="be52b-153">**CurrentAudioStream**</span></span>](currentaudiostream-property.md)                                                                                                                                                                |
| <span data-ttu-id="be52b-154">21</span><span class="sxs-lookup"><span data-stu-id="be52b-154">21</span></span>    | [<span data-ttu-id="be52b-155">**CurrentSubpictureStream**</span><span class="sxs-lookup"><span data-stu-id="be52b-155">**CurrentSubpictureStream**</span></span>](currentsubpicturestream-property.md)                                                                                                                                                      |
| <span data-ttu-id="be52b-156">22</span><span class="sxs-lookup"><span data-stu-id="be52b-156">22</span></span>    | <span data-ttu-id="be52b-157">[**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)</span><span class="sxs-lookup"><span data-stu-id="be52b-157">[**CurrentAngle**](currentangle-property.md), [**SelectParentalLevel**](selectparentallevel-method.md)</span></span>                                                                                                                 |
| <span data-ttu-id="be52b-158">23</span><span class="sxs-lookup"><span data-stu-id="be52b-158">23</span></span>    | [<span data-ttu-id="be52b-159">**KaraokeAudioPresentationMode**</span><span class="sxs-lookup"><span data-stu-id="be52b-159">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| <span data-ttu-id="be52b-160">24</span><span class="sxs-lookup"><span data-stu-id="be52b-160">24</span></span>    | <span data-ttu-id="be52b-161">Selezionare preferenza modalità video.</span><span class="sxs-lookup"><span data-stu-id="be52b-161">Select video mode preference.</span></span>                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be52b-162">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be52b-162">Return Value</span></span>

<span data-ttu-id="be52b-163">Restituisce un valore booleano che indica se l'operazione specificata è consentita dal controllo UOP.</span><span class="sxs-lookup"><span data-stu-id="be52b-163">Returns a Boolean value indicating whether the specified operation is permitted by UOP control.</span></span>

## <a name="requirements"></a><span data-ttu-id="be52b-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be52b-164">Requirements</span></span>



| <span data-ttu-id="be52b-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="be52b-165">Requirement</span></span> | <span data-ttu-id="be52b-166">Valore</span><span class="sxs-lookup"><span data-stu-id="be52b-166">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="be52b-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be52b-167">Header</span></span><br/> | <dl> <span data-ttu-id="be52b-168"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-168"><dt>Segment.h</dt></span></span> </dl> |



 

 




