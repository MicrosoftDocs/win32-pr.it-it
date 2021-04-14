---
description: Recupera un'impostazione della shell globale.
ms.assetid: b9b1542c-8e25-4966-b3df-13bfbd9b28aa
title: Metodo IShellDispatch4. GetSetting (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 755ee1d2bbd5026b1cc3ca165649e0fcb4ab20ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977986"
---
# <a name="ishelldispatch4getsetting-method"></a><span data-ttu-id="e9a2b-103">IShellDispatch4. GetSetting, metodo</span><span class="sxs-lookup"><span data-stu-id="e9a2b-103">IShellDispatch4.GetSetting method</span></span>

<span data-ttu-id="e9a2b-104">Recupera un'impostazione della shell globale.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-104">Retrieves a global Shell setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a2b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9a2b-105">Syntax</span></span>


```JScript
retVal = IShellDispatch4.GetSetting(
  lSetting
)
```


```VB

IShellDispatch4.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a><span data-ttu-id="e9a2b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9a2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9a2b-107">*lSetting* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9a2b-107">*lSetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a2b-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="e9a2b-108">Type: **long**</span></span>

<span data-ttu-id="e9a2b-109">Valore che specifica l'impostazione della shell corrente da recuperare.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-109">A value that specifies the current Shell setting to retrieve.</span></span> <span data-ttu-id="e9a2b-110">In ogni chiamata è possibile recuperare una sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-110">Only one setting can be retrieved in each call.</span></span> <span data-ttu-id="e9a2b-111">I valori seguenti sono riconosciuti da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-111">The following values are recognized by this method.</span></span>

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span data-ttu-id="e9a2b-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF\_AUTOCHECKSELECT** (0x00800000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-113">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-113">**Windows Vista and later**.</span></span> <span data-ttu-id="e9a2b-114">Stato dell'opzione **utilizza caselle di controllo per selezionare gli elementi** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-114">The state of the **Use check boxes to select items** option.</span></span> <span data-ttu-id="e9a2b-115">Questa opzione viene abilitata automaticamente quando nel sistema è configurato un dispositivo di input penna.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-115">This option is enabled automatically when the system has a pen input device configured.</span></span>

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span data-ttu-id="e9a2b-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-117">Not used.</span></span>

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span data-ttu-id="e9a2b-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF\_DONTPRETTYPATH** (0x00000800)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-119">Stato dell'opzione **Consenti tutti i nomi maiuscoli** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-119">The state of the **Allow all uppercase names** option.</span></span> <span data-ttu-id="e9a2b-120">A partire da Windows Vista, questa opzione di cartella non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-120">As of Windows Vista, this folder option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span data-ttu-id="e9a2b-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-122">Stato del **doppio clic per aprire l'opzione di un elemento (con un solo clic per la selezione)** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-122">The state of the **Double-click to open an item (single-click to select)** option.</span></span>

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span data-ttu-id="e9a2b-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ FILTER** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF\_FILTER** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-124">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span data-ttu-id="e9a2b-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF\_HIDDENFILEEXTS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-126">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-126">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span data-ttu-id="e9a2b-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF\_HIDEICONS** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-128">Lo stato dell'icona visualizzato nella visualizzazione elenco di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-128">The state of icon display in the Windows Explorer list view.</span></span> <span data-ttu-id="e9a2b-129">Se questa opzione è attiva, nessuna icona viene visualizzata nella visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-129">If this option is active, no icons are displayed in the list view.</span></span>

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span data-ttu-id="e9a2b-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF\_ICONSONLY** (0x01000000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-131">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-131">**Windows Vista and later**.</span></span> <span data-ttu-id="e9a2b-132">Lo stato del nome visualizzato viene visualizzato nella visualizzazione elenco di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-132">The state of display name display in the Windows Explorer list view.</span></span> <span data-ttu-id="e9a2b-133">Se questa opzione è attiva, le icone vengono visualizzate nella visualizzazione elenco, ma i nomi visualizzati non lo sono.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-133">If this option is active, icons are displayed in the list view, but display names are not.</span></span>

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span data-ttu-id="e9a2b-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF\_MAPNETDRVBUTTON** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-135">Stato del pulsante dell' **unità di rete Mostra mappa nell'opzione della barra degli strumenti** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-135">The state of the **Show map network drive button in toolbar** option.</span></span> <span data-ttu-id="e9a2b-136">A partire da Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-136">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span data-ttu-id="e9a2b-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF\_NOCONFIRMRECYCLE** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-138">Stato della finestra di dialogo di conferma dell' **eliminazione della visualizzazione** del cestino.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-138">The state of the Recycle Bin's **Display delete confirmation dialog** option.</span></span>

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span data-ttu-id="e9a2b-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF\_NONETCRAWLING** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-140">Lo stato dell'opzione **Cerca automaticamente le cartelle di rete e le stampanti** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-140">The state of the **Automatically search for network folders and printers** option.</span></span> <span data-ttu-id="e9a2b-141">A partire da Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-141">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span data-ttu-id="e9a2b-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF\_SEPPROCESS** (0x00080000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-143">Lo stato delle **finestre della cartella di avvio in un'opzione di processo separata** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-143">The state of the **Launch folder windows in a separate process** option.</span></span>

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span data-ttu-id="e9a2b-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF\_SERVERADMINUI** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-145">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-145">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span data-ttu-id="e9a2b-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-147">Stato dell'opzione **file e cartelle nascosti** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-147">The state of the **Hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span data-ttu-id="e9a2b-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF\_SHOWATTRIBCOL** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-149">Stato dell'opzione **Mostra attributi di file in visualizzazione dettagli** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-149">The state of the **Show File Attributes in Detail View** option.</span></span> <span data-ttu-id="e9a2b-150">A partire da Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-150">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span data-ttu-id="e9a2b-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-152">Lo stato dell'opzione **Mostra file NTFS crittografati o compressi in colore** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-152">The state of the **Show encrypted or compressed NTFS files in color** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span data-ttu-id="e9a2b-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-154">Stato dell'opzione **Nascondi estensioni per i tipi di file noti** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-154">The state of the **Hide extensions for known file types** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span data-ttu-id="e9a2b-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF\_SHOWINFOTIP** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-156">Lo stato dell'opzione **Mostra descrizione popup per cartella e elementi desktop** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-156">The state of the **Show pop-up description for folder and desktop items** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span data-ttu-id="e9a2b-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF\_SHOWSTARTPAGE** (0x00400000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-158">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-158">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span data-ttu-id="e9a2b-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF\_SHOWSUPERHIDDEN** (0x00040000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-160">Stato dell'opzione **Nascondi file del sistema operativo protetti** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-160">The state of the **Hide protected operating system files** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span data-ttu-id="e9a2b-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-162">Stato dell'opzione **file e cartelle nascosti** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-162">The state of the **Hidden files and folders** option.</span></span> <span data-ttu-id="e9a2b-163">In Windows Vista e versioni successive, equivale a SSF \_ SHOWALLOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-163">In Windows Vista and later, this is equivalent to SSF\_SHOWALLOBJECTS.</span></span> <span data-ttu-id="e9a2b-164">Nelle versioni di Windows precedenti a Windows Vista, questo valore si riferisce allo stato dell'opzione non **visualizzare cartelle e file nascosti** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-164">In versions of Windows before Windows Vista, this value referred to the state of the **Do not show hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span data-ttu-id="e9a2b-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY** (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF\_SHOWTYPEOVERLAY** (0x02000000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-166">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-166">**Windows Vista and later**.</span></span> <span data-ttu-id="e9a2b-167">Stato dell'icona del **file visualizzato nell'opzione anteprime** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-167">The state of the **Display file icon on thumbnails** option.</span></span> <span data-ttu-id="e9a2b-168">Se questa opzione è attiva, quando un file fornisce una rappresentazione di anteprima viene applicata una sovrapposizione del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-168">If this option is active, a file type overlay is applied when a file supplies a thumbnail representation.</span></span>

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span data-ttu-id="e9a2b-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF\_SORTCOLUMNS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-170">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-170">Not used.</span></span>

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span data-ttu-id="e9a2b-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF\_STARTPANELON** (0x00200000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-172">Lo stato dell'opzione di visualizzazione di Windows XP, che consente di selezionare tra lo stile di Windows XP e lo stile classico.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-172">The state of the Windows XP display option, which selects between the Windows XP style and the classic style.</span></span> <span data-ttu-id="e9a2b-173">A partire da Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-173">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span data-ttu-id="e9a2b-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WebView** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF\_WEBVIEW** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-175">Stato della **visualizzazione come opzione di visualizzazione Web**.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-175">The state of the **Display as a web view option**.</span></span> <span data-ttu-id="e9a2b-176">A partire da Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-176">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span data-ttu-id="e9a2b-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="e9a2b-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF\_WIN95CLASSIC** (0x00000400)</span></span>


</dt> <dd>

<span data-ttu-id="e9a2b-178">Stato dell'opzione di **stile classico** .</span><span class="sxs-lookup"><span data-stu-id="e9a2b-178">The state of the **Classic Style** option.</span></span> <span data-ttu-id="e9a2b-179">A partire da Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-179">As of Windows Vista, this option is no longer available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9a2b-180">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9a2b-180">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e9a2b-181">JScript</span><span class="sxs-lookup"><span data-stu-id="e9a2b-181">JScript</span></span>

<span data-ttu-id="e9a2b-182">Tipo: \**Variant \_ bool \** _</span><span class="sxs-lookup"><span data-stu-id="e9a2b-182">Type: \**VARIANT\_BOOL\** _</span></span>

<span data-ttu-id="e9a2b-183">Impostare su _ *true*\* se l'impostazione esiste; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-183">Set to _ *true*\* if the setting exists; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="e9a2b-184">VB</span><span class="sxs-lookup"><span data-stu-id="e9a2b-184">VB</span></span>

<span data-ttu-id="e9a2b-185">Tipo: \**Variant \_ bool \** _</span><span class="sxs-lookup"><span data-stu-id="e9a2b-185">Type: \**VARIANT\_BOOL\** _</span></span>

<span data-ttu-id="e9a2b-186">Impostare su _ *true*\* se l'impostazione esiste; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-186">Set to _ *true*\* if the setting exists; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="e9a2b-187">Esempio</span><span class="sxs-lookup"><span data-stu-id="e9a2b-187">Examples</span></span>

<span data-ttu-id="e9a2b-188">Negli esempi seguenti viene illustrato l'utilizzo di **GetSetting** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e9a2b-188">The following examples show the use of **GetSetting** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e9a2b-189">JScript</span><span class="sxs-lookup"><span data-stu-id="e9a2b-189">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="e9a2b-190">VBScript</span><span class="sxs-lookup"><span data-stu-id="e9a2b-190">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
</script>
```



<span data-ttu-id="e9a2b-191">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e9a2b-191">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e9a2b-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9a2b-192">Requirements</span></span>



| <span data-ttu-id="e9a2b-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9a2b-193">Requirement</span></span> | <span data-ttu-id="e9a2b-194">Valore</span><span class="sxs-lookup"><span data-stu-id="e9a2b-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a2b-195">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9a2b-195">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a2b-196">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e9a2b-196">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="e9a2b-197">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9a2b-197">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a2b-198">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9a2b-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e9a2b-199">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9a2b-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9a2b-200"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9a2b-200"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e9a2b-201">IDL</span><span class="sxs-lookup"><span data-stu-id="e9a2b-201">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e9a2b-202"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e9a2b-202"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e9a2b-203">DLL</span><span class="sxs-lookup"><span data-stu-id="e9a2b-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9a2b-204"><dt>Shell32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e9a2b-204"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




