---
title: Oggetto Settings (Windows Media Player SDK)
description: L'oggetto Settings fornisce un modo per modificare diverse impostazioni di Windows Media Player usando le proprietà e i metodi seguenti.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Finestra oggetti Impostazioni Media Player
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "103857741"
---
# <a name="settings-object"></a><span data-ttu-id="9aa9a-104">Oggetto Settings</span><span class="sxs-lookup"><span data-stu-id="9aa9a-104">Settings Object</span></span>

<span data-ttu-id="9aa9a-105">L'oggetto **Settings** fornisce un modo per modificare diverse impostazioni di Windows Media Player usando le proprietà e i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-105">The **Settings** object provides a way to modify various Windows Media Player settings by using the following properties and methods.</span></span>

<span data-ttu-id="9aa9a-106">L'oggetto **Settings** supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-106">The **Settings** object supports the following properties.</span></span>



| <span data-ttu-id="9aa9a-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9aa9a-107">Property</span></span>                                                  | <span data-ttu-id="9aa9a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9aa9a-108">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9aa9a-109">Avvio automatico</span><span class="sxs-lookup"><span data-stu-id="9aa9a-109">autoStart</span></span>](settings-autostart.md)                       | <span data-ttu-id="9aa9a-110">Specifica o recupera un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-110">Specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>                           |
| [<span data-ttu-id="9aa9a-111">bilanciare</span><span class="sxs-lookup"><span data-stu-id="9aa9a-111">balance</span></span>](settings-balance.md)                           | <span data-ttu-id="9aa9a-112">Specifica o Recupera il saldo stereo corrente.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-112">Specifies or retrieves the current stereo balance.</span></span>                                                                               |
| [<span data-ttu-id="9aa9a-113">baseURL</span><span class="sxs-lookup"><span data-stu-id="9aa9a-113">baseURL</span></span>](settings-baseurl.md)                           | <span data-ttu-id="9aa9a-114">Specifica o recupera l'URL di base usato per la risoluzione del percorso relativo con i comandi script URL incorporati nei file multimediali.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-114">Specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media files.</span></span> |
| [<span data-ttu-id="9aa9a-115">defaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="9aa9a-115">defaultAudioLanguage</span></span>](settings-defaultaudiolanguage.md) | <span data-ttu-id="9aa9a-116">Recupera l'identificatore delle impostazioni locali (LCID) della lingua audio predefinita specificata in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-116">Retrieves the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>                          |
| [<span data-ttu-id="9aa9a-117">defaultFrame</span><span class="sxs-lookup"><span data-stu-id="9aa9a-117">defaultFrame</span></span>](settings-defaultframe.md)                 | <span data-ttu-id="9aa9a-118">Specifica o Recupera il nome del fotogramma utilizzato per visualizzare un URL ricevuto in un evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="9aa9a-118">Specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>                |
| [<span data-ttu-id="9aa9a-119">enableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="9aa9a-119">enableErrorDialogs</span></span>](settings-enableerrordialogs.md)     | <span data-ttu-id="9aa9a-120">Specifica o recupera un valore che indica se le finestre di dialogo di errore vengono visualizzate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-120">Specifies or retrieves a value indicating whether error dialog boxes are shown automatically.</span></span>                                    |
| [<span data-ttu-id="9aa9a-121">invokeURLs</span><span class="sxs-lookup"><span data-stu-id="9aa9a-121">invokeURLs</span></span>](settings-invokeurls.md)                     | <span data-ttu-id="9aa9a-122">Specifica o recupera un valore che indica se gli eventi URL devono avviare un Web browser.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-122">Specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>                                        |
| [<span data-ttu-id="9aa9a-123">isAvailable</span><span class="sxs-lookup"><span data-stu-id="9aa9a-123">isAvailable</span></span>](settings-isavailable.md)                   | <span data-ttu-id="9aa9a-124">Recupera un valore che indica se è disponibile un tipo di informazioni specificato oppure se è possibile eseguire un'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-124">Retrieves whether a specified type of information is available or a specified action can be performed.</span></span>                           |
| [<span data-ttu-id="9aa9a-125">mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="9aa9a-125">mediaAccessRights</span></span>](settings-mediaaccessrights.md)       | <span data-ttu-id="9aa9a-126">Recupera un valore che indica i diritti attualmente concessi per l'accesso alla libreria.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-126">Retrieves a value indicating the rights currently granted for library access.</span></span>                                                    |
| [<span data-ttu-id="9aa9a-127">mute</span><span class="sxs-lookup"><span data-stu-id="9aa9a-127">mute</span></span>](settings-mute.md)                                 | <span data-ttu-id="9aa9a-128">Specifica o recupera un valore che indica se l'audio è disattivato.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-128">Specifies or retrieves a value indicating whether audio is muted.</span></span>                                                                |
| [<span data-ttu-id="9aa9a-129">playCount</span><span class="sxs-lookup"><span data-stu-id="9aa9a-129">playCount</span></span>](settings-playcount.md)                       | <span data-ttu-id="9aa9a-130">Specifica o Recupera il numero di volte in cui un elemento multimediale viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-130">Specifies or retrieves the number of times a media item will play.</span></span>                                                               |
| [<span data-ttu-id="9aa9a-131">tasso</span><span class="sxs-lookup"><span data-stu-id="9aa9a-131">rate</span></span>](settings-rate.md)                                 | <span data-ttu-id="9aa9a-132">Specifica o recupera la frequenza di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-132">Specifies or retrieves the current playback rate.</span></span>                                                                                |
| [<span data-ttu-id="9aa9a-133">volume</span><span class="sxs-lookup"><span data-stu-id="9aa9a-133">volume</span></span>](settings-volume.md)                             | <span data-ttu-id="9aa9a-134">Specifica o Recupera il volume corrente.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-134">Specifies or retrieves the current volume.</span></span>                                                                                       |



 

