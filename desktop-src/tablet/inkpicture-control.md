---
description: Argomento di riferimento per il controllo InkPicture per il Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: Controllo InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded5295d48e4bb14b3c0d83713f33939a360cff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316838"
---
# <a name="inkpicture-control"></a><span data-ttu-id="ddef5-103">Controllo InkPicture</span><span class="sxs-lookup"><span data-stu-id="ddef5-103">InkPicture Control</span></span>

<span data-ttu-id="ddef5-104">Il controllo [InkPicture](inkpicture-control-reference.md) consente di inserire un'immagine (formato. jpg,. bmp,. png o. gif) in un'applicazione a cui gli utenti possono aggiungere input penna.</span><span class="sxs-lookup"><span data-stu-id="ddef5-104">The [InkPicture](inkpicture-control-reference.md) control enables you to place an image (.jpg, .bmp, .png, or .gif format) in an application that users can add ink to.</span></span> <span data-ttu-id="ddef5-105">È destinato agli scenari in cui l'input penna non deve essere riconosciuto come testo ma viene archiviato come input penna.</span><span class="sxs-lookup"><span data-stu-id="ddef5-105">It is intended for scenarios in which ink need not be recognized as text but is stored as ink.</span></span>

<span data-ttu-id="ddef5-106">Gli utenti aggiungono input penna a un livello trasparente usando una penna.</span><span class="sxs-lookup"><span data-stu-id="ddef5-106">Users add ink to a transparent layer using a pen.</span></span> <span data-ttu-id="ddef5-107">Gli utenti possono ridimensionare una finestra di [InkPicture](inkpicture-control-reference.md) senza perdere le informazioni sull'input penna, anche se l'input penna viene ritagliato durante il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="ddef5-107">Users can re-size an [InkPicture](inkpicture-control-reference.md) window without losing any ink information, even if the ink is cropped when re-sizing.</span></span>

<span data-ttu-id="ddef5-108">Il controllo [InkPicture](inkpicture-control-reference.md) include il supporto di stampa di base. Tuttavia, è necessario implementare l'anteprima di stampa o altre funzionalità di stampa avanzate.</span><span class="sxs-lookup"><span data-stu-id="ddef5-108">The [InkPicture](inkpicture-control-reference.md) control includes basic printing support; however, it is up to you to implement print preview or other advanced printing capabilities.</span></span>

<span data-ttu-id="ddef5-109">L'implementazione gestita (.NET Framework) di [InkPicture](/previous-versions/ms583740(v=vs.100)) eredita dalla classe [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="ddef5-109">The managed (.NET Framework) implementation of [InkPicture](/previous-versions/ms583740(v=vs.100)) inherits from the [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) class.</span></span>

<span data-ttu-id="ddef5-110">Per impostazione predefinita, l'input penna viene colorato in nero se non è in modalità a contrasto elevato; in caso contrario, viene impostato sul valore dell'impostazione del colore di sistema corrente (colore \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="ddef5-110">By default, ink is colored black if not in high-contrast mode; otherwise, it is set to the current system color setting (COLOR\_WINDOWTEXT) value.</span></span> <span data-ttu-id="ddef5-111">Inoltre, per impostazione predefinita, [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) è **false**.</span><span class="sxs-lookup"><span data-stu-id="ddef5-111">Also, by default [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) is **FALSE**.</span></span>

<span data-ttu-id="ddef5-112">All'interno del controllo [InkPicture](inkpicture-control-reference.md) , utilizzare l'oggetto [**Ink**](inkdisp-class.md) per caricare e salvare l'input penna.</span><span class="sxs-lookup"><span data-stu-id="ddef5-112">Within the [InkPicture](inkpicture-control-reference.md) control, use the [**Ink**](inkdisp-class.md) object to load and save ink.</span></span>

> [!Note]  
> <span data-ttu-id="ddef5-113">Quando si imposta [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) su **Delete** o **Select**, vengono attivati altri eventi, ad esempio l'evento [**Stroke**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="ddef5-113">When you set the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) to **Delete** or **Select**, other events (such as the [**Stroke**](inkpicture-stroke.md) event) are triggered.</span></span> <span data-ttu-id="ddef5-114">Questi eventi sono utili se si desidera implementare modalità di eliminazione o selezione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ddef5-114">These events are useful if you want to implement your own delete or select modes.</span></span>

 

<span data-ttu-id="ddef5-115">Per informazioni di riferimento dettagliate sul controllo [InkPicture](inkpicture-control-reference.md) , vedere InkPicture.</span><span class="sxs-lookup"><span data-stu-id="ddef5-115">For detailed reference information about the [InkPicture](inkpicture-control-reference.md) control, see InkPicture.</span></span>

<span data-ttu-id="ddef5-116">Le sezioni seguenti illustrano in dettaglio l'uso del controllo [InkPicture](inkpicture-control-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="ddef5-116">The following sections detail the use of the [InkPicture](inkpicture-control-reference.md) control:</span></span>

-   [<span data-ttu-id="ddef5-117">Uso delle immagini</span><span class="sxs-lookup"><span data-stu-id="ddef5-117">Working with Pictures</span></span>](working-with-pictures.md)
-   [<span data-ttu-id="ddef5-118">Uso di InkPicture nelle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="ddef5-118">Using InkPicture on Earlier Versions of Windows</span></span>](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
