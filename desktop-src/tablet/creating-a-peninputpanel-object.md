---
description: Viene descritto come creare un oggetto PenInputPanel.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Creazione di un oggetto PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305346"
---
# <a name="creating-a-peninputpanel-object"></a><span data-ttu-id="86f8c-103">Creazione di un oggetto PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="86f8c-103">Creating a PenInputPanel Object</span></span>

<span data-ttu-id="86f8c-104">\[[**PenInputPanel**](peninputpanel-class.md) è stato sostituito da [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) e [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="86f8c-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) and [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span></span> <span data-ttu-id="86f8c-105">Vedere la pagina relativa alla [programmazione del pannello input di testo](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="86f8c-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="86f8c-106">I costruttori di codice gestito costituiscono un modo pratico per creare un oggetto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) e collegarlo a un controllo in un unico passaggio.</span><span class="sxs-lookup"><span data-stu-id="86f8c-106">Managed code constructors provide a convenient way to create a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object and attach it to a control in one step.</span></span> <span data-ttu-id="86f8c-107">In questo \# esempio C viene creato un oggetto PenInputPanel che viene collegato a un controllo [InkEdit](/previous-versions/ms835842(v=msdn.10)) esistente, `InkEdit1` , con una riga di codice.</span><span class="sxs-lookup"><span data-stu-id="86f8c-107">This C\# example creates a PenInputPanel object and attaches it to an existing [InkEdit](/previous-versions/ms835842(v=msdn.10)) control, `InkEdit1`, with one line of code.</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



<span data-ttu-id="86f8c-108">Lo stesso esempio in Visual Basic .NET ha un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="86f8c-108">The same example in Visual Basic .NET looks like this:</span></span>


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



<span data-ttu-id="86f8c-109">Questa tecnica è utile nei casi in cui un oggetto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) verrà associato a un singolo controllo per tutta la sua durata.</span><span class="sxs-lookup"><span data-stu-id="86f8c-109">This technique is useful in cases where one [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object will be associated with a single control throughout its lifetime.</span></span> <span data-ttu-id="86f8c-110">Nei casi in cui si desidera utilizzare un oggetto PenInputPanel e associarlo a più controlli, come illustrato nell' [esempio PenInputPanel](peninputpanel-sample.md), utilizzare la proprietà [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) per modificare il controllo a cui è associato l'oggetto PenInputPanel.</span><span class="sxs-lookup"><span data-stu-id="86f8c-110">In cases where you want to use one PenInputPanel object and associate it with multiple controls, as demonstrated in the [PenInputPanel Sample](peninputpanel-sample.md), use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property to change the control to which the PenInputPanel object is associated.</span></span>

<span data-ttu-id="86f8c-111">Per alleghi un oggetto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a un controllo senza utilizzare un costruttore, utilizzare la proprietà [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="86f8c-111">To attach a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control without using a constructor, use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property.</span></span> <span data-ttu-id="86f8c-112">Usare questa tecnica per i linguaggi che non supportano i costruttori gestiti, ad esempio C++.</span><span class="sxs-lookup"><span data-stu-id="86f8c-112">Use this technique for languages that do not support the managed constructors, such as C++.</span></span>

 

 