<span data-ttu-id="9aa9a-135">L'oggetto **Settings** supporta i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9aa9a-135">The **Settings** object supports the following methods.</span></span>



| <span data-ttu-id="9aa9a-136">Metodo</span><span class="sxs-lookup"><span data-stu-id="9aa9a-136">Method</span></span>                                                            | <span data-ttu-id="9aa9a-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9aa9a-137">Description</span></span>                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="9aa9a-138">getMode</span><span class="sxs-lookup"><span data-stu-id="9aa9a-138">getMode</span></span>](settings-getmode.md)                                   | <span data-ttu-id="9aa9a-139">Determina se la modalità ciclo o shuffle è attiva.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-139">Determines whether the loop mode or shuffle mode is active.</span></span> |
| [<span data-ttu-id="9aa9a-140">requestMediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="9aa9a-140">requestMediaAccessRights</span></span>](settings-requestmediaaccessrights.md) | <span data-ttu-id="9aa9a-141">Richiede un livello specificato di accesso alla libreria.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-141">Requests a specified level of access to the library.</span></span>        |
| [<span data-ttu-id="9aa9a-142">setMode</span><span class="sxs-lookup"><span data-stu-id="9aa9a-142">setMode</span></span>](settings-setmode.md)                                   | <span data-ttu-id="9aa9a-143">Imposta la modalità ciclo o shuffle su attivo o inattivo.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-143">Sets the loop mode or shuffle mode to active or inactive.</span></span>   |



 

<span data-ttu-id="9aa9a-144">È possibile accedere all'oggetto **Settings** tramite la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="9aa9a-144">The **Settings** object is accessed through the following property.</span></span>



| <span data-ttu-id="9aa9a-145">Oggetto</span><span class="sxs-lookup"><span data-stu-id="9aa9a-145">Object</span></span>                      | <span data-ttu-id="9aa9a-146">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9aa9a-146">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="9aa9a-147">Player</span><span class="sxs-lookup"><span data-stu-id="9aa9a-147">Player</span></span>](player-object.md) | [<span data-ttu-id="9aa9a-148">impostazioni</span><span class="sxs-lookup"><span data-stu-id="9aa9a-148">settings</span></span>](player-settings.md) |



 

## <a name="see-also"></a><span data-ttu-id="9aa9a-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9aa9a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa9a-150">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="9aa9a-150">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




