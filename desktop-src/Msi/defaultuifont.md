---
description: La proprietà DefaultUIFont imposta lo stile del carattere predefinito usato per i controlli. Per specificare l'impostazione predefinita, impostare DefaultUIFont su uno degli stili predefiniti nella tabella TextStyle della tabella delle proprietà.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Proprietà DefaultUIFont
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333981"
---
# <a name="defaultuifont-property"></a><span data-ttu-id="98a80-104">Proprietà DefaultUIFont</span><span class="sxs-lookup"><span data-stu-id="98a80-104">DefaultUIFont property</span></span>

<span data-ttu-id="98a80-105">La proprietà **DefaultUIFont** imposta lo stile del carattere predefinito usato per i controlli.</span><span class="sxs-lookup"><span data-stu-id="98a80-105">The **DefaultUIFont** property sets the default font style used for controls.</span></span> <span data-ttu-id="98a80-106">Per specificare l'impostazione predefinita, impostare **DefaultUIFont** su uno degli stili predefiniti nella [tabella TextStyle](textstyle-table.md) della [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="98a80-106">To specify the default, set **DefaultUIFont** to one of the predefined styles in the [TextStyle table](textstyle-table.md) in the [Property table](property-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="98a80-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="98a80-107">Remarks</span></span>

<span data-ttu-id="98a80-108">È necessario impostare la proprietà **DefaultUIFont** di ogni pacchetto di installazione con un'interfaccia utente nella [tabella delle proprietà](property-table.md) su uno degli stili predefiniti elencati nella [tabella TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="98a80-108">The **DefaultUIFont** property of every installation package with a UI should be set in the [Property table](property-table.md) to one of the predefined styles listed in the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="98a80-109">Se questa proprietà non è specificata, il programma di installazione utilizza il tipo di carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="98a80-109">If this property is not specified, the installer uses the System font.</span></span> <span data-ttu-id="98a80-110">Questo può causare la visualizzazione non corretta delle stringhe di testo del programma di installazione quando la tabella codici del pacchetto è diversa dalla tabella codici dell'interfaccia utente predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="98a80-110">This can cause the installer to improperly display text strings when the package's code page is different from the user's default UI code page.</span></span>

<span data-ttu-id="98a80-111">Il testo e lo stile del carattere di un controllo possono essere impostati come descritto in [aggiunta di controlli e testo](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="98a80-111">The text and font style of a control can be set as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="98a80-112">Se la stringa di caratteri elencata nella colonna di testo della tabella di [controllo](control-table.md) o della [tabella BBControl](bbcontrol-table.md) non specifica lo stile del tipo di carattere, il controllo utilizzerà il valore della proprietà **DefaultUIFont** come stile del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="98a80-112">If the character string listed in the Text column of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) does not specify the font style, the control uses the value of the **DefaultUIFont** property as the font style.</span></span>

## <a name="requirements"></a><span data-ttu-id="98a80-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98a80-113">Requirements</span></span>



| <span data-ttu-id="98a80-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98a80-114">Requirement</span></span> | <span data-ttu-id="98a80-115">Valore</span><span class="sxs-lookup"><span data-stu-id="98a80-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98a80-116">Versione</span><span class="sxs-lookup"><span data-stu-id="98a80-116">Version</span></span><br/> | <span data-ttu-id="98a80-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="98a80-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="98a80-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="98a80-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="98a80-119">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98a80-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="98a80-120">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="98a80-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98a80-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98a80-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98a80-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="98a80-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




