---
description: Avvia la procedura guidata Passport se utilizzata con Rundll32.exe.
title: PassportWizardRunDll (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: a858a36caa4af8095fc7023abae5ad918321f53e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232110"
---
# <a name="passportwizardrundll-function"></a><span data-ttu-id="0d7d7-103">PassportWizardRunDll (funzione)</span><span class="sxs-lookup"><span data-stu-id="0d7d7-103">PassportWizardRunDll function</span></span>

<span data-ttu-id="0d7d7-104">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="0d7d7-105">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d7d7-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0d7d7-106">Avvia la procedura guidata Passport se utilizzata con Rundll32.exe.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-106">Launches the Passport Wizard when used with Rundll32.exe.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d7d7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d7d7-107">Syntax</span></span>


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="0d7d7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d7d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d7d7-109">*hwndStub* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d7d7-109">*hwndStub* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d7d7-110">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="0d7d7-110">Type: **HWND**</span></span>

<span data-ttu-id="0d7d7-111">Handle per una finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-111">A handle to an owner window.</span></span> <span data-ttu-id="0d7d7-112">Questo parametro è in genere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-112">This parameter is typically set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0d7d7-113">*hAppInstance* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d7d7-113">*hAppInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d7d7-114">Tipo: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="0d7d7-114">Type: **HINSTANCE**</span></span>

<span data-ttu-id="0d7d7-115">Handle per il file di libreria, ottenuto come valore restituito da [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("Netplwiz").</span><span class="sxs-lookup"><span data-stu-id="0d7d7-115">A handle to the library file, obtained as a return value from [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span></span>

</dd> <dt>

<span data-ttu-id="0d7d7-116">*lpszCmdLine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d7d7-116">*lpszCmdLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d7d7-117">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="0d7d7-117">Type: **LPTSTR**</span></span>

<span data-ttu-id="0d7d7-118">Dati dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-118">Argument data.</span></span> <span data-ttu-id="0d7d7-119">Questo valore sarà sempre vuoto.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-119">This value will always be empty.</span></span>

</dd> <dt>

<span data-ttu-id="0d7d7-120">*nCmdShow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d7d7-120">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d7d7-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0d7d7-121">Type: **int**</span></span>

<span data-ttu-id="0d7d7-122">Imposta la modalità di visualizzazione per la finestra.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-122">Sets the display mode for the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d7d7-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d7d7-123">Return value</span></span>

<span data-ttu-id="0d7d7-124">No.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-124">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d7d7-125">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="0d7d7-125">Remarks</span></span>

<span data-ttu-id="0d7d7-126">La procedura guidata Passport viene utilizzata per ottenere un Passport predefinito per Windows.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-126">The Passport Wizard is used to obtain a default Passport for Windows.</span></span> <span data-ttu-id="0d7d7-127">Un passaporto consente all'utente di accedere in modo personalizzato a tutti i siti Web di MSN e ad altri siti abilitati per Passport usando l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-127">A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address.</span></span> <span data-ttu-id="0d7d7-128">L'uso di **PassportWizardRunDll** come punto di ingresso nel file Netplwiz.dll tramite un comando rundll32 consente di avviare la procedura guidata Passport da una riga di comando come se si trattasse di un file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-128">Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.</span></span>

<span data-ttu-id="0d7d7-129">**PassportWizardRunDll** viene usato esclusivamente nel contesto di un comando Rundll32.exe come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0d7d7-129">**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:</span></span>

<span data-ttu-id="0d7d7-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span><span class="sxs-lookup"><span data-stu-id="0d7d7-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span></span>

<span data-ttu-id="0d7d7-131">L'uso di una funzione del punto di ingresso con Rundll32.exe non è simile a una normale chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-131">Using an entry point function with Rundll32.exe does not resemble a normal function call.</span></span> <span data-ttu-id="0d7d7-132">Il nome della funzione e il nome del file con estensione dll in cui è archiviato vengono utilizzati solo come parametri della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-132">The function name and the name of the .dll file where it is stored are used only as command-line parameters.</span></span> <span data-ttu-id="0d7d7-133">La definizione della funzione mostrata in sintassi è solo un prototipo standard per tutte le funzioni che è possibile chiamare usando rundll32.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-133">The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32.</span></span> <span data-ttu-id="0d7d7-134">I valori specifici per *hwndStub*, *hAppInstance* e *nCmdShow* non vengono forniti dall'utente, ma vengono gestiti dietro le quinte da rundll32.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-134">The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32.</span></span> <span data-ttu-id="0d7d7-135">**PassportWizardRunDll** non utilizza il valore *lpszCmdLine* , pertanto non sono necessari dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="0d7d7-135">**PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d7d7-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d7d7-136">Requirements</span></span>



| <span data-ttu-id="0d7d7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d7d7-137">Requirement</span></span> | <span data-ttu-id="0d7d7-138">Valore</span><span class="sxs-lookup"><span data-stu-id="0d7d7-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d7d7-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d7d7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0d7d7-140">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0d7d7-140">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="0d7d7-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d7d7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0d7d7-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d7d7-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0d7d7-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d7d7-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d7d7-144"><dt>Nessuno</dt></span><span class="sxs-lookup"><span data-stu-id="0d7d7-144"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="0d7d7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0d7d7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d7d7-146"><dt>Netplwiz.dll (versione 5,60 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="0d7d7-146"><dt>Netplwiz.dll (version 5.60 or later)</dt></span></span> </dl> |



 

 
