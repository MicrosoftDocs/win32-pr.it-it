---
description: L'utilità di controllo file di sistema, Sfc.exe, consente agli amministratori di analizzare tutte le risorse protette per verificarne le versioni.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: Verifica file di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f751aa30c06dbff90b8d5221974236b45edf9f0f278c144f755568a0040f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330283"
---
# <a name="system-file-checker"></a>Verifica file di sistema

L'utilità di controllo file di sistema, Sfc.exe, consente agli amministratori di analizzare tutte le risorse protette per verificarne le versioni.

I file critici per il Windows che non corrispondono alla versione Windows prevista possono essere sostituiti con le versioni corrette. Se un file viene ripristinato, vengono ripristinati anche i dati del Registro di sistema corrispondenti. I file protetti non critici per il riavvio Windows non vengono ripristinati.

## <a name="syntax"></a>Sintassi

Di seguito è riportata la sintassi della riga di comando per Sfc.

**Opzioni SFC \[ =percorso completo del file\]**

## <a name="options"></a>Opzioni

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*
</dt> <dd>

Questo valore non è supportato.

**Windows Server 2003 e Windows XP:** Imposta le dimensioni della cache del file. Le dimensioni predefinite della cache sono 0x32 (50 MB).

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

Verificare o ripristinare solo i file. Non verificare o ripristinare le chiavi del Registro di sistema.

**Windows XP:** Non supportato.

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR
</dt> <dd>

Usare questa opzione per le riparazione offline. Specificare il percorso della directory di avvio offline.

**Windows XP:** Non supportato.

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR
</dt> <dd>

Usare questa opzione per le riparazione offline. Specificare il percorso della directory Windows offline.

**Windows XP:** Non supportato.

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE
</dt> <dd>

Questo valore non è supportato.

**Windows Server 2003 e Windows XP:** Svuota la cache dei file e analizza tutti i file di sistema protetti.

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

<span id="_SCANNOW"></span><span id="_scannow"></span>/scannow
</dt> <dd>

Analizza immediatamente tutti i file di sistema protetti.

</dd> <dt>

<span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE
</dt> <dd>

Questo valore non è supportato.

**Windows Server 2003 e Windows XP:** Analizza tutti i file di sistema protetti al successivo avvio.

</dd> <dt>

<span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE
</dt> <dd>

Verifica il file nel percorso completo specificato. Questa opzione non ripristina il file.

**Windows XP:** Non supportato.

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY
</dt> <dd>

Analizza tutti i file di sistema protetti, ma non ripristina i file.

**Windows XP:** Non supportato.

</dd> </dl>

Sfc imposta il valore del Registro di sistema seguente:

 = HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon \\ SFCScan

Per altre informazioni, vedere [Valori del Registro di sistema WFP.](wfp-registry-values.md)

## <a name="remarks"></a>Commenti

Solo Windows Vista è possibile impostare la variabile di ambiente **\_ \_ LOGFILE** DI TRACCIA DI WINDOWS sul percorso di una directory valida per ricevere un file di log.

## <a name="examples"></a>Esempio

Le righe di comando di esempio seguenti sono esempi di sfc.exe sintassi.

**sfc /SCANNOW**

**sfc /VERIFYFILE=c: \\ windows \\ system32 \\kernel32.dll**

**sfc /SCANFILE=d: \\ windows \\ system32 \\kernel32.dll /OFFBOOTDIR=d: \\ /OFFWINDIR=d: \\ windows**

**sfc /VERIFYONLY /FILESONLY**

 

 



