---
description: La classe del dispositivo comm/DataModel è costituita da dispositivi DataModel.
ms.assetid: 6bc314c6-30ec-4318-856a-3ab2fa6aadfb
title: comunicazione/datamode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89210bcf14931e3905f71cdbb8678f5519cc4c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308313"
---
# <a name="commdatamodem"></a><span data-ttu-id="7405e-103">comunicazione/datamode</span><span class="sxs-lookup"><span data-stu-id="7405e-103">comm/datamodem</span></span>

<span data-ttu-id="7405e-104">La classe del dispositivo comm/DataModel è costituita da dispositivi DataModel.</span><span class="sxs-lookup"><span data-stu-id="7405e-104">The comm/datamodem device class consists of datamodem devices.</span></span> <span data-ttu-id="7405e-105">Per accedere a questi dispositivi, è possibile usare le funzioni [file](/windows/desktop/FileIO/file-management-functions) e [comunicazioni](/windows/desktop/DevIO/communications-functions).</span><span class="sxs-lookup"><span data-stu-id="7405e-105">You access these devices by using the [file](/windows/desktop/FileIO/file-management-functions) and [communications functions](/windows/desktop/DevIO/communications-functions).</span></span> <span data-ttu-id="7405e-106">I dispositivi in questa classe sono associati a dispositivi line che supportano il \_ tipo di supporto LINEMEDIAMODE DATAmodel, specificato nel membro **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="7405e-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_DATAMODEM media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="7405e-107">La funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo questi membri aggiuntivi:</span><span class="sxs-lookup"><span data-stu-id="7405e-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to the STRINGFORMAT\_BINARY value and appending these additional members:</span></span>

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

