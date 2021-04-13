---
description: Panoramica dei controlli input penna per il Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Controlli Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525968"
---
# <a name="ink-controls"></a><span data-ttu-id="742f2-103">Controlli Ink</span><span class="sxs-lookup"><span data-stu-id="742f2-103">Ink Controls</span></span>

<span data-ttu-id="742f2-104">La piattaforma Tablet PC fornisce due controlli, [InkEdit](inkedit-control.md) e [InkPicture](inkpicture-control.md), che consentono di aggiungere facilmente il riconoscimento di input penna e grafia alle applicazioni Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="742f2-104">The Tablet PC platform provides two controls, [InkEdit](inkedit-control.md) and [InkPicture](inkpicture-control.md), which enable you to easily add ink and handwriting recognition to Tablet PC applications.</span></span> <span data-ttu-id="742f2-105">Il controllo InkEdit ha versioni [gestite](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) e Win32, mentre InkPicture include solo le versioni gestite [InkPicture](/previous-versions/ms583740(v=vs.100)) e [ActiveX](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="742f2-105">The InkEdit control has [managed](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) , and Win32 versions, while InkPicture has only the managed [InkPicture](/previous-versions/ms583740(v=vs.100)) and [ActiveX](inkpicture-control-reference.md) versions.</span></span>

<span data-ttu-id="742f2-106">La differenza principale tra i controlli è la modalità di salvataggio dei dati.</span><span class="sxs-lookup"><span data-stu-id="742f2-106">The key difference between the controls is in how data is saved.</span></span> <span data-ttu-id="742f2-107">Per impostazione predefinita, il controllo [InkEdit](inkedit-control.md) Salva l'input penna come testo, mentre [InkPicture](inkpicture-control.md) Salva l'input penna come input penna.</span><span class="sxs-lookup"><span data-stu-id="742f2-107">The [InkEdit](inkedit-control.md) control saves ink as text by default, while [InkPicture](inkpicture-control.md) saves ink as ink.</span></span>

<span data-ttu-id="742f2-108">Il controllo [InkEdit](inkedit-control.md) è destinato alla voce di testo tramite il riconoscimento della grafia.</span><span class="sxs-lookup"><span data-stu-id="742f2-108">The [InkEdit](inkedit-control.md) control is intended for text entry through handwriting recognition.</span></span> <span data-ttu-id="742f2-109">[InkPicture](inkpicture-control.md) è progettato per l'annotazione, ad esempio per contrassegnare una diapositiva della presentazione o un'altra immagine.</span><span class="sxs-lookup"><span data-stu-id="742f2-109">[InkPicture](inkpicture-control.md) is intended for annotation (for example, marking up a presentation slide or other picture).</span></span>

<span data-ttu-id="742f2-110">Nel codice gestito, creare controlli Ink nello stesso thread del thread principale per il form.</span><span class="sxs-lookup"><span data-stu-id="742f2-110">In managed code, create ink controls in the same thread as the main thread for the form.</span></span> <span data-ttu-id="742f2-111">Se un controllo [InkEdit](inkedit-control.md) o [InkPicture](inkpicture-control.md) viene creato in un thread diverso, è possibile che l'applicazione non risponda correttamente.</span><span class="sxs-lookup"><span data-stu-id="742f2-111">If an [InkEdit](inkedit-control.md) or [InkPicture](inkpicture-control.md) control is created in a different thread, then your application may not respond properly.</span></span>

<span data-ttu-id="742f2-112">È necessario modificare in modo esplicito il modello di threading in Apartment a thread singolo (STA) prima di creare un controllo Ink.</span><span class="sxs-lookup"><span data-stu-id="742f2-112">You should explicitly change the threading model to single-thread apartment (STA) before creating an ink control.</span></span> <span data-ttu-id="742f2-113">In questo modo il controllo viene creato nel thread principale.</span><span class="sxs-lookup"><span data-stu-id="742f2-113">This causes the control to be created on the main thread.</span></span> <span data-ttu-id="742f2-114">È possibile utilizzare il codice C++ gestito seguente per impostare in modo esplicito il modello di Threading.</span><span class="sxs-lookup"><span data-stu-id="742f2-114">You can use the following Managed C++ code to explicitly set the threading model.</span></span>


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



<span data-ttu-id="742f2-115">È possibile utilizzare il codice seguente per eseguire la stessa operazione in C \# .</span><span class="sxs-lookup"><span data-stu-id="742f2-115">You can use the following code to do the same thing in C\#.</span></span>


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



<span data-ttu-id="742f2-116">Nel codice gestito, per evitare una perdita di memoria, è necessario chiamare in modo esplicito il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) su qualsiasi controllo Tablet PC a cui è stato collegato un gestore eventi prima che il controllo esca dall'ambito.</span><span class="sxs-lookup"><span data-stu-id="742f2-116">In managed code, to avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC control to which an event handler has been attached before the control goes out of scope.</span></span>

<span data-ttu-id="742f2-117">Le sezioni seguenti descrivono i controlli Ink e l'uso dei controlli Ink nelle applicazioni:</span><span class="sxs-lookup"><span data-stu-id="742f2-117">The following sections describe ink controls and the use of ink controls in applications:</span></span>

-   [<span data-ttu-id="742f2-118">Aggiunta di controlli Ink a un progetto</span><span class="sxs-lookup"><span data-stu-id="742f2-118">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
-   [<span data-ttu-id="742f2-119">Controllo InkEdit</span><span class="sxs-lookup"><span data-stu-id="742f2-119">InkEdit Control</span></span>](inkedit-control.md)
-   [<span data-ttu-id="742f2-120">Controllo InkPicture</span><span class="sxs-lookup"><span data-stu-id="742f2-120">InkPicture Control</span></span>](inkpicture-control.md)

 

 
