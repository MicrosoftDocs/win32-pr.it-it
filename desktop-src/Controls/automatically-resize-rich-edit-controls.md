---
title: Come ridimensionare automaticamente i controlli Rich Edit
description: Un'applicazione può ridimensionare un controllo Rich Edit in base alle esigenze, in modo che sia sempre della stessa dimensione del contenuto.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047452"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a><span data-ttu-id="5f388-103">Come ridimensionare automaticamente i controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="5f388-103">How to Automatically Resize Rich Edit Controls</span></span>

<span data-ttu-id="5f388-104">Un'applicazione può ridimensionare un controllo Rich Edit in base alle esigenze, in modo che sia sempre della stessa dimensione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="5f388-104">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="5f388-105">Un controllo Rich Edit supporta questa cosiddetta funzionalità senza *fondo* inviando la finestra padre di un codice di notifica [en \_ REQUESTRESIZE](en-requestresize.md) ogni volta che viene modificata la dimensione del contenuto del controllo.</span><span class="sxs-lookup"><span data-stu-id="5f388-105">A rich edit control supports this so-called *bottomless* functionality by sending its parent window an [EN\_REQUESTRESIZE](en-requestresize.md) notification code whenever the size of the control's content changes.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5f388-106">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="5f388-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5f388-107">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="5f388-107">Technologies</span></span>

-   [<span data-ttu-id="5f388-108">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="5f388-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5f388-109">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="5f388-109">Prerequisites</span></span>

-   <span data-ttu-id="5f388-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="5f388-110">C/C++</span></span>
-   <span data-ttu-id="5f388-111">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="5f388-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5f388-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="5f388-112">Instructions</span></span>

### <a name="automatically-resize-a-rich-edit-control"></a><span data-ttu-id="5f388-113">Ridimensiona automaticamente un controllo Rich Edit</span><span class="sxs-lookup"><span data-stu-id="5f388-113">Automatically Resize a Rich Edit Control</span></span>

<span data-ttu-id="5f388-114">Quando si elabora il codice di notifica [en \_ REQUESTRESIZE](en-requestresize.md) , un'applicazione deve ridimensionare il controllo alle dimensioni nella struttura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) specificata.</span><span class="sxs-lookup"><span data-stu-id="5f388-114">When processing the [EN\_REQUESTRESIZE](en-requestresize.md) notification code, an application should resize the control to the dimensions in the specified [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure.</span></span> <span data-ttu-id="5f388-115">Un'applicazione può anche spostare le informazioni che si avvicinano al controllo per adattarsi alla modifica dell'altezza del controllo.</span><span class="sxs-lookup"><span data-stu-id="5f388-115">An application might also move any information that is near the control to accommodate the control's change in height.</span></span> <span data-ttu-id="5f388-116">Per ridimensionare il controllo, è possibile usare la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .</span><span class="sxs-lookup"><span data-stu-id="5f388-116">To resize the control, you can use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function.</span></span>

<span data-ttu-id="5f388-117">È possibile forzare un controllo Rich Edit senza fondo per inviare un codice di notifica [en \_ REQUESTRESIZE](en-requestresize.md) usando il messaggio [**em \_ REQUESTRESIZE**](em-requestresize.md) .</span><span class="sxs-lookup"><span data-stu-id="5f388-117">You can force a bottomless rich edit control to send an [EN\_REQUESTRESIZE](en-requestresize.md) notification code by using the [**EM\_REQUESTRESIZE**](em-requestresize.md) message.</span></span> <span data-ttu-id="5f388-118">Questo messaggio può essere utile quando si elabora il messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) .</span><span class="sxs-lookup"><span data-stu-id="5f388-118">This message can be useful when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f388-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f388-119">Remarks</span></span>

<span data-ttu-id="5f388-120">Per ricevere i codici di notifica di [ \_ REQUESTRESIZE](en-requestresize.md) , è necessario abilitare la notifica usando il messaggio [em \_ SETEVENTMASK](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="5f388-120">To receive [EN\_REQUESTRESIZE](en-requestresize.md) notification codes, you must enable the notification by using the [EM\_SETEVENTMASK](em-seteventmask.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f388-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f388-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f388-122">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="5f388-122">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="5f388-123">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="5f388-123">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 