<span data-ttu-id="7405e-108">Il membro **hComm** è l'handle della porta di comunicazione aperta.</span><span class="sxs-lookup"><span data-stu-id="7405e-108">The **hComm** member is the handle of the open communications port.</span></span> <span data-ttu-id="7405e-109">Questo membro è **null** se la porta non è ancora aperta o se il parametro *dwSelect* di [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) non è il \_ valore della chiamata LINECALLSELECT.</span><span class="sxs-lookup"><span data-stu-id="7405e-109">This member is **NULL** if the port is not yet open or if the *dwSelect* parameter of [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) is not the LINECALLSELECT\_CALL value.</span></span> <span data-ttu-id="7405e-110">Se una chiamata è attiva, il provider di servizi di solito apre la porta stessa per ottenere il controllo diretto dell'hardware di comunicazione, ma è necessario solo per restituire un handle valido se la linea è connessa.</span><span class="sxs-lookup"><span data-stu-id="7405e-110">If a call is active, the service provider typically opens the port itself to get direct control of the communications hardware, but is only required to return a valid handle if the line is connected.</span></span> <span data-ttu-id="7405e-111">Il provider di servizi apre la porta usando il \_ valore Overlapped del flag file \_ e quindi configura la porta usando le impostazioni specificate dalla funzione [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="7405e-111">The service provider opens the port using the FILE\_FLAG\_OVERLAPPED value and then configures the port using the settings specified by the [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) function.</span></span> <span data-ttu-id="7405e-112">È possibile impostare altre opzioni di configurazione per il dispositivo usando le funzioni di comunicazione con l'handle restituito.</span><span class="sxs-lookup"><span data-stu-id="7405e-112">You can set additional configuration options for the device by using communications functions with the returned handle.</span></span>

<span data-ttu-id="7405e-113">Il membro **szDeviceName** è una stringa con terminazione **null** che specifica il nome della porta di comunicazione associata alla riga, all'indirizzo o alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="7405e-113">The **szDeviceName** member is a **null**-terminated string that specifies the name of the communications port associated with the line, address, or call.</span></span>

<span data-ttu-id="7405e-114">Se **hComm** è un handle valido, è possibile usarlo nelle chiamate successive alle funzioni di file, ad esempio [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), per inviare e ricevere dati sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="7405e-114">If **hComm** is a valid handle, you can use it in subsequent calls to file functions, such as [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), to send and receive data on the call.</span></span> <span data-ttu-id="7405e-115">Al termine dell'utilizzo della porta di comunicazione e preferibilmente prima di utilizzare la funzione [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) per deallocare la chiamata, è necessario chiudere la porta utilizzando la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="7405e-115">When you are finished using the communications port and preferably before you use the [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) function to deallocate the call, you must close the port by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="7405e-116">Quando si usano le funzioni [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) , alcuni provider di servizi richiedono che i dati di configurazione per questa classe di dispositivo abbiano il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="7405e-116">When using the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions, some service providers require that the configuration data for this device class have the following format:</span></span>

``` syntax
typedef struct  tagDEVCFG  {
  DEVCFGHDR   dfgHdr;
  COMMCONFIG  commconfig;
} DEVCFG, *PDEVCFG, FAR* LPDEVCFG;

// Device setting information
typedef struct  tagDEVCFGDR  {
  DWORD       dwSize;
  DWORD       dwVersion;
  WORD        fwOptions;
  WORD        wWaitBong;
} DEVCFGHDR;
```

<span data-ttu-id="7405e-117">Di seguito sono riportate le informazioni di configurazione del dispositivo da usare con le funzioni [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="7405e-117">The following is device configuration information for use with the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions.</span></span>

<dl> <dt>

<span data-ttu-id="7405e-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="7405e-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="7405e-119">Somma delle dimensioni della struttura **DEVCFGHDR** e delle dimensioni effettive della struttura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) .</span><span class="sxs-lookup"><span data-stu-id="7405e-119">Sum of the size of the **DEVCFGHDR** structure and the actual size of the [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7405e-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="7405e-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7405e-121">Numero di versione della struttura **DEVCONFIG** UniModel.</span><span class="sxs-lookup"><span data-stu-id="7405e-121">Version number of the Unimodem **DevConfig** structure.</span></span> <span data-ttu-id="7405e-122">Questo membro può essere MDMCFG \_ Version (0x00010003).</span><span class="sxs-lookup"><span data-stu-id="7405e-122">This member can be MDMCFG\_VERSION (0x00010003).</span></span>

</dd> <dt>

<span data-ttu-id="7405e-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span><span class="sxs-lookup"><span data-stu-id="7405e-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span></span>
</dt> <dd>

<span data-ttu-id="7405e-124">Flag di opzione visualizzati nella pagina di opzioni UniModel.</span><span class="sxs-lookup"><span data-stu-id="7405e-124">Option flags that appear on the Unimodem Option page.</span></span> <span data-ttu-id="7405e-125">Questo membro può essere una combinazione di questi valori:</span><span class="sxs-lookup"><span data-stu-id="7405e-125">This member can be a combination of these values:</span></span>

<dl> <dt>

<span data-ttu-id="7405e-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>PRE-terminale \_ (1)</span><span class="sxs-lookup"><span data-stu-id="7405e-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL\_PRE (1)</span></span>
</dt> <dd>

<span data-ttu-id="7405e-127">Visualizza la schermata pre-terminale.</span><span class="sxs-lookup"><span data-stu-id="7405e-127">Displays the pre-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="7405e-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>POST del terminale \_ (2)</span><span class="sxs-lookup"><span data-stu-id="7405e-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>TERMINAL\_POST (2)</span></span>
</dt> <dd>

<span data-ttu-id="7405e-129">Visualizza la schermata post-terminale.</span><span class="sxs-lookup"><span data-stu-id="7405e-129">Displays the post-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="7405e-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>\_Composizione manuale (4)</span><span class="sxs-lookup"><span data-stu-id="7405e-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>MANUAL\_DIAL (4)</span></span>
</dt> <dd>

<span data-ttu-id="7405e-131">Consente di comporre il telefono manualmente, se è in grado di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="7405e-131">Dials the phone manually, if capable of doing so.</span></span>

</dd> <dt>

<span data-ttu-id="7405e-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>Luci di avvio \_ (8)</span><span class="sxs-lookup"><span data-stu-id="7405e-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>LAUNCH\_LIGHTS (8)</span></span>
</dt> <dd>

<span data-ttu-id="7405e-133">Visualizza l'icona del modem nell'area stato della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7405e-133">Displays the modem icon in the status area of the taskbar.</span></span>

<span data-ttu-id="7405e-134">\_Per impostazione predefinita viene impostato solo il valore luci di avvio</span><span class="sxs-lookup"><span data-stu-id="7405e-134">Only the LAUNCH\_LIGHTS value is set by default</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7405e-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span><span class="sxs-lookup"><span data-stu-id="7405e-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span></span>
</dt> <dd>

<span data-ttu-id="7405e-136">Numero di secondi (in granularità di due secondi) per sostituire l'attesa del tono di credito ($).</span><span class="sxs-lookup"><span data-stu-id="7405e-136">Number of seconds (in two seconds granularity) to replace the wait for credit tone ($).</span></span>

</dd> <dt>

<span data-ttu-id="7405e-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span><span class="sxs-lookup"><span data-stu-id="7405e-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span></span>
</dt> <dd>

<span data-ttu-id="7405e-138">Struttura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) che può essere utilizzata con le funzioni di configurazione delle comunicazioni e del modem.</span><span class="sxs-lookup"><span data-stu-id="7405e-138">[**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure that can be used with the communications and modem configuration functions.</span></span>

</dd> </dl>

 

 
