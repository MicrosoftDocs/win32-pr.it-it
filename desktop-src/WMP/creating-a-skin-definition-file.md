---
title: Creazione di un file di definizione dell'interfaccia personalizzata
description: Creazione di un file di definizione dell'interfaccia personalizzata
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Interfacce di Windows Media Player Mobile, file di definizione dell'interfaccia
- interfacce, file di definizione dell'interfaccia
- file per le interfacce, definizione dell'interfaccia
- file di definizione dell'interfaccia, creazione
- creazione di interfacce, informazioni
- creazione di interfacce, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711722"
---
# <a name="creating-a-skin-definition-file"></a><span data-ttu-id="4cc84-109">Creazione di un file di definizione dell'interfaccia personalizzata</span><span class="sxs-lookup"><span data-stu-id="4cc84-109">Creating a Skin Definition File</span></span>

<span data-ttu-id="4cc84-110">Un file di definizione dell'interfaccia è un file di testo che definisce un'interfaccia e tutte le relative parti composite.</span><span class="sxs-lookup"><span data-stu-id="4cc84-110">A skin definition file is a text file that defines a skin and all its composite parts.</span></span> <span data-ttu-id="4cc84-111">L'estensione del nome file deve essere. skn.</span><span class="sxs-lookup"><span data-stu-id="4cc84-111">The file name extension must be .skn.</span></span>

<span data-ttu-id="4cc84-112">Ogni file di definizione dell'interfaccia deve iniziare con la riga seguente, che specifica il numero di versione del file di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4cc84-112">Every skin definition file must start with the following line, which specifies the skin file version number.</span></span> <span data-ttu-id="4cc84-113">La tabella seguente illustra le versioni di Windows Media Player e la riga di codice che devono essere usate per identificare ogni in un file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4cc84-113">The following table shows Windows Media Player versions and the code line that should be used to identify each in a skin definition file.</span></span> <span data-ttu-id="4cc84-114">Sebbene alcuni dei numeri nelle righe di codice non siano quelli previsti, sono corretti, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4cc84-114">Although some of the numbers in the code lines are not what you would expect, they are correct as shown in the following table.</span></span>



