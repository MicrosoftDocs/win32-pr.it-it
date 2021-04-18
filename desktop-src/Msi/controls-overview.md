---
description: Windows Installer implementa una serie di controlli standard che gli autori di pacchetti possono inserire nelle finestre di dialogo. Tuttavia, non tutti i controlli standard di Microsoft Windows sono disponibili e non è possibile creare controlli personalizzati per l'uso con l'interfaccia utente del programma di installazione.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Panoramica sui controlli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fbd8477416eb5a126eca56cb1050112309b0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318290"
---
# <a name="controls-overview"></a><span data-ttu-id="c3ba9-104">Panoramica sui controlli</span><span class="sxs-lookup"><span data-stu-id="c3ba9-104">Controls Overview</span></span>

<span data-ttu-id="c3ba9-105">Windows Installer implementa una serie di controlli standard che gli autori di pacchetti possono inserire nelle finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c3ba9-105">Windows Installer implements a number of standard controls that package authors can place onto dialog boxes.</span></span> <span data-ttu-id="c3ba9-106">Tuttavia, non tutti i controlli standard di Microsoft Windows sono disponibili e non è possibile creare controlli personalizzati per l'uso con l'interfaccia utente del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="c3ba9-106">However, not all standard Microsoft Windows controls are available, and custom controls cannot be created for use with the installer UI.</span></span>

<span data-ttu-id="c3ba9-107">I controlli vengono creati nelle finestre di dialogo del programma di installazione in modo analogo a come le finestre di dialogo vengono create a livello di programmazione tramite l'API dell'interfaccia utente di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c3ba9-107">Controls are created on dialog boxes in the installer in a manner similar to how dialog boxes are created programmatically using the Microsoft Windows user interface API.</span></span> <span data-ttu-id="c3ba9-108">Viene creato un controllo da un modello registrato nella tabella dei controlli.</span><span class="sxs-lookup"><span data-stu-id="c3ba9-108">A control is created from a template recorded in the Control table.</span></span> <span data-ttu-id="c3ba9-109">Questo modello è leggermente diverso perché contiene il nome univoco della finestra di dialogo in cui viene visualizzato il controllo.</span><span class="sxs-lookup"><span data-stu-id="c3ba9-109">This template is slightly different in that it contains the unique name of the dialog box on which the control appears.</span></span>

<span data-ttu-id="c3ba9-110">Nell'API dell'interfaccia utente di Microsoft Windows, l'interazione dell'utente viene eseguita creando una funzione di callback per gestire i messaggi inviati dal controllo.</span><span class="sxs-lookup"><span data-stu-id="c3ba9-110">In the Microsoft Windows user interface API, user interaction is accomplished by creating a callback function to handle messages posted by the control.</span></span> <span data-ttu-id="c3ba9-111">Inoltre, la maggior parte dei controlli di Microsoft Windows riceve messaggi, ad esempio quelli inviati dalla funzione [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="c3ba9-111">Also, most Microsoft Windows controls receive messages, such as those sent by the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="c3ba9-112">La comunicazione tra l'utente e i controlli viene eseguita nel programma di installazione tramite l'uso di [ControlEvents](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c3ba9-112">Communication between the user and controls is accomplished in the installer through the use of [ControlEvents](controlevent-overview.md).</span></span> <span data-ttu-id="c3ba9-113">Tuttavia, esiste un set limitato di ControlEvents specifici per ogni controllo nel set limitato di controlli in Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c3ba9-113">However, there is a limited set of ControlEvents that are specific to each control in the limited set of controls in Windows Installer.</span></span> <span data-ttu-id="c3ba9-114">I controlli possono inviare più di un ControlEvent e possono ricevere più di un ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="c3ba9-114">Controls may post more than one ControlEvent and may receive more than one ControlEvent.</span></span>

<span data-ttu-id="c3ba9-115">I controlli possono pubblicare ControlEvents specifiche tramite l'uso della tabella ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="c3ba9-115">Controls can publish specific ControlEvents through the use of the ControlEvent table.</span></span> <span data-ttu-id="c3ba9-116">I controlli possono ricevere ControlEvents tramite l'uso della [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3ba9-116">Controls can receive ControlEvents through the use of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="c3ba9-117">Windows Installer pubblica ControlEvents anche durante l'esecuzione di alcune azioni e i controlli sottoscritti a questi ControlEvents nella tabella EventMapping li ricevono.</span><span class="sxs-lookup"><span data-stu-id="c3ba9-117">Windows Installer publishes ControlEvents during the execution of some actions as well, and controls subscribed to these ControlEvents in the EventMapping table receive them.</span></span>

 

 
