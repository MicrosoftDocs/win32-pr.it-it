---
description: Se questo criterio di sistema per computer è impostato su un valore maggiore di 0, il programma di installazione di Windows salva le versioni precedenti dei file in una cache quando viene applicata una patch a un'applicazione.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85291977073d1ab65c43ce9c4307e7c97519133330769e56c4b9dc7a883972dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013059"
---
# <a name="maxpatchcachesize"></a>MaxPatchCacheSize

Se questo criterio [](system-policy.md) di sistema per computer è impostato su un valore maggiore di 0, il programma di installazione di Windows salva le versioni precedenti dei file in una cache quando viene applicata una patch a un'applicazione. Caching aumentare le prestazioni delle installazioni future che altrimenti devono ottenere i file vecchi da un'origine dell'applicazione originale.

Il valore dei criteri MaxPatchCacheSize è la percentuale massima di spazio su disco che il programma di installazione può usare per la cache dei file vecchi. Ad esempio, un valore pari a 20 specifica che non deve essere usato più del 20%. Se le dimensioni totali della cache raggiungono la percentuale specificata di spazio su disco, non vengono salvati file aggiuntivi nella cache. I criteri non influiscono sui file che sono già stati salvati.

Se il valore del criterio MaxPatchCacheSize è impostato su 0, non vengono salvati file aggiuntivi.

Se il criterio MaxPatchCacheSize non è impostato, il valore predefinito è 10 e un massimo del 10% dello spazio su disco può essere usato per salvare i file vecchi.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software di LOCAL MACHINE** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



