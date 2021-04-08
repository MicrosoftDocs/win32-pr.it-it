---
title: Uso di controlli Rebar
description: Questa sezione contiene argomenti che illustrano come creare e usare i controlli Rebar.
ms.assetid: b821216f-609e-41a4-8d45-69609f3572bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9174a4ee05b966037bb30be3e796bcc2c3e00da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730506"
---
# <a name="using-rebar-controls"></a><span data-ttu-id="e593e-103">Uso di controlli Rebar</span><span class="sxs-lookup"><span data-stu-id="e593e-103">Using Rebar Controls</span></span>

<span data-ttu-id="e593e-104">Questa sezione contiene argomenti che illustrano come creare e usare i controlli Rebar.</span><span class="sxs-lookup"><span data-stu-id="e593e-104">This section contains topics that demonstrate how to create and use rebar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e593e-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e593e-105">In this section</span></span>



| <span data-ttu-id="e593e-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="e593e-106">Topic</span></span>                                                                | <span data-ttu-id="e593e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e593e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e593e-108">Come creare controlli Rebar</span><span class="sxs-lookup"><span data-stu-id="e593e-108">How to Create Rebar Controls</span></span>](create-rebar-controls.md)<br/> | <span data-ttu-id="e593e-109">Un'applicazione crea un controllo Rebar chiamando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando [**REBARCLASSNAME**](common-control-window-classes.md) come classe Window.</span><span class="sxs-lookup"><span data-stu-id="e593e-109">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="e593e-110">Per prima cosa, l'applicazione deve registrare la classe della finestra chiamando la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , specificando il bit per le classi di accesso sporadico di ICC \_ \_ nella struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) associata.</span><span class="sxs-lookup"><span data-stu-id="e593e-110">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span> <br/> |



 

 

