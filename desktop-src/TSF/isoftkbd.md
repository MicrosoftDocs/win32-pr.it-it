---
title: Interfaccia ISoftKbd (Softkbdc. h)
description: L'interfaccia ISoftKbd viene utilizzata dalle applicazioni e dai servizi di testo per implementare una tastiera soft.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- Framework servizi di testo interfaccia ISoftKbd
- Framework dei servizi di testo dell'interfaccia ISoftKbd, descritto
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300947"
---
# <a name="isoftkbd-interface"></a><span data-ttu-id="36012-105">Interfaccia ISoftKbd</span><span class="sxs-lookup"><span data-stu-id="36012-105">ISoftKbd interface</span></span>

<span data-ttu-id="36012-106">L'interfaccia **ISoftKbd** viene utilizzata dalle applicazioni e dai servizi di testo per implementare una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-106">The **ISoftKbd** interface is used by applications and text services to implement a soft keyboard.</span></span>

## <a name="members"></a><span data-ttu-id="36012-107">Membri</span><span class="sxs-lookup"><span data-stu-id="36012-107">Members</span></span>

<span data-ttu-id="36012-108">L'interfaccia **ISoftKbd** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="36012-108">The **ISoftKbd** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="36012-109">**ISoftKbd** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="36012-109">**ISoftKbd** also has these types of members:</span></span>

