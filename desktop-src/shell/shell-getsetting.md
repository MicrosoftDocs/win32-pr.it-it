---
description: "Metodo Shell.GetSetting: recupera un'impostazione shell globale."
ms.assetid: 3E8C7C6A-5696-4756-B4BF-902FA2420AE9
title: Metodo Shell.GetSetting (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: dc8fe6277208808ad5f5b182f3eee416daf4a5d0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083739"
---
# <a name="shellgetsetting-method"></a><span data-ttu-id="6dd46-103">Metodo Shell.GetSetting</span><span class="sxs-lookup"><span data-stu-id="6dd46-103">Shell.GetSetting method</span></span>

<span data-ttu-id="6dd46-104">Recupera un'impostazione shell globale.</span><span class="sxs-lookup"><span data-stu-id="6dd46-104">Retrieves a global Shell setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd46-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6dd46-105">Syntax</span></span>


```JScript
retVal = Shell.GetSetting(
  lSetting
)
```


```VB

Shell.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a><span data-ttu-id="6dd46-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6dd46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dd46-107">*lSetting* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6dd46-107">*lSetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd46-108">Tipo: **long**</span><span class="sxs-lookup"><span data-stu-id="6dd46-108">Type: **long**</span></span>

<span data-ttu-id="6dd46-109">Valore che specifica l'impostazione shell corrente da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6dd46-109">A value that specifies the current Shell setting to retrieve.</span></span> <span data-ttu-id="6dd46-110">In ogni chiamata è possibile recuperare una sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="6dd46-110">Only one setting can be retrieved in each call.</span></span> <span data-ttu-id="6dd46-111">I valori seguenti vengono riconosciuti da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="6dd46-111">The following values are recognized by this method.</span></span>

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span data-ttu-id="6dd46-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF\_AUTOCHECKSELECT** (0x00800000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-113">**Windows Vista e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-113">**Windows Vista and later**.</span></span> <span data-ttu-id="6dd46-114">Stato dell'opzione **Usa caselle di controllo per selezionare gli** elementi.</span><span class="sxs-lookup"><span data-stu-id="6dd46-114">The state of the **Use check boxes to select items** option.</span></span> <span data-ttu-id="6dd46-115">Questa opzione viene abilitata automaticamente quando nel sistema è configurato un dispositivo di input penna.</span><span class="sxs-lookup"><span data-stu-id="6dd46-115">This option is enabled automatically when the system has a pen input device configured.</span></span>

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span data-ttu-id="6dd46-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="6dd46-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6dd46-117">Not used.</span></span>

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span data-ttu-id="6dd46-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="6dd46-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF\_DONTPRETTYPATH** (0x00000800)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-119">Stato **dell'opzione Consenti tutti i nomi maiuscoli.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-119">The state of the **Allow all uppercase names** option.</span></span> <span data-ttu-id="6dd46-120">A causa di Windows Vista, questa opzione di cartella non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6dd46-120">As of Windows Vista, this folder option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span data-ttu-id="6dd46-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="6dd46-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-122">Stato dell'opzione **Doppio clic per aprire un elemento (clic singolo per selezionare).**</span><span class="sxs-lookup"><span data-stu-id="6dd46-122">The state of the **Double-click to open an item (single-click to select)** option.</span></span>

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span data-ttu-id="6dd46-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ FILTER** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF\_FILTER** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6dd46-124">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span data-ttu-id="6dd46-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="6dd46-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF\_HIDDENFILEEXTS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-126">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6dd46-126">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span data-ttu-id="6dd46-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF\_HIDEICONS** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-128">Lo stato dell'icona viene visualizzato nella Esplora risorse visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="6dd46-128">The state of icon display in the Windows Explorer list view.</span></span> <span data-ttu-id="6dd46-129">Se questa opzione è attiva, non viene visualizzata alcuna icona nella visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="6dd46-129">If this option is active, no icons are displayed in the list view.</span></span>

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span data-ttu-id="6dd46-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF\_ICONSONLY** (0x01000000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-131">**Windows Vista e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-131">**Windows Vista and later**.</span></span> <span data-ttu-id="6dd46-132">Lo stato del nome visualizzato viene visualizzato nella Esplora risorse elenco.</span><span class="sxs-lookup"><span data-stu-id="6dd46-132">The state of display name display in the Windows Explorer list view.</span></span> <span data-ttu-id="6dd46-133">Se questa opzione è attiva, le icone vengono visualizzate nella visualizzazione elenco, ma non i nomi visualizzati.</span><span class="sxs-lookup"><span data-stu-id="6dd46-133">If this option is active, icons are displayed in the list view, but display names are not.</span></span>

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span data-ttu-id="6dd46-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF\_MAPNETDRVBUTTON** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-135">Stato dell'opzione **Mostra unità di rete mappa nella barra degli** strumenti.</span><span class="sxs-lookup"><span data-stu-id="6dd46-135">The state of the **Show map network drive button in toolbar** option.</span></span> <span data-ttu-id="6dd46-136">A data di Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6dd46-136">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span data-ttu-id="6dd46-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF\_NOCONFIRMRECYCLE** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-138">Stato dell'opzione visualizza Cestino di conferma **dell'eliminazione** della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6dd46-138">The state of the Recycle Bin's **Display delete confirmation dialog** option.</span></span>

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span data-ttu-id="6dd46-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF\_NONETCRAWLING** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-140">Stato dell'opzione **Cerca automaticamente cartelle di rete e** stampanti .</span><span class="sxs-lookup"><span data-stu-id="6dd46-140">The state of the **Automatically search for network folders and printers** option.</span></span> <span data-ttu-id="6dd46-141">A data di Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6dd46-141">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span data-ttu-id="6dd46-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF\_SEPPROCESS** (0x00080000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-143">Stato delle finestre **della cartella di avvio in un'opzione di processo** separata.</span><span class="sxs-lookup"><span data-stu-id="6dd46-143">The state of the **Launch folder windows in a separate process** option.</span></span>

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span data-ttu-id="6dd46-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="6dd46-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF\_SERVERADMINUI** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-145">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6dd46-145">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span data-ttu-id="6dd46-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="6dd46-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-147">Stato **dell'opzione File e cartelle nascosti.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-147">The state of the **Hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span data-ttu-id="6dd46-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="6dd46-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF\_SHOWATTRIBCOL** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-149">Stato **dell'opzione Mostra attributi file nella visualizzazione** dettagli.</span><span class="sxs-lookup"><span data-stu-id="6dd46-149">The state of the **Show File Attributes in Detail View** option.</span></span> <span data-ttu-id="6dd46-150">A causa di Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6dd46-150">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span data-ttu-id="6dd46-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="6dd46-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-152">Stato dell'opzione Mostra a colori **i file NTFS crittografati o** compressi.</span><span class="sxs-lookup"><span data-stu-id="6dd46-152">The state of the **Show encrypted or compressed NTFS files in color** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span data-ttu-id="6dd46-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="6dd46-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-154">Stato **dell'opzione Nascondi estensioni per i tipi di file** noti.</span><span class="sxs-lookup"><span data-stu-id="6dd46-154">The state of the **Hide extensions for known file types** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span data-ttu-id="6dd46-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF\_SHOWINFOTIP** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-156">Stato dell'opzione **Mostra descrizione popup per gli elementi della** cartella e del desktop.</span><span class="sxs-lookup"><span data-stu-id="6dd46-156">The state of the **Show pop-up description for folder and desktop items** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span data-ttu-id="6dd46-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF\_SHOWSTARTPAGE** (0x00400000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-158">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6dd46-158">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span data-ttu-id="6dd46-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF\_SHOWSUPERHIDDEN** (0x00040000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-160">Stato dell'opzione **Nascondi file del sistema operativo protetti.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-160">The state of the **Hide protected operating system files** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span data-ttu-id="6dd46-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="6dd46-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-162">Stato **dell'opzione File e cartelle nascosti.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-162">The state of the **Hidden files and folders** option.</span></span> <span data-ttu-id="6dd46-163">In Windows Vista e versioni successive equivale a SSF \_ SHOWALLOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="6dd46-163">In Windows Vista and later, this is equivalent to SSF\_SHOWALLOBJECTS.</span></span> <span data-ttu-id="6dd46-164">Nelle versioni di Windows precedenti a Windows Vista, questo valore fa riferimento allo stato dell'opzione Non visualizzare file **e cartelle nascosti.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-164">In versions of Windows before Windows Vista, this value referred to the state of the **Do not show hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span data-ttu-id="6dd46-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY** (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF\_SHOWTYPEOVERLAY** (0x02000000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-166">**Windows Vista e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-166">**Windows Vista and later**.</span></span> <span data-ttu-id="6dd46-167">Stato **dell'opzione Visualizza icona file nelle anteprime.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-167">The state of the **Display file icon on thumbnails** option.</span></span> <span data-ttu-id="6dd46-168">Se questa opzione è attiva, viene applicata una sovrimpressione del tipo di file quando un file fornisce una rappresentazione in anteprima.</span><span class="sxs-lookup"><span data-stu-id="6dd46-168">If this option is active, a file type overlay is applied when a file supplies a thumbnail representation.</span></span>

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span data-ttu-id="6dd46-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="6dd46-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF\_SORTCOLUMNS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-170">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6dd46-170">Not used.</span></span>

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span data-ttu-id="6dd46-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF\_STARTPANELON** (0x00200000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-172">Stato dell'opzione di visualizzazione di Windows XP, che consente di scegliere tra lo stile di Windows XP e lo stile classico.</span><span class="sxs-lookup"><span data-stu-id="6dd46-172">The state of the Windows XP display option, which selects between the Windows XP style and the classic style.</span></span> <span data-ttu-id="6dd46-173">A data di Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6dd46-173">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span data-ttu-id="6dd46-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WEBVIEW** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="6dd46-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF\_WEBVIEW** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-175">Stato **dell'opzione Visualizza come visualizzazione Web**.</span><span class="sxs-lookup"><span data-stu-id="6dd46-175">The state of the **Display as a web view option**.</span></span> <span data-ttu-id="6dd46-176">A data di Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6dd46-176">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span data-ttu-id="6dd46-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="6dd46-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF\_WIN95CLASSIC** (0x00000400)</span></span>


</dt> <dd>

<span data-ttu-id="6dd46-178">Stato **dell'opzione Stile** classico.</span><span class="sxs-lookup"><span data-stu-id="6dd46-178">The state of the **Classic Style** option.</span></span> <span data-ttu-id="6dd46-179">A data di Windows Vista, questa opzione non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6dd46-179">As of Windows Vista, this option is no longer available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dd46-180">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6dd46-180">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6dd46-181">JScript</span><span class="sxs-lookup"><span data-stu-id="6dd46-181">JScript</span></span>

<span data-ttu-id="6dd46-182">Tipo: **VARIANT \_ BOOL \***</span><span class="sxs-lookup"><span data-stu-id="6dd46-182">Type: **VARIANT\_BOOL\***</span></span>

<span data-ttu-id="6dd46-183">Impostare su **true se** l'impostazione esiste; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-183">Set to **true** if the setting exists; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="6dd46-184">VB</span><span class="sxs-lookup"><span data-stu-id="6dd46-184">VB</span></span>

<span data-ttu-id="6dd46-185">Tipo: **VARIANT \_ BOOL \***</span><span class="sxs-lookup"><span data-stu-id="6dd46-185">Type: **VARIANT\_BOOL\***</span></span>

<span data-ttu-id="6dd46-186">Impostare su **true se** l'impostazione esiste; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="6dd46-186">Set to **true** if the setting exists; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="6dd46-187">Esempio</span><span class="sxs-lookup"><span data-stu-id="6dd46-187">Examples</span></span>

<span data-ttu-id="6dd46-188">Negli esempi seguenti viene illustrato l'uso **di GetSetting** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6dd46-188">The following examples show the use of **GetSetting** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6dd46-189">Jscript:</span><span class="sxs-lookup"><span data-stu-id="6dd46-189">JScript:</span></span>


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



<span data-ttu-id="6dd46-190">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="6dd46-190">VBScript:</span></span>


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
```



<span data-ttu-id="6dd46-191">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6dd46-191">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6dd46-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6dd46-192">Requirements</span></span>



| <span data-ttu-id="6dd46-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dd46-193">Requirement</span></span> | <span data-ttu-id="6dd46-194">Valore</span><span class="sxs-lookup"><span data-stu-id="6dd46-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd46-195">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dd46-195">Minimum supported client</span></span><br/> | <span data-ttu-id="6dd46-196">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6dd46-196">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="6dd46-197">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dd46-197">Minimum supported server</span></span><br/> | <span data-ttu-id="6dd46-198">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6dd46-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6dd46-199">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6dd46-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dd46-200"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="6dd46-200"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6dd46-201">Idl</span><span class="sxs-lookup"><span data-stu-id="6dd46-201">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6dd46-202"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="6dd46-202"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6dd46-203">DLL</span><span class="sxs-lookup"><span data-stu-id="6dd46-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dd46-204"><dt>Shell32.dll (versione 6.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6dd46-204"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




