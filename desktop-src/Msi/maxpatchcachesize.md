---
description: Se questo criterio di sistema per computer è impostato su un valore maggiore di 0, Windows Installer Salva le versioni precedenti dei file in una cache quando viene applicata una patch a un'applicazione.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485261"
---
# <a name="maxpatchcachesize"></a>MaxPatchCacheSize

Se questo [criterio di sistema](system-policy.md) per computer è impostato su un valore maggiore di 0, Windows Installer Salva le versioni precedenti dei file in una cache quando viene applicata una patch a un'applicazione. La memorizzazione nella cache può migliorare le prestazioni delle installazioni future che altrimenti dovranno ottenere i vecchi file da un'origine applicazione originale.

Il valore del criterio MaxPatchCacheSize è la percentuale massima di spazio su disco che il programma di installazione può utilizzare per la cache dei file obsoleti. Ad esempio, un valore pari a 20 indica che non viene utilizzato più del 20%. Se la dimensione totale della cache raggiunge la percentuale di spazio su disco specificata, nessun file aggiuntivo viene salvato nella cache. Il criterio non influisce sui file che sono già stati salvati.

Se il valore del criterio MaxPatchCacheSize è impostato su 0, non viene salvato alcun file aggiuntivo.

Se il criterio MaxPatchCacheSize non è impostato, il valore predefinito è 10 e un massimo del 10% dello spazio su disco può essere utilizzato per salvare i file obsoleti.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



