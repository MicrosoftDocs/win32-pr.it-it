---
description: Nondeferred azioni personalizzate che chiamano librerie a collegamento dinamico o script possono accedere a un'installazione in esecuzione per eseguire query o modificare gli attributi della sessione di installazione corrente.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Accesso alla sessione corrente del programma di installazione dall'interno di un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967307"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a><span data-ttu-id="13ffc-103">Accesso alla sessione corrente del programma di installazione dall'interno di un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="13ffc-103">Accessing the Current Installer Session from Inside a Custom Action</span></span>

<span data-ttu-id="13ffc-104">Nondeferred azioni personalizzate che chiamano [librerie a collegamento dinamico](dynamic-link-libraries.md) o [script](scripts.md) possono accedere a un'installazione in esecuzione per eseguire query o modificare gli attributi della sessione di installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="13ffc-104">Nondeferred custom actions that call [dynamic-link libraries](dynamic-link-libraries.md) or [scripts](scripts.md) may access a running installation to query or modify the attributes of the current installation session.</span></span> <span data-ttu-id="13ffc-105">Per ogni processo può esistere un solo oggetto **sessione** e gli script di azione personalizzati non devono tentare di creare un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="13ffc-105">Only one **Session** object can exist for each process, and custom action scripts must not attempt to create another session.</span></span>

<span data-ttu-id="13ffc-106">Le azioni personalizzate possono aggiungere, modificare o rimuovere solo righe, colonne o tabelle temporanee da un database.</span><span class="sxs-lookup"><span data-stu-id="13ffc-106">Custom actions can only add, modify, or remove temporary rows, columns, or tables from a database.</span></span> <span data-ttu-id="13ffc-107">Le azioni personalizzate non possono modificare i dati persistenti in un database, ad esempio i dati che fanno parte del database archiviato su disco.</span><span class="sxs-lookup"><span data-stu-id="13ffc-107">Custom actions cannot modify persistent data in a database, for example, data that is a part of the database stored on disk.</span></span>

[<span data-ttu-id="13ffc-108">Librerie a collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="13ffc-108">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)

<span data-ttu-id="13ffc-109">Per accedere a un'installazione in esecuzione, le azioni personalizzate che chiamano librerie a collegamento dinamico (DLL) vengono passate un handle del tipo MSIHANDLE per la sessione corrente come unico argomento al punto di ingresso della DLL denominato nella colonna di destinazione della [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="13ffc-109">To access a running installation, custom actions that call dynamic-link libraries (DLL) are passed a handle of the type MSIHANDLE for the current session as the only argument to the DLL entry point named in the Target column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="13ffc-110">Poiché il programma di installazione fornisce questo handle, l'azione personalizzata non deve chiuderla, ad esempio per ricevere l'handle *hinstall* dal programma di installazione, la funzione azione personalizzata viene dichiarata come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="13ffc-110">Because the installer provides this handle, the custom action should not close it, for example, to receive the handle *hInstall* from the installer, the custom action function is declared as follows.</span></span>


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="13ffc-111">Per l'accesso in sola lettura al database corrente, ottenere l'handle di database chiamando [**funzione MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span><span class="sxs-lookup"><span data-stu-id="13ffc-111">For read-only access to the current database obtain the database handle by calling [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span></span> <span data-ttu-id="13ffc-112">Per ulteriori informazioni, vedere [ottenere un handle di database](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="13ffc-112">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

[<span data-ttu-id="13ffc-113">Script</span><span class="sxs-lookup"><span data-stu-id="13ffc-113">Scripts</span></span>](scripts.md)

<span data-ttu-id="13ffc-114">Le azioni personalizzate scritte in VBScript o JScript possono accedere alla sessione di installazione corrente usando l' [**oggetto Session**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="13ffc-114">Custom actions written in VBScript or JScript can access the current installation session by using the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="13ffc-115">Il programma di installazione crea un oggetto **sessione** denominato "Session" che fa riferimento all'installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="13ffc-115">The installer creates a **Session** object named "Session" that references the current installation.</span></span> <span data-ttu-id="13ffc-116">Per l'accesso in sola lettura al database corrente, utilizzare la proprietà [**database**](session-database.md) dell'oggetto **Session** .</span><span class="sxs-lookup"><span data-stu-id="13ffc-116">For read-only access to the current database use the [**Database**](session-database.md) property of the **Session** object.</span></span>

<span data-ttu-id="13ffc-117">Poiché uno script viene eseguito dal contesto dell'oggetto [**sessione**](session-object.md) , non è sempre necessario qualificare completamente le proprietà e i metodi.</span><span class="sxs-lookup"><span data-stu-id="13ffc-117">Because a script is run from the context of the [**Session**](session-object.md) object, it is not always necessary to fully qualify properties and methods.</span></span> <span data-ttu-id="13ffc-118">Nell'esempio seguente, quando si usa VBScript, il riferimento me può sostituire l'oggetto **Session** . ad esempio, le tre righe seguenti sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="13ffc-118">In the following example, when using VBScript, the Me reference can replace the **Session** object, for example, the following three lines are equivalent.</span></span>


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[<span data-ttu-id="13ffc-119">File eseguibili</span><span class="sxs-lookup"><span data-stu-id="13ffc-119">Executable Files</span></span>](executable-files.md)

<span data-ttu-id="13ffc-120">Non è possibile accedere alla sessione del programma di installazione corrente da azioni personalizzate che chiamano file eseguibili avviati con una riga di comando, ad esempio, il [tipo di azione personalizzata 2](custom-action-type-2.md) e il [tipo di azione personalizzata 18](custom-action-type-18.md).</span><span class="sxs-lookup"><span data-stu-id="13ffc-120">You cannot access the current installer session from custom actions that call executable files launched with a command-line, for example, [Custom Action Type 2](custom-action-type-2.md) and [Custom Action Type 18](custom-action-type-18.md).</span></span>

[<span data-ttu-id="13ffc-121">Azioni personalizzate di esecuzione posticipata</span><span class="sxs-lookup"><span data-stu-id="13ffc-121">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)

<span data-ttu-id="13ffc-122">Non è possibile accedere alla sessione del programma di installazione corrente o a tutti i dati di proprietà da un'azione personalizzata di esecuzione posticipata.</span><span class="sxs-lookup"><span data-stu-id="13ffc-122">You cannot access the current installer session or all property data from a deferred execution custom action.</span></span> <span data-ttu-id="13ffc-123">Per altre informazioni, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="13ffc-123">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="13ffc-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13ffc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13ffc-125">Accesso a un database o a una sessione dall'interno di un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="13ffc-125">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



