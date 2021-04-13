---
description: Poiché le applicazioni esistenti diventano obsolete o non vengono più utilizzate, potrebbe essere necessario rimuoverle.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Eliminazione di un'applicazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401464"
---
# <a name="deleting-a-com-application"></a><span data-ttu-id="1a19a-103">Eliminazione di un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="1a19a-103">Deleting a COM+ Application</span></span>

<span data-ttu-id="1a19a-104">Poiché le applicazioni esistenti diventano obsolete o non vengono più utilizzate, potrebbe essere necessario rimuoverle.</span><span class="sxs-lookup"><span data-stu-id="1a19a-104">As existing applications become dated or are no longer being used, you may need to remove them.</span></span>

<span data-ttu-id="1a19a-105">**Per eliminare un'applicazione COM+**</span><span class="sxs-lookup"><span data-stu-id="1a19a-105">**To delete a COM+ application**</span></span>

1.  <span data-ttu-id="1a19a-106">Nell'albero della console dello strumento di amministrazione Servizi componenti selezionare il computer per cui si desidera eliminare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a19a-106">In the console tree of the Component Services administrative tool, select the computer for which you want to delete an application.</span></span>

2.  <span data-ttu-id="1a19a-107">Aprire la cartella **applicazioni com+** per il computer specificato per visualizzare tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1a19a-107">Open the **COM+ Applications** folder for the specified computer to display all the applications.</span></span>

3.  <span data-ttu-id="1a19a-108">Selezionare l'applicazione che si desidera rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1a19a-108">Select the application you want to remove.</span></span>

4.  <span data-ttu-id="1a19a-109">Se è stata selezionata un'applicazione server, arrestare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a19a-109">If you selected a server application, shut down the application.</span></span> <span data-ttu-id="1a19a-110">Per arrestare un'applicazione, è possibile selezionarla nello strumento di amministrazione Servizi componenti, fare clic con il pulsante destro del mouse e quindi scegliere **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="1a19a-110">You can shut down an application by selecting it in the Component Services administrative tool, right-clicking, and then clicking **Shut down**.</span></span> <span data-ttu-id="1a19a-111">Se è stata selezionata un'applicazione libreria, assicurarsi che tutti i processi che attualmente utilizzano questa applicazione di libreria vengano arrestati.</span><span class="sxs-lookup"><span data-stu-id="1a19a-111">If you selected a library application, make sure that all processes currently using this library application are shut down.</span></span>

5.  <span data-ttu-id="1a19a-112">Scegliere **Elimina** dal menu **azione** .</span><span class="sxs-lookup"><span data-stu-id="1a19a-112">On the **Action** menu, click **Delete**.</span></span> <span data-ttu-id="1a19a-113">È anche possibile fare clic con il pulsante destro del mouse sul nome dell'applicazione e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="1a19a-113">You can also right-click the application name and then click **Delete**.</span></span> <span data-ttu-id="1a19a-114">Per eliminare un'applicazione, è anche possibile selezionarla nello strumento di amministrazione Servizi componenti e premere il tasto **Canc** oppure selezionare l'applicazione, fare clic con il pulsante destro del mouse e scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="1a19a-114">You can also delete an application by selecting it in the Component Services administrative tool and pressing the **Delete** key, or you can select the application, right-click, and then click **Delete**.</span></span>

6.  <span data-ttu-id="1a19a-115">Quando viene richiesto di confermare l'azione, fare clic su **Sì** .</span><span class="sxs-lookup"><span data-stu-id="1a19a-115">Click **Yes** when prompted to confirm your action.</span></span>

<span data-ttu-id="1a19a-116">Inoltre, se un'applicazione server o un proxy di applicazione è stato installato in un computer utilizzando Windows Installer (come descritto in "installazione di applicazioni COM+" nella Guida all'amministrazione di Servizi componenti), è possibile eliminarlo tramite l'utilità Installazione applicazioni nel pannello di controllo di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1a19a-116">In addition, if a server application or application proxy has been installed on a computer using Windows Installer (as described in "Installing COM+ Applications" in the Component Services Administration Guide), you can delete it through the Add/Remove Programs utility in the Microsoft Windows Control Panel.</span></span> <span data-ttu-id="1a19a-117">In alternativa, è possibile eliminare un'applicazione server o un proxy di applicazione installato utilizzando la sintassi della riga di comando Windows Installer:</span><span class="sxs-lookup"><span data-stu-id="1a19a-117">Or you can delete an installed server application or application proxy by using the Windows Installer command line syntax:</span></span>

<span data-ttu-id="1a19a-118">**msiexec-x** *\_ nome applicazione \* \* *. msi**</span><span class="sxs-lookup"><span data-stu-id="1a19a-118">**msiexec -x** *application\_name\*\*\*.msi*\*</span></span>

<span data-ttu-id="1a19a-119">Questi metodi sono particolarmente utili per eliminare le applicazioni COM+ nei computer client che non eseguono lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="1a19a-119">These methods are especially useful for deleting COM+ applications on client machines that are not running the Component Services administrative tool.</span></span>

<span data-ttu-id="1a19a-120">Eliminando l'applicazione vengono eliminati anche tutti i componenti contenuti nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a19a-120">Deleting the application also deletes any components contained in the application.</span></span> <span data-ttu-id="1a19a-121">Se questi componenti dipendono da risorse aggiuntive (connessioni di database, file di dati o di testo, configurazione della radice virtuale di IIS e così via), queste risorse devono essere rimosse tramite meccanismi diversi dallo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="1a19a-121">If these components depend on additional resources (database connections, data or text files, IIS virtual root configuration, and so on), these resources must be removed through mechanisms other than the Component Services administrative tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a19a-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a19a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a19a-123">Copia di componenti</span><span class="sxs-lookup"><span data-stu-id="1a19a-123">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="1a19a-124">Creazione di una nuova applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="1a19a-124">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="1a19a-125">Importazione di componenti</span><span class="sxs-lookup"><span data-stu-id="1a19a-125">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="1a19a-126">Installazione di nuovi componenti</span><span class="sxs-lookup"><span data-stu-id="1a19a-126">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="1a19a-127">Spostamento dei componenti</span><span class="sxs-lookup"><span data-stu-id="1a19a-127">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="1a19a-128">Rimozione di un componente da un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="1a19a-128">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



