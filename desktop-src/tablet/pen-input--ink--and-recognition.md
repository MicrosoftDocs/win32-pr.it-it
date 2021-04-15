---
description: Una nuova funzionalità interessante di Tablet PC è il sistema di input penna.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Input penna, input penna e riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568192"
---
# <a name="pen-input-ink-and-recognition"></a><span data-ttu-id="b5906-103">Input penna, input penna e riconoscimento</span><span class="sxs-lookup"><span data-stu-id="b5906-103">Pen Input, Ink, and Recognition</span></span>

<span data-ttu-id="b5906-104">Una nuova funzionalità interessante di Tablet PC è il sistema di input penna.</span><span class="sxs-lookup"><span data-stu-id="b5906-104">One interesting new feature of Tablet PC is the pen input system.</span></span> <span data-ttu-id="b5906-105">Tutti i computer Tablet PC hanno un digitalizzatore sotto la schermata che accetta input penna.</span><span class="sxs-lookup"><span data-stu-id="b5906-105">All Tablet PC computers have a digitizer beneath the screen that accepts pen input.</span></span> <span data-ttu-id="b5906-106">Questo nuovo meccanismo di input richiede di considerare come compilare applicazioni specifiche per Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="b5906-106">This new input mechanism requires you to think about how to build applications specifically for Tablet PC.</span></span> <span data-ttu-id="b5906-107">La piattaforma Tablet PC Application Programming Interface (API) consente di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="b5906-107">The Tablet PC platform application programming interface (API) helps you do this.</span></span>

## <a name="collection-data-management-and-recognition"></a><span data-ttu-id="b5906-108">Raccolta, Gestione dati e riconoscimento</span><span class="sxs-lookup"><span data-stu-id="b5906-108">Collection, Data Management, and Recognition</span></span>

<span data-ttu-id="b5906-109">La piattaforma Tablet PC può essere divisa in tre aree distinte:</span><span class="sxs-lookup"><span data-stu-id="b5906-109">The Tablet PC platform can be divided into three distinct areas:</span></span>

-   <span data-ttu-id="b5906-110">Raccolta di input penna (oggetti utilizzati per raccogliere input penna dal digitalizzatore).</span><span class="sxs-lookup"><span data-stu-id="b5906-110">Ink collection (objects that are used to collect ink from the digitizer).</span></span>
-   <span data-ttu-id="b5906-111">Gestione dati Ink (oggetti utilizzati per gestire l'input penna).</span><span class="sxs-lookup"><span data-stu-id="b5906-111">Ink data management (objects that are used to manage the collected ink).</span></span>
-   <span data-ttu-id="b5906-112">Riconoscimento dell'input penna (oggetti utilizzati per convertire l'input penna raccolto in altri tipi di dati, ad esempio testo).</span><span class="sxs-lookup"><span data-stu-id="b5906-112">Ink recognition (objects that are used to convert the collected ink into other types of data, such as text).</span></span>

<span data-ttu-id="b5906-113">La figura seguente illustra, a livello generale, il modo in cui l'API della raccolta di input penna (API penna), l'API Gestione dati input penna e l'API di riconoscimento input penna (API di riconoscimento) funzionano insieme nella piattaforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="b5906-113">The following image shows, at a high level, how the Ink Collection API (Pen API), Ink Data Management API (Ink API), and Ink Recognition API (Recognition API) work together in the Tablet PC platform.</span></span>

![Illustraton che illustra in che modo l'API Pen, l'API Ink e l'API di riconoscimento collaborano](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

<span data-ttu-id="b5906-115">L'API della piattaforma Tablet PC è disponibile nelle API gestite e in una libreria COM.</span><span class="sxs-lookup"><span data-stu-id="b5906-115">The Tablet PC platform API is available in Managed APIs as well as a COM library.</span></span> <span data-ttu-id="b5906-116">Negli argomenti seguenti vengono descritti gli oggetti nell'API e viene illustrato il modo in cui le applicazioni utilizzano questi oggetti:</span><span class="sxs-lookup"><span data-stu-id="b5906-116">The following topics describe the objects in the API and illustrate how applications use these objects:</span></span>

-   [<span data-ttu-id="b5906-117">Raccolta di input penna</span><span class="sxs-lookup"><span data-stu-id="b5906-117">Ink Collection</span></span>](ink-collection.md)
-   [<span data-ttu-id="b5906-118">Dati Ink</span><span class="sxs-lookup"><span data-stu-id="b5906-118">Ink Data</span></span>](ink-data.md)
-   [<span data-ttu-id="b5906-119">Riconoscimento input penna</span><span class="sxs-lookup"><span data-stu-id="b5906-119">Ink Recognition</span></span>](ink-recognition.md)
-   [<span data-ttu-id="b5906-120">Analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b5906-120">Ink Analysis</span></span>](ink-analysis.md)
-   [<span data-ttu-id="b5906-121">Riconoscimento della grafia in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5906-121">Handwriting Recognition in Windows Server 2008 R2</span></span>](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



