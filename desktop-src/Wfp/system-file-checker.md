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
# <a name="system-file-checker"></a>Controllo file di sistema

L'utilità verifica file di sistema, Sfc.exe, consente agli amministratori di analizzare tutte le risorse protette per verificarne le versioni.

I file critici per riavviare le finestre che non corrispondono alla versione di Windows prevista possono essere sostituiti con le versioni corrette. Se un file viene ripristinato, vengono ripristinati anche i dati del registro di sistema corrispondenti. I file protetti non critici per il riavvio di Windows non vengono corretti.

## <a name="syntax"></a>Sintassi

Di seguito è riportata la sintassi della riga di comando per SFC.

**Opzioni SFC \[ = percorso file completo\]**

## <a name="options"></a>Opzioni

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE =*x*
</dt> <dd>

Questo valore non è supportato.

**Windows Server 2003 e Windows XP:** Imposta la dimensione della cache del file. La dimensione predefinita della cache è 0x32 (50 MB).

</dd> <dt>

<span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL
</dt> <dd>

Questo valore non è supportato.

</dd> <dt>

<span id="_ENABLE"></span><span id="_enable"></span>/ENABLE
</dt> <dd>

Questo valore non è supportato.

</dd> <dt>

<span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY
</dt> <dd>

Verificare o ripristinare solo i file. Non verificare né ripristinare le chiavi del registro di sistema.

**Windows XP:** Non supportato.

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR
</dt> <dd>

Usare questa opzione per le riparazioni offline. Specificare il percorso della directory di avvio offline.

**Windows XP:** Non supportato.

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR
</dt> <dd>

Usare questa opzione per le riparazioni offline. Specificare il percorso della directory Windows offline.

**Windows XP:** Non supportato.

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE
</dt> <dd>

Questo valore non è supportato.

**Windows Server 2003 e Windows XP:** Svuota la cache dei file ed esegue l'analisi di tutti i file di sistema protetti.

</dd> <dt>

<span id="_QUIET"></span><span id="_quiet"></span>/QUIET
</dt> <dd>

Questo valore non è supportato.

</dd> <dt>

<span id="_REVERT"></span><span id="_revert"></span>/REVERT
</dt> <dd>

Tornare alle impostazioni predefinite.

**Windows Server 2008 e Windows Vista:** Non supportato.

</dd> <dt>

<span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT
</dt> <dd>

Questo valore non è supportato.

**Windows Server 2003 e Windows XP:** Analizza tutti i file di sistema protetti a ogni avvio.

</dd> <dt>

<span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE
</dt> <dd>

Analizza e ripristina il file che si trova nel percorso completo specificato.

**Windows XP:** Non supportato.

</dd> <dt>

<span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW
</dt> <dd>

Analizza immediatamente tutti i file di sistema protetti.

</dd> <dt>

<span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE
</dt> <dd>

Questo valore non è supportato.

**Windows Server 2003 e Windows XP:** Analizza tutti i file di sistema protetti all'avvio successivo.

</dd> <dt>

<span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE
</dt> <dd>

Verifica il file nel percorso completo specificato. Questa opzione non consente di ripristinare il file.

**Windows XP:** Non supportato.

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY.
</dt> <dd>

Analizza tutti i file di sistema protetti senza ripristinare i file.

**Windows XP:** Non supportato.

</dd> </dl>

SFC imposta il seguente valore del registro di sistema:

 = HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SfcScan

Per ulteriori informazioni, vedere la pagina relativa ai [valori del registro di sistema WFP](wfp-registry-values.md).

## <a name="remarks"></a>Commenti

Solo in Windows Vista, è possibile impostare la variabile di ambiente **\_ \_ registro traccia di Windows** sul percorso di una directory valida per ricevere un file di log.

## <a name="examples"></a>Esempio

Le righe di comando di esempio seguenti sono esempi di sintassi sfc.exe.

**SFC/SCANNOW**

**sfc/VERIFYFILE = c: \\ Windows \\ system32 \\kernel32.dll**

**sfc/SCANFILE = d: \\ Windows \\ system32 \\kernel32.dll/OFFBOOTDIR = d: \\ /OFFWINDIR = d: \\ Windows**

**sfc/VERIFYONLY./FILESONLY**

 

 



