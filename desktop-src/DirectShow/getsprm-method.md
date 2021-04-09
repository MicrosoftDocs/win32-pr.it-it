---
description: Il metodo GetSPRM Recupera il registro dei parametri di sistema specificato.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Metodo GetSPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965474"
---
# <a name="getsprm-method"></a><span data-ttu-id="aac59-103">Metodo GetSPRM</span><span class="sxs-lookup"><span data-stu-id="aac59-103">GetSPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="aac59-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="aac59-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="aac59-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="aac59-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="aac59-106">Il `GetSPRM` metodo recupera il registro dei parametri di sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="aac59-106">The `GetSPRM` method retrieves the specified system parameter register.</span></span>

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="aac59-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="aac59-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aac59-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="aac59-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="aac59-109">Specifica il registro di cui si desidera recuperare il valore come Integer.</span><span class="sxs-lookup"><span data-stu-id="aac59-109">Specifies the register whose value you want to retrieve as an Integer.</span></span> <span data-ttu-id="aac59-110">Il valore integer deve essere compreso tra 0 e 23.</span><span class="sxs-lookup"><span data-stu-id="aac59-110">The Integer must range from 0 through 23.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aac59-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aac59-111">Return Value</span></span>

<span data-ttu-id="aac59-112">Restituisce un valore intero che rappresenta il contenuto del registro specificato.</span><span class="sxs-lookup"><span data-stu-id="aac59-112">Returns an integer value representing the contents of the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="aac59-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="aac59-113">Remarks</span></span>

<span data-ttu-id="aac59-114">Il disco controlla i registri dei parametri di sistema (SPRMs).</span><span class="sxs-lookup"><span data-stu-id="aac59-114">The disc controls system parameter registers (SPRMs).</span></span> <span data-ttu-id="aac59-115">Un'applicazione del lettore non deve accedere a questi registri per le funzionalità di navigazione standard.</span><span class="sxs-lookup"><span data-stu-id="aac59-115">A player application doesn't need to access these registers for any standard navigation functionality.</span></span> <span data-ttu-id="aac59-116">SPRMs rappresenta lo stato del lettore.</span><span class="sxs-lookup"><span data-stu-id="aac59-116">SPRMs represent the status of the player.</span></span> <span data-ttu-id="aac59-117">Ognuno ha un significato, impostato in base alle preferenze dell'utente, ai comandi del disco e ad altre occorrenze che un'applicazione non ha controllo diretto.</span><span class="sxs-lookup"><span data-stu-id="aac59-117">Each one has a meaning, set by user preferences, disc commands, and other occurrences that an application has no direct control over.</span></span> <span data-ttu-id="aac59-118">Un'applicazione può leggere questi registri ma non scriverli.</span><span class="sxs-lookup"><span data-stu-id="aac59-118">An application can read these registers but cannot write to them.</span></span> <span data-ttu-id="aac59-119">Per utilizzare i registri in modo efficace, probabilmente sarà necessaria una conoscenza più approfondita dei comandi di spostamento del DVD rispetto a quanto specificato in questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="aac59-119">To use these registers effectively, you will probably need a more detailed knowledge of the DVD navigation commands than is provided in this documentation.</span></span> <span data-ttu-id="aac59-120">Nella tabella seguente viene illustrato il contenuto di ogni registro.</span><span class="sxs-lookup"><span data-stu-id="aac59-120">The following table shows the contents of each register.</span></span> <span data-ttu-id="aac59-121">Per informazioni più dettagliate sul contenuto del registro, vedere [ **IDvdInfo2:: GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span><span class="sxs-lookup"><span data-stu-id="aac59-121">For more detailed information on the register contents, see [**IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span></span>



