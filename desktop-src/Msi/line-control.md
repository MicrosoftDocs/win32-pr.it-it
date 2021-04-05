---
description: Il controllo linea è una linea orizzontale.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Controllo linea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba3b7374574e2a0087e7dae8d0ffa9f097be9f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755618"
---
# <a name="line-control"></a><span data-ttu-id="dd07f-103">Controllo linea</span><span class="sxs-lookup"><span data-stu-id="dd07f-103">Line Control</span></span>

<span data-ttu-id="dd07f-104">Il controllo linea è una linea orizzontale.</span><span class="sxs-lookup"><span data-stu-id="dd07f-104">The Line control is a horizontal line.</span></span>

## <a name="control-attributes"></a><span data-ttu-id="dd07f-105">Attributi del controllo</span><span class="sxs-lookup"><span data-stu-id="dd07f-105">Control Attributes</span></span>

<span data-ttu-id="dd07f-106">Con questo controllo è possibile usare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="dd07f-106">You can use the following attributes with this control.</span></span> <span data-ttu-id="dd07f-107">Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo.</span><span class="sxs-lookup"><span data-stu-id="dd07f-107">To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column.</span></span> <span data-ttu-id="dd07f-108">Immettere l'identificatore del ControlEvent nella colonna evento.</span><span class="sxs-lookup"><span data-stu-id="dd07f-108">Enter the identifier of the ControlEvent in the Event column.</span></span>



| <span data-ttu-id="dd07f-109">Identificatore di attributo</span><span class="sxs-lookup"><span data-stu-id="dd07f-109">Attribute identifier</span></span>                       | <span data-ttu-id="dd07f-110">Bit esadecimale</span><span class="sxs-lookup"><span data-stu-id="dd07f-110">Hexadecimal bit</span></span>                  | <span data-ttu-id="dd07f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd07f-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd07f-112">Position</span><span class="sxs-lookup"><span data-stu-id="dd07f-112">Position</span></span>](position-control-attribute.md) |                                  | <span data-ttu-id="dd07f-113">Posizione del controllo nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="dd07f-113">Position of the control in the dialog box.</span></span> <span data-ttu-id="dd07f-114">Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella di controllo](control-table.md) o della [tabella BBControl](bbcontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="dd07f-114">Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md).</span></span> <span data-ttu-id="dd07f-115">Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.</span><span class="sxs-lookup"><span data-stu-id="dd07f-115">Use [installer units](installer-units.md) for length and distance.</span></span><br/>                                         |
| [<span data-ttu-id="dd07f-116">Visible</span><span class="sxs-lookup"><span data-stu-id="dd07f-116">Visible</span></span>](visible-control-attribute.md)   | <span data-ttu-id="dd07f-117">0x00000001 0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd07f-117">0x00000000 0x00000001</span></span><br/> | <span data-ttu-id="dd07f-118">Controllo nascosto.</span><span class="sxs-lookup"><span data-stu-id="dd07f-118">Hidden control.</span></span> <span data-ttu-id="dd07f-119">Controllo visibile.</span><span class="sxs-lookup"><span data-stu-id="dd07f-119">Visible control.</span></span><br/> <span data-ttu-id="dd07f-120">Includere questo bit nella parola bit della colonna attributi nella [tabella dei controlli](control-table.md) o nella [tabella BBControl](bbcontrol-table.md) per rendere il controllo visibile o nascosto alla sua creazione.</span><span class="sxs-lookup"><span data-stu-id="dd07f-120">Include this bit in the bit word of the Attributes column in the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) to make the control visible or hidden upon its creation.</span></span><br/> <span data-ttu-id="dd07f-121">È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).</span><span class="sxs-lookup"><span data-stu-id="dd07f-121">You can also hide or show a control by using the [ControlCondition table](controlcondition-table.md).</span></span><br/> |
| [<span data-ttu-id="dd07f-122">Sunken</span><span class="sxs-lookup"><span data-stu-id="dd07f-122">Sunken</span></span>](sunken-control-attribute.md)     | <span data-ttu-id="dd07f-123">0x00000004 0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd07f-123">0x00000000 0x00000004</span></span><br/> | <span data-ttu-id="dd07f-124">Visualizza lo stile di visualizzazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="dd07f-124">Displays the default visual style.</span></span> <span data-ttu-id="dd07f-125">Visualizza il controllo con un aspetto incassato, 3D.</span><span class="sxs-lookup"><span data-stu-id="dd07f-125">Displays the control with a sunken, 3-D look.</span></span><br/> <span data-ttu-id="dd07f-126">Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="dd07f-126">Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="dd07f-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd07f-127">Remarks</span></span>

<span data-ttu-id="dd07f-128">Questo controllo può essere creato dalla classe statica tramite la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="dd07f-128">This control can be created from the STATIC class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="dd07f-129">Dispone degli stili **\_ incassati** **SS \_ ETCHEDHORZ** e SS.</span><span class="sxs-lookup"><span data-stu-id="dd07f-129">It has the **SS\_ETCHEDHORZ** and **SS\_SUNKEN** styles.</span></span>

 

 
