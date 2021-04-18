---
description: Panoramica del Framework di servizi di testo per il Tablet PC.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Framework servizi di testo (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318686"
---
# <a name="text-services-framework-tablet-pc"></a><span data-ttu-id="b6169-103">Framework servizi di testo (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="b6169-103">Text Services Framework (Tablet PC)</span></span>

<span data-ttu-id="b6169-104">Quando il [Framework dei servizi di testo (TSF)](../tsf/text-services-framework.md) viene abilitato in un controllo con un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) collegato, l'oggetto PenInputPanel può inserire direttamente il testo.</span><span class="sxs-lookup"><span data-stu-id="b6169-104">When the [Text Services Framework (TSF)](../tsf/text-services-framework.md) is enabled on a control with a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached, the PenInputPanel object can insert text directly.</span></span> <span data-ttu-id="b6169-105">Se il controllo non supporta il Framework di servizi di testo (TSF), l'oggetto PenInputPanel deve ricorrere all'uso della [funzione SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) per inserire il testo.</span><span class="sxs-lookup"><span data-stu-id="b6169-105">If the control does not support Text Services Framework (TSF), the PenInputPanel object must resort to using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) to insert text.</span></span>

<span data-ttu-id="b6169-106">La possibilità di inserire testo direttamente diventa molto importante per i caratteri asiatici orientali, in cui l'uso della [funzione SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) può produrre caratteri non corretti.</span><span class="sxs-lookup"><span data-stu-id="b6169-106">The ability to insert text directly becomes very important for those inputting East Asian characters, where using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) can produce incorrect characters.</span></span>

<span data-ttu-id="b6169-107">TSF fornisce un'interfaccia per la correzione degli errori di riconoscimento che consentono all'utente finale di correggere, riscrivere o persino dettare il testo appropriato.</span><span class="sxs-lookup"><span data-stu-id="b6169-107">TSF provides an interface for correcting recognition errors enabling the end user to correct, rewrite, or even dictate the proper text.</span></span>

<span data-ttu-id="b6169-108">TSF è abilitato chiamando il metodo [EnableTsf](/previous-versions/ms569656(v=vs.100)) con il parametro *Enable* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="b6169-108">TSF is enabled by calling the [EnableTsf](/previous-versions/ms569656(v=vs.100)) method with the *enable* parameter set to **TRUE**.</span></span>

<span data-ttu-id="b6169-109">\[C\#\]</span><span class="sxs-lookup"><span data-stu-id="b6169-109">\[C\#\]</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



<span data-ttu-id="b6169-110">Un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) associato a un controllo [InkEdit](/previous-versions/ms552265(v=vs.100)) fornisce un'esperienza utente affidabile perché il InkEdit supporta TSF.</span><span class="sxs-lookup"><span data-stu-id="b6169-110">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached to a [InkEdit](/previous-versions/ms552265(v=vs.100)) control provides a robust user experience because the InkEdit supports TSF.</span></span> <span data-ttu-id="b6169-111">Tuttavia, assicurarsi di impostare la proprietà [InkMode](/previous-versions/ms835850(v=msdn.10)) su [Microsoft. Ink. InkMode. Ink](/previous-versions/ms827399(v=msdn.10)) sul controllo InkEdit come indicato nell'argomento [procedure consigliate](best-practices.md) .</span><span class="sxs-lookup"><span data-stu-id="b6169-111">However, be sure to set the [InkMode](/previous-versions/ms835850(v=msdn.10)) property to [Microsoft.Ink.InkMode.Ink](/previous-versions/ms827399(v=msdn.10)) on the InkEdit control as mentioned in the [Best Practices](best-practices.md) topic.</span></span>

<span data-ttu-id="b6169-112">L'esempio [PenInputPanel](peninputpanel-sample.md) fornisce un esempio di abilitazione di TSF.</span><span class="sxs-lookup"><span data-stu-id="b6169-112">The [PenInputPanel Sample](peninputpanel-sample.md) provides an example of enabling TSF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6169-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6169-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6169-114">Text Services Framework</span><span class="sxs-lookup"><span data-stu-id="b6169-114">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
