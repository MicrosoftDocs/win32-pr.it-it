---
description: Il ControlEvent IgnoreChange viene pubblicato dal controllo Directory quando la cartella selezionata viene modificata da una directory a un'altra nel controllo. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: ControlEvent IgnoreChange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310975"
---
# <a name="ignorechange-controlevent"></a><span data-ttu-id="29b2b-104">ControlEvent IgnoreChange</span><span class="sxs-lookup"><span data-stu-id="29b2b-104">IgnoreChange ControlEvent</span></span>

<span data-ttu-id="29b2b-105">Il ControlEvent IgnoreChange viene pubblicato dal [controllo Directory](directorylist-control.md) quando la cartella selezionata viene modificata da una directory a un'altra nel controllo.</span><span class="sxs-lookup"><span data-stu-id="29b2b-105">The IgnoreChange ControlEvent is published by the [DirectoryList control](directorylist-control.md) when the selected folder is changed from one directory to another directory in the control.</span></span> <span data-ttu-id="29b2b-106">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="29b2b-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="29b2b-107">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="29b2b-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="29b2b-108">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="29b2b-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="29b2b-109">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="29b2b-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="29b2b-110">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="29b2b-110">Published By</span></span>

[<span data-ttu-id="29b2b-111">Elenco di directory</span><span class="sxs-lookup"><span data-stu-id="29b2b-111">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="29b2b-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="29b2b-112">Argument</span></span>

<span data-ttu-id="29b2b-113">Questo ControlEvent non usa un argomento.</span><span class="sxs-lookup"><span data-stu-id="29b2b-113">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="29b2b-114">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="29b2b-114">Action on Subscribers</span></span>

<span data-ttu-id="29b2b-115">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="29b2b-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="29b2b-116">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="29b2b-116">Typical Use</span></span>

<span data-ttu-id="29b2b-117">Il [controllo DirectoryCombo](directorycombo-control.md) USA in genere il IgnoreChange ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="29b2b-117">The [DirectoryCombo control](directorycombo-control.md) commonly employs the IgnoreChange ControlEvent.</span></span>

 

 