-   [<span data-ttu-id="36012-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="36012-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="36012-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="36012-111">Methods</span></span>

<span data-ttu-id="36012-112">L'interfaccia **ISoftKbd** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="36012-112">The **ISoftKbd** interface has these methods.</span></span>



| <span data-ttu-id="36012-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="36012-113">Method</span></span>                                                                                        | <span data-ttu-id="36012-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36012-114">Description</span></span>                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36012-115">**AdviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="36012-115">**AdviseSoftKeyboardEventSink**</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)                   | <span data-ttu-id="36012-116">Installa un sink di evento della tastiera soft per gestire le notifiche OnKeySelection dalla tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-116">Installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span><br/> |
| [<span data-ttu-id="36012-117">**CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="36012-117">**CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md) | <span data-ttu-id="36012-118">Crea un layout di tastiera soft dalla risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="36012-118">Creates a soft keyboard layout from the specified resource.</span></span><br/>                                        |
| [<span data-ttu-id="36012-119">**CreateSoftKeyboardLayoutFromXMLFile**</span><span class="sxs-lookup"><span data-stu-id="36012-119">**CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | <span data-ttu-id="36012-120">Crea un layout di tastiera soft dal file XML specificato.</span><span class="sxs-lookup"><span data-stu-id="36012-120">Creates a soft keyboard layout from the specified XML file.</span></span><br/>                                        |
| [<span data-ttu-id="36012-121">**CreateSoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="36012-121">**CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)                         | <span data-ttu-id="36012-122">Crea una finestra della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-122">Creates a soft keyboard window.</span></span><br/>                                                                    |
| [<span data-ttu-id="36012-123">**DestroySoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="36012-123">**DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)                       | <span data-ttu-id="36012-124">Elimina una finestra della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-124">Destroys a soft keyboard window.</span></span><br/>                                                                   |
| [<span data-ttu-id="36012-125">**EnumSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="36012-125">**EnumSoftKeyboard**</span></span>](isoftkbd-enumsoftkeyboard.md)                                         | <span data-ttu-id="36012-126">Enumera le possibili tastiere flessibili che supportano la lingua specificata.</span><span class="sxs-lookup"><span data-stu-id="36012-126">Enumerates the possible soft keyboards that support the specified language.</span></span><br/>                        |
| [<span data-ttu-id="36012-127">**GetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="36012-127">**GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)                               | <span data-ttu-id="36012-128">Recupera il colore della tastiera flessibile corrispondente al tipo di colore fornito.</span><span class="sxs-lookup"><span data-stu-id="36012-128">Retrieves the soft keyboard color corresponding to the supplied color type.</span></span><br/>                        |
| [<span data-ttu-id="36012-129">**GetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="36012-129">**GetSoftKeyboardPosSize**</span></span>](isoftkbd-getsoftkeyboardpossize.md)                             | <span data-ttu-id="36012-130">Recupera la posizione iniziale e le dimensioni di una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-130">Retrieves the starting position and size of a soft keyboard.</span></span><br/>                                       |
| [<span data-ttu-id="36012-131">**GetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="36012-131">**GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)                           | <span data-ttu-id="36012-132">Recupera il tipo di carattere del testo utilizzato da una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-132">Retrieves the text font used by a soft keyboard.</span></span><br/>                                                   |
| [<span data-ttu-id="36012-133">**GetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="36012-133">**GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)                           | <span data-ttu-id="36012-134">Recupera la modalità del tipo per una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-134">Retrieves the type mode for a soft keyboard.</span></span><br/>                                                       |
| [<span data-ttu-id="36012-135">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="36012-135">**Initialize**</span></span>](isoftkbd-initialize.md)                                                     | <span data-ttu-id="36012-136">Inizializza tutti i campi necessari per una tastiera morbida e genera layout di tastiera soft standard.</span><span class="sxs-lookup"><span data-stu-id="36012-136">Initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span><br/> |
| [<span data-ttu-id="36012-137">**SelectSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="36012-137">**SelectSoftKeyboard**</span></span>](isoftkbd-selectsoftkeyboard.md)                                     | <span data-ttu-id="36012-138">Seleziona la tastiera soft specificata.</span><span class="sxs-lookup"><span data-stu-id="36012-138">Selects the specified soft keyboard.</span></span><br/>                                                               |
| [<span data-ttu-id="36012-139">**SetKeyboardLabelText**</span><span class="sxs-lookup"><span data-stu-id="36012-139">**SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)                                 | <span data-ttu-id="36012-140">Imposta il testo dell'etichetta dal layout per una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-140">Sets the label text from the layout for a soft keyboard.</span></span><br/>                                           |
| [<span data-ttu-id="36012-141">**SetKeyboardLabelTextCombination**</span><span class="sxs-lookup"><span data-stu-id="36012-141">**SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)           | <span data-ttu-id="36012-142">Imposta una combinazione di etichetta e testo utilizzati per descrivere una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-142">Sets a combination of label and text used to describe a soft keyboard.</span></span><br/>                             |
| [<span data-ttu-id="36012-143">**SetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="36012-143">**SetSoftKeyboardColors**</span></span>](isoftkbd-setsoftkeyboardcolors.md)                               | <span data-ttu-id="36012-144">Imposta il colore della tastiera flessibile corrispondente al tipo di colore fornito.</span><span class="sxs-lookup"><span data-stu-id="36012-144">Sets the soft keyboard color corresponding to the supplied color type.</span></span><br/>                             |
| [<span data-ttu-id="36012-145">**SetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="36012-145">**SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)                             | <span data-ttu-id="36012-146">Imposta la posizione iniziale e la dimensione di una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-146">Sets the starting position and size of a soft keyboard.</span></span><br/>                                            |
| [<span data-ttu-id="36012-147">**SetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="36012-147">**SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)                           | <span data-ttu-id="36012-148">Imposta il tipo di carattere del testo utilizzato da una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-148">Sets the text font used by a soft keyboard.</span></span><br/>                                                        |
| [<span data-ttu-id="36012-149">**SetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="36012-149">**SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)                           | <span data-ttu-id="36012-150">Imposta la modalità del tipo per una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-150">Sets the type mode for a soft keyboard.</span></span><br/>                                                            |
| [<span data-ttu-id="36012-151">**ShowKeysForKeyScanMode**</span><span class="sxs-lookup"><span data-stu-id="36012-151">**ShowKeysForKeyScanMode**</span></span>](isoftkbd-showkeysforkeyscanmode.md)                             | <span data-ttu-id="36012-152">Visualizza le chiavi usate per la modalità di analisi della chiave per una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-152">Displays the keys used for the key scan mode for a soft keyboard.</span></span><br/>                                  |
| [<span data-ttu-id="36012-153">**ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="36012-153">**ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)                                         | <span data-ttu-id="36012-154">Visualizza una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="36012-154">Displays a soft keyboard.</span></span><br/>                                                                          |
| [<span data-ttu-id="36012-155">**UnadviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="36012-155">**UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)               | <span data-ttu-id="36012-156">Rimuove un sink di evento della tastiera flessibile.</span><span class="sxs-lookup"><span data-stu-id="36012-156">Removes a soft keyboard event sink.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="36012-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36012-157">Requirements</span></span>



| <span data-ttu-id="36012-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="36012-158">Requirement</span></span> | <span data-ttu-id="36012-159">Valore</span><span class="sxs-lookup"><span data-stu-id="36012-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36012-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36012-160">Minimum supported client</span></span><br/> | <span data-ttu-id="36012-161">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="36012-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="36012-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36012-162">Minimum supported server</span></span><br/> | <span data-ttu-id="36012-163">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="36012-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="36012-164">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="36012-164">Redistributable</span></span><br/>          | <span data-ttu-id="36012-165">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="36012-165">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="36012-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36012-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="36012-167"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="36012-167"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="36012-168">IDL</span><span class="sxs-lookup"><span data-stu-id="36012-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36012-169"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36012-169"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="36012-170">DLL</span><span class="sxs-lookup"><span data-stu-id="36012-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36012-171"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36012-171"><dt>Softkbd.dll</dt></span></span> </dl> |



 

