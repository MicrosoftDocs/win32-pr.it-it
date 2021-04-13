---
description: '\\Desktop del pannello di controllo HKCU \\ .'
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401478"
---
# <a name="scrnsaveexe"></a><span data-ttu-id="cb4c3-103">SCRNSAVE.EXE</span><span class="sxs-lookup"><span data-stu-id="cb4c3-103">SCRNSAVE.EXE</span></span>

<span data-ttu-id="cb4c3-104">**\\Desktop del pannello di controllo HKCU \\**</span><span class="sxs-lookup"><span data-stu-id="cb4c3-104">**HKCU\\Control Panel\\Desktop**</span></span>



| <span data-ttu-id="cb4c3-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cb4c3-105">Data type</span></span> | <span data-ttu-id="cb4c3-106">Range</span><span class="sxs-lookup"><span data-stu-id="cb4c3-106">Range</span></span>       | <span data-ttu-id="cb4c3-107">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="cb4c3-107">Default value</span></span> |
|-----------|-------------|---------------|
| <span data-ttu-id="cb4c3-108">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="cb4c3-108">REG\_SZ</span></span>   | <span data-ttu-id="cb4c3-109">*Nome file*</span><span class="sxs-lookup"><span data-stu-id="cb4c3-109">*File name*</span></span> | <span data-ttu-id="cb4c3-110">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="cb4c3-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="cb4c3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb4c3-111">Description</span></span>

<span data-ttu-id="cb4c3-112">Specifica il nome del file eseguibile screen saver.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-112">Specifies the name of the screen saver executable file.</span></span>

## <a name="change-method"></a><span data-ttu-id="cb4c3-113">Cambia metodo</span><span class="sxs-lookup"><span data-stu-id="cb4c3-113">Change Method</span></span>

<span data-ttu-id="cb4c3-114">Per modificare il valore di questa voce, nel pannello di controllo fare doppio clic su **schermo**, fare clic sulla scheda **screen saver** , quindi selezionare un screen saver dall'elenco **screen saver** .</span><span class="sxs-lookup"><span data-stu-id="cb4c3-114">To change the value of this entry, in Control Panel double-click **Display**, click the **Screen Saver** tab, and then select a screen saver from the **Screen saver** list.</span></span>

<span data-ttu-id="cb4c3-115">È anche possibile modificare questa voce con la funzione Application Programming Interface (API) **InstallScreenSaver**, che viene esportata da Desk.cpl.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-115">You can also change this entry with the application programming interface (API) function **InstallScreenSaver**, which is exported by Desk.cpl.</span></span> <span data-ttu-id="cb4c3-116">È possibile accedere a questa funzione con la riga di comando **rundll32.exe desk.cpl** *file* InstallScreenSaver, dove *file* è il nome di un file eseguibile di screen saver.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-116">You can access this function with the command line **rundll32.exe desk.cpl,InstallScreenSaver** *file*, where *file* is the name of a screen saver executable file.</span></span>

## <a name="activation-method"></a><span data-ttu-id="cb4c3-117">Metodo di attivazione</span><span class="sxs-lookup"><span data-stu-id="cb4c3-117">Activation Method</span></span>

<span data-ttu-id="cb4c3-118">Le modifiche apportate a questa voce diventano effettive al successivo avvio di un screen saver da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-118">Changes made to this entry become effective the next time the system starts a screen saver.</span></span> <span data-ttu-id="cb4c3-119">Le modifiche apportate a questa voce mentre un screen saver è in esecuzione non hanno alcun effetto sulla screen saver in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-119">Changes made to this entry while a screen saver is running have no effect on the running screen saver.</span></span>

## <a name="notes"></a><span data-ttu-id="cb4c3-120">Note</span><span class="sxs-lookup"><span data-stu-id="cb4c3-120">Notes</span></span>

-   <span data-ttu-id="cb4c3-121">I sistemi operativi Windows aggiungono questa voce al registro di sistema quando si usa **Visualizza** nel pannello di controllo per selezionare un screen saver.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-121">Windows operating systems add this entry to the registry when you use **Display** in Control Panel to select a screen saver.</span></span> <span data-ttu-id="cb4c3-122">Se si disabilitano tutti i salvaschermi selezionando **(nessuno)** dall'elenco Screen saver, il sistema operativo elimina questa voce dal registro di sistema e chiama la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con *uiAction* uguale a spi \_ SETSCREENSAVEACTIVE e *uiParam* uguale a **false**.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-122">If you disable all screen savers by choosing **(None)** from the screen saver list, then the operating system deletes this entry from the registry and calls the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function with *uiAction* equal to SPI\_SETSCREENSAVEACTIVE and *uiParam* equal to **FALSE**.</span></span>
-   <span data-ttu-id="cb4c3-123">Questa voce può essere sostituita da un'impostazione di Criteri di gruppo nei sistemi che supportano Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-123">This entry can be superseded by a Group Policy setting on systems that support Group Policy.</span></span> <span data-ttu-id="cb4c3-124">Mentre il **nome dell'eseguibile screen saver** criteri di gruppo impostazione è abilitato, il sistema ignora questa voce.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-124">While the **Screen saver executable name** Group Policy setting is enabled, the system ignores this entry.</span></span> <span data-ttu-id="cb4c3-125">La configurazione di questa impostazione dei criteri viene archiviata nella voce **SCRNSAVE.EXE** , che si trova nella sottochiave **policy** .</span><span class="sxs-lookup"><span data-stu-id="cb4c3-125">The configuration of this policy setting is stored in the **SCRNSAVE.EXE** entry, which is in the **Policies** subkey.</span></span>

 

 
