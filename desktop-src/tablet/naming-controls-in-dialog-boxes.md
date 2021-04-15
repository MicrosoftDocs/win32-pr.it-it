---
description: Quando si utilizzano le finestre di dialogo di Microsoft Windows, è necessario etichettare tutti i controlli per facilitare la funzionalità di riconoscimento vocale. Nella finestra di dialogo Esegui seguente viene visualizzata un'etichetta di controllo testo statico per una casella di riepilogo a discesa. Il testo statico termina con i due punti.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Denominazione dei controlli nelle finestre di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554083"
---
# <a name="naming-controls-in-dialog-boxes"></a><span data-ttu-id="92d2a-105">Denominazione dei controlli nelle finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="92d2a-105">Naming Controls in Dialog Boxes</span></span>

<span data-ttu-id="92d2a-106">Quando si utilizzano le finestre di dialogo di Microsoft Windows, è necessario etichettare tutti i controlli per facilitare la funzionalità di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="92d2a-106">When using Microsoft Windows dialog boxes, you must label all controls to facilitate speech functionality.</span></span> <span data-ttu-id="92d2a-107">Nella finestra di dialogo **Esegui** seguente viene visualizzata un'etichetta di controllo testo statico per una casella di riepilogo a discesa.</span><span class="sxs-lookup"><span data-stu-id="92d2a-107">The following **Run** dialog box shows a static text control label for a drop-down list box.</span></span> <span data-ttu-id="92d2a-108">Il testo statico termina con i due punti.</span><span class="sxs-lookup"><span data-stu-id="92d2a-108">Static text ends with a colon.</span></span>

![screenshot che mostra la finestra di dialogo Esegui](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

<span data-ttu-id="92d2a-110">Sono disponibili due tipi di controlli:</span><span class="sxs-lookup"><span data-stu-id="92d2a-110">There are two types of controls:</span></span>

-   <span data-ttu-id="92d2a-111">Controlli con didascalie come proprietà del controllo, ad esempio pulsanti di comando e caselle di controllo.</span><span class="sxs-lookup"><span data-stu-id="92d2a-111">Controls that have their captions as a property of that control, such as command buttons and check boxes.</span></span> <span data-ttu-id="92d2a-112">Gli strumenti di accessibilità non hanno problemi nell'identificazione di questi controlli purché la didascalia sia definita correttamente.</span><span class="sxs-lookup"><span data-stu-id="92d2a-112">Accessibility aids have no trouble identifying these controls as long as the caption is properly defined.</span></span>
-   <span data-ttu-id="92d2a-113">I controlli che non hanno didascalie proprie, ad esempio i controlli di modifica, le caselle di riepilogo e le visualizzazioni elenco, devono essere contrassegnati con controlli di testo statici distinti.</span><span class="sxs-lookup"><span data-stu-id="92d2a-113">Controls that do not have their own captions, such as edit controls, list boxes and list views, must be labeled by using separate static text controls.</span></span> <span data-ttu-id="92d2a-114">Per ulteriori informazioni sui controlli che non dispongono di didascalie, vedere [controlli senza proprietà didascalia](controls-without-caption-properties.md).</span><span class="sxs-lookup"><span data-stu-id="92d2a-114">For more information about controls that do not have their own captions, see [Controls Without Caption Properties](controls-without-caption-properties.md).</span></span>

<span data-ttu-id="92d2a-115">È possibile utilizzare diverse tecniche per superare le situazioni in cui i controlli non hanno didascalie proprie, ma sono efficaci solo per le finestre visualizzate da Gestione finestre di dialogo standard (SDM).</span><span class="sxs-lookup"><span data-stu-id="92d2a-115">Several techniques can be used to overcome situations in which controls do not have their own captions, but they are only effective for windows that are displayed by the Standard Dialog Manager (SDM).</span></span> <span data-ttu-id="92d2a-116">Tutte le altre finestre devono esporre i nomi e la relazione tra i controlli, supportando in modo esplicito Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="92d2a-116">All other windows need to expose the names and relationship between controls by explicitly supporting Microsoft Active Accessibility.</span></span> <span data-ttu-id="92d2a-117">Per ulteriori informazioni su Active Accessibility, vedere la sezione relativa all' [accessibilità](/windows/desktop/accessibility) in MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="92d2a-117">For more information about Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section of the MSDN Library.</span></span>

 

 