| <span data-ttu-id="4cc84-115">Versione di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="4cc84-115">Windows Media Player version</span></span> | <span data-ttu-id="4cc84-116">Prima riga del file di definizione dell'interfaccia personalizzata</span><span class="sxs-lookup"><span data-stu-id="4cc84-116">First line of skin definition file</span></span> |
|------------------------------|------------------------------------|
| <span data-ttu-id="4cc84-117">1.01.1</span><span class="sxs-lookup"><span data-stu-id="4cc84-117">1.01.1</span></span><br/>            | <span data-ttu-id="4cc84-118">\[File skin di Pocket WMP v 1.0\]</span><span class="sxs-lookup"><span data-stu-id="4cc84-118">\[Pocket WMP Skin File v1.0\]</span></span>      |
| <span data-ttu-id="4cc84-119">1.2</span><span class="sxs-lookup"><span data-stu-id="4cc84-119">1.2</span></span>                          | <span data-ttu-id="4cc84-120">\[File skin di Pocket WMP v 1.2\]</span><span class="sxs-lookup"><span data-stu-id="4cc84-120">\[Pocket WMP Skin File v1.2\]</span></span>      |
| <span data-ttu-id="4cc84-121">7.0</span><span class="sxs-lookup"><span data-stu-id="4cc84-121">7.0</span></span>                          | <span data-ttu-id="4cc84-122">\[File skin di Pocket WMP v 2.0\]</span><span class="sxs-lookup"><span data-stu-id="4cc84-122">\[Pocket WMP Skin File v2.0\]</span></span>      |
| <span data-ttu-id="4cc84-123">7.1</span><span class="sxs-lookup"><span data-stu-id="4cc84-123">7.1</span></span>                          | <span data-ttu-id="4cc84-124">\[File skin di Pocket WMP v 8.0\]</span><span class="sxs-lookup"><span data-stu-id="4cc84-124">\[Pocket WMP Skin File v8.0\]</span></span>      |
| <span data-ttu-id="4cc84-125">serie 9</span><span class="sxs-lookup"><span data-stu-id="4cc84-125">9 Series</span></span>                     | <span data-ttu-id="4cc84-126">\[File skin di Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="4cc84-126">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="4cc84-127">Windows 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="4cc84-127">10 Mobile</span></span>                    | <span data-ttu-id="4cc84-128">\[File skin di Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="4cc84-128">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="4cc84-129">10,1 Mobile</span><span class="sxs-lookup"><span data-stu-id="4cc84-129">10.1 Mobile</span></span>                  | <span data-ttu-id="4cc84-130">\[File skin di Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="4cc84-130">\[Pocket WMP Skin File v9.0.1\]</span></span>    |



 

<span data-ttu-id="4cc84-131">Il numero di versione 9.0.1 è per le interfacce create appositamente per Windows Media Player 9 serie o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4cc84-131">The version number 9.0.1 is for skins created specifically for Windows Media Player 9 Series or later.</span></span> <span data-ttu-id="4cc84-132">Le interfacce con un numero di versione precedente vengono aperte da Windows Media Player 9 serie o successive come modalità verticale, 96 punti per pollice (DPI).</span><span class="sxs-lookup"><span data-stu-id="4cc84-132">Skins having an earlier version number are opened by Windows Media Player 9 Series or later as portrait mode, 96 dots per inch (DPI) skins.</span></span>

<span data-ttu-id="4cc84-133">Il file di definizione dell'interfaccia è costituito da diverse sezioni.</span><span class="sxs-lookup"><span data-stu-id="4cc84-133">The skin definition file consists of several sections.</span></span> <span data-ttu-id="4cc84-134">Ogni sezione definisce un'area specifica dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4cc84-134">Each section defines a particular area of the skin.</span></span> <span data-ttu-id="4cc84-135">Le sezioni devono essere inserite nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="4cc84-135">The sections must be placed in the following order:</span></span>

1.  <span data-ttu-id="4cc84-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cc84-136">Description</span></span>
2.  <span data-ttu-id="4cc84-137">Bitmap</span><span class="sxs-lookup"><span data-stu-id="4cc84-137">Bitmaps</span></span>
3.  <span data-ttu-id="4cc84-138">Video</span><span class="sxs-lookup"><span data-stu-id="4cc84-138">Video</span></span>
4.  <span data-ttu-id="4cc84-139">Pulsanti</span><span class="sxs-lookup"><span data-stu-id="4cc84-139">Buttons</span></span>
5.  <span data-ttu-id="4cc84-140">Stato</span><span class="sxs-lookup"><span data-stu-id="4cc84-140">Status</span></span>
6.  <span data-ttu-id="4cc84-141">Testo</span><span class="sxs-lookup"><span data-stu-id="4cc84-141">Text</span></span>
7.  <span data-ttu-id="4cc84-142">Testo scorrevole</span><span class="sxs-lookup"><span data-stu-id="4cc84-142">Marquee</span></span>
8.  <span data-ttu-id="4cc84-143">TrackBar</span><span class="sxs-lookup"><span data-stu-id="4cc84-143">Trackbars</span></span>

<span data-ttu-id="4cc84-144">Ogni sezione inizia con il nome della sezione tra parentesi quadre, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4cc84-144">Each section starts with the name of the section in square brackets, for example:</span></span>


```C++
[ Bitmaps ]

```



> [!Note]  
> <span data-ttu-id="4cc84-145">Il file di definizione dell'interfaccia personalizzata non verrà analizzato correttamente a meno che non si includano spazi tra le parentesi quadre e il nome della sezione.</span><span class="sxs-lookup"><span data-stu-id="4cc84-145">Your skin definition file will not be parsed correctly unless you include spaces between the brackets and the name of the section.</span></span>

 

<span data-ttu-id="4cc84-146">Quindi, una o più righe definiscono singole immagini, pulsanti e così via.</span><span class="sxs-lookup"><span data-stu-id="4cc84-146">Then, one or more lines define individual images, buttons, and so on.</span></span> <span data-ttu-id="4cc84-147">Ad esempio, una sezione bitmap potrebbe includere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="4cc84-147">For example, a Bitmaps section might include the following:</span></span>


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="4cc84-148">Non è necessario allineare i valori nelle colonne, ma consentirà al codice di essere più leggibile.</span><span class="sxs-lookup"><span data-stu-id="4cc84-148">It is not necessary to line up the values in columns, but it will help your code to be more readable.</span></span> <span data-ttu-id="4cc84-149">Per altri dettagli su ogni sezione del file di definizione dell'interfaccia, vedere informazioni di [riferimento sull'interfaccia](skin-reference.md).</span><span class="sxs-lookup"><span data-stu-id="4cc84-149">For more details about each section of the skin definition file, see the [Skin Reference](skin-reference.md).</span></span>

> [!Note]  
> <span data-ttu-id="4cc84-150">Non usare le schede in un punto qualsiasi del file; usare invece spazi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="4cc84-150">Do not use tabs anywhere in the file; use extra spaces instead.</span></span> <span data-ttu-id="4cc84-151">Questo è molto importante, perché premendo il tasto TAB durante la scrittura o la modifica del file di definizione della pelle si verificherà un errore dell'intera interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4cc84-151">This is very important, because pressing the TAB key while writing or editing your skin definition file will cause the entire skin to fail.</span></span> <span data-ttu-id="4cc84-152">Ogni riga deve essere completata e non può proseguire su una seconda riga.</span><span class="sxs-lookup"><span data-stu-id="4cc84-152">Each line must be complete and cannot continue onto a second line.</span></span> <span data-ttu-id="4cc84-153">Inoltre, l'area e i valori Super sono deprecati per le interfacce usate con Windows Media Player 10 mobile o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="4cc84-153">Also, the Region and Super values are deprecated for skins used with Windows Media Player 10 Mobile or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4cc84-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4cc84-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cc84-155">**File di definizione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="4cc84-155">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 





