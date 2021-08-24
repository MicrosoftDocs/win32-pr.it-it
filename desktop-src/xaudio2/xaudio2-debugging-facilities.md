---
description: La versione di debug del motore XAudio2 convalida i parametri e fornisce messaggi di avviso e di errore dettagliati.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Funzionalità di debug di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc6a89bb298a2e836e4d8dc63ed0144b9a789950432c5c83f33ec7ad86f4de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706991"
---
# <a name="xaudio2-debugging-facilities"></a>Funzionalità di debug di XAudio2

La versione di debug del motore XAudio2 convalida i parametri e fornisce messaggi di avviso e di errore dettagliati.

## <a name="setting-the-debug-logging-level-at-run-time"></a>Impostazione del livello di registrazione di debug in fase di esecuzione

È possibile impostare il livello di informazioni di debug visualizzate da XAudio2 in qualsiasi momento compilando una struttura [**XAUDIO2 \_ DEBUG \_ CONFIGURATION**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) con i flag per il livello di registrazione desiderato e quindi passare la struttura al metodo [**IXAudio2::SetDebugConfiguration.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) I valori passati al **metodo IXAudio2::SetDebugConfiguration** eseguono sempre l'override di tutti i valori predefiniti impostati nel Registro Windows sistema.

## <a name="debug-support"></a>Supporto per il debug

Le funzionalità di debug sono sempre disponibili per XAUDIO2 in Windows 8.

Per le versioni directx SDK di XAUDIO2, è necessario usare **XAUDIO2 \_ DEBUG \_ ENGINE** quando si crea l'oggetto XAUDIO2 con [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) e il sistema deve avere installato DirectX SDK Developer Runtime per il supporto del debug.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di debug](debugging-facilities.md)
</dt> <dt>

[Guida di riferimento alla programmazione di XAudio2](programming-reference.md)
</dt> </dl>

 

 
