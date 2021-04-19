---
description: Questo evento notifica al controllo Directory che è necessario creare una nuova cartella; viene creata la nuova cartella e viene selezionato il campo nome della cartella per la modifica.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: ControlEvent DirectoryListNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319971"
---
# <a name="directorylistnew-controlevent"></a><span data-ttu-id="39c90-103">ControlEvent DirectoryListNew</span><span class="sxs-lookup"><span data-stu-id="39c90-103">DirectoryListNew ControlEvent</span></span>

<span data-ttu-id="39c90-104">Questo evento notifica al [controllo Directory](directorylist-control.md) che è necessario creare una nuova cartella; viene creata la nuova cartella e viene selezionato il campo nome della cartella per la modifica.</span><span class="sxs-lookup"><span data-stu-id="39c90-104">This event notifies the [DirectoryList control](directorylist-control.md) that a new folder must be created; it creates the new folder, and selects the name field of the folder for editing.</span></span> <span data-ttu-id="39c90-105">Il nome predefinito della nuova cartella può essere creato nella [tabella UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="39c90-105">The default name of the new folder may be authored in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="39c90-106">Immettere "NewFolder" nella colonna chiave.</span><span class="sxs-lookup"><span data-stu-id="39c90-106">Enter "NewFolder" into the Key column.</span></span> <span data-ttu-id="39c90-107">Immettere il valore per il nome predefinito della nuova cartella nella colonna di testo.</span><span class="sxs-lookup"><span data-stu-id="39c90-107">Enter the value for the default name of the new folder into the Text column.</span></span> <span data-ttu-id="39c90-108">Questo valore deve essere nel formato di un tipo di dati della colonna [filename](filename.md) e utilizzare la \| sintassi LFN di SFN.</span><span class="sxs-lookup"><span data-stu-id="39c90-108">This value must be in the form of a [Filename](filename.md) column data type and use the SFN\|LFN syntax.</span></span> <span data-ttu-id="39c90-109">Se questo valore non è presente nella tabella UIText o non è un valore valido, il programma di installazione userà il valore predefinito "FLDR \| New Folder".</span><span class="sxs-lookup"><span data-stu-id="39c90-109">If this value is not present in the UIText table or is an invalid value, the installer uses a default value of "Fldr\|New Folder."</span></span> <span data-ttu-id="39c90-110">Per informazioni correlate, vedere [finestra di dialogo Sfoglia](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="39c90-110">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="39c90-111">Questo evento deve essere pubblicato da un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che sottoscrive questo evento.</span><span class="sxs-lookup"><span data-stu-id="39c90-111">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="39c90-112">L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="39c90-112">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="39c90-113">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="39c90-113">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="39c90-114">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="39c90-114">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="39c90-115">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="39c90-115">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="39c90-116">Si noti che se questo ControlEvent viene chiamato nuovamente quando una nuova cartella esiste già, non verrà creata una seconda nuova cartella.</span><span class="sxs-lookup"><span data-stu-id="39c90-116">Note that if this ControlEvent is called again when a new folder already exists, a second new folder will not be created.</span></span> <span data-ttu-id="39c90-117">In questo caso, la chiamata a DirectoryListNew consente di selezionare il nome della nuova cartella esistente per la modifica.</span><span class="sxs-lookup"><span data-stu-id="39c90-117">In this case, calling DirectoryListNew selects the existing new folder's name for editing.</span></span>

## <a name="published-by"></a><span data-ttu-id="39c90-118">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="39c90-118">Published By</span></span>

[<span data-ttu-id="39c90-119">Elenco di directory</span><span class="sxs-lookup"><span data-stu-id="39c90-119">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="39c90-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="39c90-120">Argument</span></span>

<span data-ttu-id="39c90-121">Questo ControlEvent non usa un argomento.</span><span class="sxs-lookup"><span data-stu-id="39c90-121">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="39c90-122">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="39c90-122">Action on Subscribers</span></span>

<span data-ttu-id="39c90-123">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="39c90-123">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="39c90-124">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="39c90-124">Typical Use</span></span>

<span data-ttu-id="39c90-125">Per attivare la creazione di una nuova cartella, viene usato un controllo [pulsante](pushbutton-control.md) nella stessa finestra di dialogo modale dell'elenco di directory.</span><span class="sxs-lookup"><span data-stu-id="39c90-125">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger the creation of a new folder.</span></span>

 

 



