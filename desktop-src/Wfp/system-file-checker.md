---
description: L'utilità verifica file di sistema, Sfc.exe, consente agli amministratori di analizzare tutte le risorse protette per verificarne le versioni.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: Controllo file di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318899"
---
# <a name="system-file-checker"></a><span data-ttu-id="ed220-103">Controllo file di sistema</span><span class="sxs-lookup"><span data-stu-id="ed220-103">System File Checker</span></span>

<span data-ttu-id="ed220-104">L'utilità verifica file di sistema, Sfc.exe, consente agli amministratori di analizzare tutte le risorse protette per verificarne le versioni.</span><span class="sxs-lookup"><span data-stu-id="ed220-104">The system file checker utility, Sfc.exe, allows administrators to scan all protected resources to verify their versions.</span></span>

<span data-ttu-id="ed220-105">I file critici per riavviare le finestre che non corrispondono alla versione di Windows prevista possono essere sostituiti con le versioni corrette.</span><span class="sxs-lookup"><span data-stu-id="ed220-105">Files critical to restart Windows that do not match the expected Windows version may be replaced with the correct versions.</span></span> <span data-ttu-id="ed220-106">Se un file viene ripristinato, vengono ripristinati anche i dati del registro di sistema corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ed220-106">If a file is repaired, the corresponding registry data is also repaired.</span></span> <span data-ttu-id="ed220-107">I file protetti non critici per il riavvio di Windows non vengono corretti.</span><span class="sxs-lookup"><span data-stu-id="ed220-107">Protected files not critical to restart Windows are not repaired.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed220-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed220-108">Syntax</span></span>

<span data-ttu-id="ed220-109">Di seguito è riportata la sintassi della riga di comando per SFC.</span><span class="sxs-lookup"><span data-stu-id="ed220-109">The following is the command-line syntax for Sfc.</span></span>

<span data-ttu-id="ed220-110">**Opzioni SFC \[ = percorso file completo\]**</span><span class="sxs-lookup"><span data-stu-id="ed220-110">**SFC options \[=full file path\]**</span></span>

## <a name="options"></a><span data-ttu-id="ed220-111">Opzioni</span><span class="sxs-lookup"><span data-stu-id="ed220-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="ed220-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE =*x*</span><span class="sxs-lookup"><span data-stu-id="ed220-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*</span></span>
</dt> <dd>

<span data-ttu-id="ed220-113">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-113">This value is not supported.</span></span>

<span data-ttu-id="ed220-114">**Windows Server 2003 e Windows XP:** Imposta la dimensione della cache del file.</span><span class="sxs-lookup"><span data-stu-id="ed220-114">**Windows Server 2003 and Windows XP:** Sets the file cache size.</span></span> <span data-ttu-id="ed220-115">La dimensione predefinita della cache è 0x32 (50 MB).</span><span class="sxs-lookup"><span data-stu-id="ed220-115">The default size of the cache is 0x32 (50 MB).</span></span>

</dd> <dt>

<span data-ttu-id="ed220-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span><span class="sxs-lookup"><span data-stu-id="ed220-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="ed220-117">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-117">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span><span class="sxs-lookup"><span data-stu-id="ed220-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span></span>
</dt> <dd>

<span data-ttu-id="ed220-119">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-119">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span><span class="sxs-lookup"><span data-stu-id="ed220-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span></span>
</dt> <dd>

<span data-ttu-id="ed220-121">Verificare o ripristinare solo i file.</span><span class="sxs-lookup"><span data-stu-id="ed220-121">Verify or repair only files.</span></span> <span data-ttu-id="ed220-122">Non verificare né ripristinare le chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ed220-122">Do not verify or repair registry keys.</span></span>

<span data-ttu-id="ed220-123">**Windows XP:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-123">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span><span class="sxs-lookup"><span data-stu-id="ed220-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span></span>
</dt> <dd>

<span data-ttu-id="ed220-125">Usare questa opzione per le riparazioni offline.</span><span class="sxs-lookup"><span data-stu-id="ed220-125">Use this option for offline repairs.</span></span> <span data-ttu-id="ed220-126">Specificare il percorso della directory di avvio offline.</span><span class="sxs-lookup"><span data-stu-id="ed220-126">Specify the location of the offline boot directory.</span></span>

<span data-ttu-id="ed220-127">**Windows XP:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-127">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span><span class="sxs-lookup"><span data-stu-id="ed220-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span></span>
</dt> <dd>

<span data-ttu-id="ed220-129">Usare questa opzione per le riparazioni offline.</span><span class="sxs-lookup"><span data-stu-id="ed220-129">Use this option for offline repairs.</span></span> <span data-ttu-id="ed220-130">Specificare il percorso della directory Windows offline.</span><span class="sxs-lookup"><span data-stu-id="ed220-130">Specify the location of the offline Windows directory.</span></span>

<span data-ttu-id="ed220-131">**Windows XP:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-131">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span><span class="sxs-lookup"><span data-stu-id="ed220-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span></span>
</dt> <dd>

<span data-ttu-id="ed220-133">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-133">This value is not supported.</span></span>

<span data-ttu-id="ed220-134">**Windows Server 2003 e Windows XP:** Svuota la cache dei file ed esegue l'analisi di tutti i file di sistema protetti.</span><span class="sxs-lookup"><span data-stu-id="ed220-134">**Windows Server 2003 and Windows XP:** Empties the file cache and scans all protected system files.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span><span class="sxs-lookup"><span data-stu-id="ed220-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span></span>
</dt> <dd>

<span data-ttu-id="ed220-136">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-136">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span><span class="sxs-lookup"><span data-stu-id="ed220-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span></span>
</dt> <dd>