| <span data-ttu-id="aac59-122">Registrazione</span><span class="sxs-lookup"><span data-stu-id="aac59-122">Register</span></span> | <span data-ttu-id="aac59-123">Contenuto</span><span class="sxs-lookup"><span data-stu-id="aac59-123">Contents</span></span>                        |
|----------|---------------------------------|
| <span data-ttu-id="aac59-124">0</span><span class="sxs-lookup"><span data-stu-id="aac59-124">0</span></span>        | <span data-ttu-id="aac59-125">Codice lingua menu</span><span class="sxs-lookup"><span data-stu-id="aac59-125">Menu language code</span></span>              |
| <span data-ttu-id="aac59-126">1</span><span class="sxs-lookup"><span data-stu-id="aac59-126">1</span></span>        | <span data-ttu-id="aac59-127">Numero flusso audio</span><span class="sxs-lookup"><span data-stu-id="aac59-127">Audio stream number</span></span>             |
| <span data-ttu-id="aac59-128">2</span><span class="sxs-lookup"><span data-stu-id="aac59-128">2</span></span>        | <span data-ttu-id="aac59-129">Numero di flusso di immagini subimmagine</span><span class="sxs-lookup"><span data-stu-id="aac59-129">Subpicture stream number</span></span>        |
| <span data-ttu-id="aac59-130">3</span><span class="sxs-lookup"><span data-stu-id="aac59-130">3</span></span>        | <span data-ttu-id="aac59-131">Numero angolo corrente</span><span class="sxs-lookup"><span data-stu-id="aac59-131">Current angle number</span></span>            |
| <span data-ttu-id="aac59-132">4</span><span class="sxs-lookup"><span data-stu-id="aac59-132">4</span></span>        | <span data-ttu-id="aac59-133">Numero del titolo corrente</span><span class="sxs-lookup"><span data-stu-id="aac59-133">Current title number</span></span>            |
| <span data-ttu-id="aac59-134">5</span><span class="sxs-lookup"><span data-stu-id="aac59-134">5</span></span>        | <span data-ttu-id="aac59-135">Numero titolo</span><span class="sxs-lookup"><span data-stu-id="aac59-135">Title number</span></span>                    |
| <span data-ttu-id="aac59-136">6</span><span class="sxs-lookup"><span data-stu-id="aac59-136">6</span></span>        | <span data-ttu-id="aac59-137">Numero PGC</span><span class="sxs-lookup"><span data-stu-id="aac59-137">PGC number</span></span>                      |
| <span data-ttu-id="aac59-138">7</span><span class="sxs-lookup"><span data-stu-id="aac59-138">7</span></span>        | <span data-ttu-id="aac59-139">Numero del capitolo corrente (PTT)</span><span class="sxs-lookup"><span data-stu-id="aac59-139">Current chapter number (PTT)</span></span>    |
| <span data-ttu-id="aac59-140">8</span><span class="sxs-lookup"><span data-stu-id="aac59-140">8</span></span>        | <span data-ttu-id="aac59-141">Numero pulsante evidenziato</span><span class="sxs-lookup"><span data-stu-id="aac59-141">Highlighted button number</span></span>       |
| <span data-ttu-id="aac59-142">9</span><span class="sxs-lookup"><span data-stu-id="aac59-142">9</span></span>        | <span data-ttu-id="aac59-143">Timer di spostamento</span><span class="sxs-lookup"><span data-stu-id="aac59-143">Navigation timer</span></span>                |
| <span data-ttu-id="aac59-144">10</span><span class="sxs-lookup"><span data-stu-id="aac59-144">10</span></span>       | <span data-ttu-id="aac59-145">Salto PGC per NAV.</span><span class="sxs-lookup"><span data-stu-id="aac59-145">PGC jump for nav.</span></span> <span data-ttu-id="aac59-146">timer</span><span class="sxs-lookup"><span data-stu-id="aac59-146">timer</span></span>         |
| <span data-ttu-id="aac59-147">11</span><span class="sxs-lookup"><span data-stu-id="aac59-147">11</span></span>       | <span data-ttu-id="aac59-148">Modalità presentazione audio karaoke</span><span class="sxs-lookup"><span data-stu-id="aac59-148">Karaoke audio presentation mode</span></span> |
| <span data-ttu-id="aac59-149">12</span><span class="sxs-lookup"><span data-stu-id="aac59-149">12</span></span>       | <span data-ttu-id="aac59-150">Codice di paese/area geografica PML</span><span class="sxs-lookup"><span data-stu-id="aac59-150">PML country/region code</span></span>         |
| <span data-ttu-id="aac59-151">13</span><span class="sxs-lookup"><span data-stu-id="aac59-151">13</span></span>       | <span data-ttu-id="aac59-152">PML</span><span class="sxs-lookup"><span data-stu-id="aac59-152">PML</span></span>                             |
| <span data-ttu-id="aac59-153">14</span><span class="sxs-lookup"><span data-stu-id="aac59-153">14</span></span>       | <span data-ttu-id="aac59-154">Impostazione video</span><span class="sxs-lookup"><span data-stu-id="aac59-154">Video setting</span></span>                   |
| <span data-ttu-id="aac59-155">15</span><span class="sxs-lookup"><span data-stu-id="aac59-155">15</span></span>       | <span data-ttu-id="aac59-156">Funzionalità audio</span><span class="sxs-lookup"><span data-stu-id="aac59-156">Audio capability</span></span>                |
| <span data-ttu-id="aac59-157">16</span><span class="sxs-lookup"><span data-stu-id="aac59-157">16</span></span>       | <span data-ttu-id="aac59-158">Lingua audio</span><span class="sxs-lookup"><span data-stu-id="aac59-158">Audio language</span></span>                  |
| <span data-ttu-id="aac59-159">17</span><span class="sxs-lookup"><span data-stu-id="aac59-159">17</span></span>       | <span data-ttu-id="aac59-160">Estensione del linguaggio audio</span><span class="sxs-lookup"><span data-stu-id="aac59-160">Audio language extension</span></span>        |
| <span data-ttu-id="aac59-161">18</span><span class="sxs-lookup"><span data-stu-id="aac59-161">18</span></span>       | <span data-ttu-id="aac59-162">Lingua di immagine</span><span class="sxs-lookup"><span data-stu-id="aac59-162">Subpicture language</span></span>             |
| <span data-ttu-id="aac59-163">19</span><span class="sxs-lookup"><span data-stu-id="aac59-163">19</span></span>       | <span data-ttu-id="aac59-164">Estensione della lingua di immagine</span><span class="sxs-lookup"><span data-stu-id="aac59-164">Subpicture language extension</span></span>   |
| <span data-ttu-id="aac59-165">20</span><span class="sxs-lookup"><span data-stu-id="aac59-165">20</span></span>       | <span data-ttu-id="aac59-166">Codice area del lettore</span><span class="sxs-lookup"><span data-stu-id="aac59-166">Player region code</span></span>              |
| <span data-ttu-id="aac59-167">21</span><span class="sxs-lookup"><span data-stu-id="aac59-167">21</span></span>       | <span data-ttu-id="aac59-168">Riservato</span><span class="sxs-lookup"><span data-stu-id="aac59-168">Reserved</span></span>                        |
| <span data-ttu-id="aac59-169">22</span><span class="sxs-lookup"><span data-stu-id="aac59-169">22</span></span>       | <span data-ttu-id="aac59-170">Riservato</span><span class="sxs-lookup"><span data-stu-id="aac59-170">Reserved</span></span>                        |
| <span data-ttu-id="aac59-171">23</span><span class="sxs-lookup"><span data-stu-id="aac59-171">23</span></span>       | <span data-ttu-id="aac59-172">Riservato</span><span class="sxs-lookup"><span data-stu-id="aac59-172">Reserved</span></span>                        |



 

## <a name="see-also"></a><span data-ttu-id="aac59-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aac59-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac59-174">**GetGPRM**</span><span class="sxs-lookup"><span data-stu-id="aac59-174">**GetGPRM**</span></span>](getgprm-method.md)
</dt> <dt>

[<span data-ttu-id="aac59-175">**SetGPRM**</span><span class="sxs-lookup"><span data-stu-id="aac59-175">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



