---
description: La versione di debug del motore XAudio2 convalida i parametri e fornisce messaggi di avviso e di errore dettagliati.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Funzionalità di debug XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752410"
---
# <a name="xaudio2-debugging-facilities"></a>Funzionalità di debug XAudio2

La versione di debug del motore XAudio2 convalida i parametri e fornisce messaggi di avviso e di errore dettagliati.

## <a name="setting-the-debug-logging-level-at-run-time"></a>Impostazione del livello di registrazione del debug in fase di esecuzione

È possibile impostare il livello di informazioni di debug visualizzate da XAudio2 in qualsiasi momento compilando una struttura di [**\_ \_ configurazione di debug XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) con i flag per il livello di registrazione desiderato, quindi passare la struttura al metodo [**IXAudio2:: SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) . I valori passati al metodo **IXAudio2:: SetDebugConfiguration** eseguono sempre l'override dei valori predefiniti impostati nel registro di sistema di Windows.

## <a name="debug-support"></a>Supporto per il debug

Le funzionalità di debug sono sempre disponibili per XAUDIO2 in Windows 8.

Per le versioni di DirectX SDK di XAUDIO2, è necessario usare il **\_ \_ motore di debug di XAUDIO2** quando si crea l'oggetto XAUDIO2 con [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) e il sistema deve disporre del runtime di DirectX SDK Developer installato per supportare il debug.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di debug](debugging-facilities.md)
</dt> <dt>

[Guida di riferimento alla programmazione di XAudio2](programming-reference.md)
</dt> </dl>

 

 