<span data-ttu-id="ed220-138">Tornare alle impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="ed220-138">Return to default settings.</span></span>

<span data-ttu-id="ed220-139">**Windows Server 2008 e Windows Vista:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-139">**Windows Server 2008 and Windows Vista:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span><span class="sxs-lookup"><span data-stu-id="ed220-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span></span>
</dt> <dd>

<span data-ttu-id="ed220-141">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-141">This value is not supported.</span></span>

<span data-ttu-id="ed220-142">**Windows Server 2003 e Windows XP:** Analizza tutti i file di sistema protetti a ogni avvio.</span><span class="sxs-lookup"><span data-stu-id="ed220-142">**Windows Server 2003 and Windows XP:** Scans all protected system files at every boot.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span><span class="sxs-lookup"><span data-stu-id="ed220-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span></span>
</dt> <dd>

<span data-ttu-id="ed220-144">Analizza e ripristina il file che si trova nel percorso completo specificato.</span><span class="sxs-lookup"><span data-stu-id="ed220-144">Scans and repairs the file located at the specified full path.</span></span>

<span data-ttu-id="ed220-145">**Windows XP:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-145">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span><span class="sxs-lookup"><span data-stu-id="ed220-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span></span>
</dt> <dd>

<span data-ttu-id="ed220-147">Analizza immediatamente tutti i file di sistema protetti.</span><span class="sxs-lookup"><span data-stu-id="ed220-147">Scans all protected system files immediately.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span><span class="sxs-lookup"><span data-stu-id="ed220-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span></span>
</dt> <dd>

<span data-ttu-id="ed220-149">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-149">This value is not supported.</span></span>

<span data-ttu-id="ed220-150">**Windows Server 2003 e Windows XP:** Analizza tutti i file di sistema protetti all'avvio successivo.</span><span class="sxs-lookup"><span data-stu-id="ed220-150">**Windows Server 2003 and Windows XP:** Scans all protected system files at the next boot.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span><span class="sxs-lookup"><span data-stu-id="ed220-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span></span>
</dt> <dd>

<span data-ttu-id="ed220-152">Verifica il file nel percorso completo specificato.</span><span class="sxs-lookup"><span data-stu-id="ed220-152">Verifies the file at the specified full path.</span></span> <span data-ttu-id="ed220-153">Questa opzione non consente di ripristinare il file.</span><span class="sxs-lookup"><span data-stu-id="ed220-153">This option does not repair the file.</span></span>

<span data-ttu-id="ed220-154">**Windows XP:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-154">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed220-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY.</span><span class="sxs-lookup"><span data-stu-id="ed220-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span></span>
</dt> <dd>

<span data-ttu-id="ed220-156">Analizza tutti i file di sistema protetti senza ripristinare i file.</span><span class="sxs-lookup"><span data-stu-id="ed220-156">Scans all protected system files but does not repair files.</span></span>

<span data-ttu-id="ed220-157">**Windows XP:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="ed220-157">**Windows XP:** Not supported.</span></span>

</dd> </dl>

<span data-ttu-id="ed220-158">SFC imposta il seguente valore del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="ed220-158">Sfc sets the following registry value:</span></span>

 <span data-ttu-id="ed220-159">= HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SfcScan</span><span class="sxs-lookup"><span data-stu-id="ed220-159">= HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\SFCScan</span></span>

<span data-ttu-id="ed220-160">Per ulteriori informazioni, vedere la pagina relativa ai [valori del registro di sistema WFP](wfp-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="ed220-160">For more information, see [WFP Registry Values](wfp-registry-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed220-161">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed220-161">Remarks</span></span>

<span data-ttu-id="ed220-162">Solo in Windows Vista, è possibile impostare la variabile di ambiente **\_ \_ registro traccia di Windows** sul percorso di una directory valida per ricevere un file di log.</span><span class="sxs-lookup"><span data-stu-id="ed220-162">On Windows Vista only, you can set the **WINDOWS\_TRACING\_LOGFILE** environment variable to the location of a valid directory to receive a log file.</span></span>

## <a name="examples"></a><span data-ttu-id="ed220-163">Esempio</span><span class="sxs-lookup"><span data-stu-id="ed220-163">Examples</span></span>

<span data-ttu-id="ed220-164">Le righe di comando di esempio seguenti sono esempi di sintassi sfc.exe.</span><span class="sxs-lookup"><span data-stu-id="ed220-164">The following sample command lines are examples of sfc.exe syntax.</span></span>

<span data-ttu-id="ed220-165">**SFC/SCANNOW**</span><span class="sxs-lookup"><span data-stu-id="ed220-165">**sfc /SCANNOW**</span></span>

<span data-ttu-id="ed220-166">**sfc/VERIFYFILE = c: \\ Windows \\ system32 \\kernel32.dll**</span><span class="sxs-lookup"><span data-stu-id="ed220-166">**sfc /VERIFYFILE=c:\\windows\\system32\\kernel32.dll**</span></span>

<span data-ttu-id="ed220-167">**sfc/SCANFILE = d: \\ Windows \\ system32 \\kernel32.dll/OFFBOOTDIR = d: \\ /OFFWINDIR = d: \\ Windows**</span><span class="sxs-lookup"><span data-stu-id="ed220-167">**sfc /SCANFILE=d:\\windows\\system32\\kernel32.dll /OFFBOOTDIR=d:\\ /OFFWINDIR=d:\\windows**</span></span>

<span data-ttu-id="ed220-168">**sfc/VERIFYONLY./FILESONLY**</span><span class="sxs-lookup"><span data-stu-id="ed220-168">**sfc /VERIFYONLY /FILESONLY**</span></span>

 

 



