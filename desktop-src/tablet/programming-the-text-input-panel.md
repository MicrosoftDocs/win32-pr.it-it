---
description: A partire da Windows Vista, TextInputPanel sostituisce l'oggetto PenInputPanel per il controllo dell'aspetto e del comportamento sullo schermo del pannello di input del tablet. nelle sezioni seguenti viene descritto come programmare il pannello input utilizzando le interfacce di programmazione dell'applicazione Pannello di input di testo. TextInputPanel per gli utenti del pannello di input di PenInputPanelUsing AutoCompleteEnabling correzione del testo per l'input penna personalizzato CollectorsNote il pannello input di testo viene implementato in un file eseguibile denominato TabTip.exe. L'esecuzione di TabTip.exe con il parametro/SeekDesktop tenta di eseguire una versione ridotta della funzionalità del pannello di input in un desktop interattivo non standard, creato con CreateDesktop. Per la maggior parte dei desktop creati, il pannello di input verrà eseguito automaticamente in questa modalità. Questo parametro fornisce i mezzi per avviarlo in scenari di applicazione insoliti che altrimenti impediscano l'avvio automatico. Se il pannello input è già in esecuzione sul desktop, questo parametro non avrà alcun effetto e l'istanza di TabTip.exe verrà chiusa immediatamente.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programmazione del pannello input di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318692"
---
# <a name="programming-the-text-input-panel"></a><span data-ttu-id="e0ace-107">Programmazione del pannello input di testo</span><span class="sxs-lookup"><span data-stu-id="e0ace-107">Programming the Text Input Panel</span></span>

<span data-ttu-id="e0ace-108">A partire da Windows Vista, [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) sostituisce l'oggetto [**PenInputPanel**](peninputpanel-class.md) per il controllo dell'aspetto e del comportamento sullo schermo del pannello input penna.</span><span class="sxs-lookup"><span data-stu-id="e0ace-108">Starting with Windows Vista, the [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) supersedes the [**PenInputPanel**](peninputpanel-class.md) for controlling the onscreen appearance and behavior of the Tablet Input Panel.</span></span>

<span data-ttu-id="e0ace-109">Le sezioni seguenti descrivono la programmazione del pannello di input usando le interfacce di programmazione delle applicazioni del pannello input di testo.</span><span class="sxs-lookup"><span data-stu-id="e0ace-109">The following sections describe programming the Input Panel using the Text Input Panel application programming interfaces.</span></span>

-   [<span data-ttu-id="e0ace-110">TextInputPanel per utenti di PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="e0ace-110">TextInputPanel for Users of PenInputPanel</span></span>](textinputpanel-for-users-of-peninputpanel.md)
-   [<span data-ttu-id="e0ace-111">Uso del completamento automatico del pannello di input</span><span class="sxs-lookup"><span data-stu-id="e0ace-111">Using Input Panel AutoComplete</span></span>](using-input-panel-autocomplete.md)
-   [<span data-ttu-id="e0ace-112">Abilitazione della correzione del testo per gli agenti di raccolta input penna personalizzati</span><span class="sxs-lookup"><span data-stu-id="e0ace-112">Enabling Text Correction for Custom Ink Collectors</span></span>](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> <span data-ttu-id="e0ace-113">Il pannello input di testo viene implementato in un file eseguibile denominato TabTip.exe.</span><span class="sxs-lookup"><span data-stu-id="e0ace-113">The Text Input Panel is implemented in an executable file called TabTip.exe.</span></span> <span data-ttu-id="e0ace-114">L'esecuzione di TabTip.exe con il parametro */SeekDesktop* tenta di eseguire una versione ridotta della funzionalità del pannello di input in un desktop interattivo non standard, creato con [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span><span class="sxs-lookup"><span data-stu-id="e0ace-114">Running TabTip.exe with the */SeekDesktop* parameter attempts to run a reduced functionality version of Input Panel on a nonstandard interactive desktop, as created with [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span> <span data-ttu-id="e0ace-115">Per la maggior parte dei desktop creati, il pannello di input verrà eseguito automaticamente in questa modalità.</span><span class="sxs-lookup"><span data-stu-id="e0ace-115">For most created desktops, Input Panel will automatically run in this mode already.</span></span> <span data-ttu-id="e0ace-116">Questo parametro fornisce i mezzi per avviarlo in scenari di applicazione insoliti che altrimenti impediscano l'avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="e0ace-116">This parameter provides the means for launching it in unusual application scenarios that otherwise prevent the automatic launch.</span></span> <span data-ttu-id="e0ace-117">Se il pannello input è già in esecuzione sul desktop, questo parametro non avrà alcun effetto e l'istanza di TabTip.exe verrà chiusa immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e0ace-117">If Input Panel is already running on the desktop, this parameter will have no effect and the instance of TabTip.exe will exit immediately.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e0ace-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0ace-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0ace-119">Programmazione del pannello di input usando la classe PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="e0ace-119">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
