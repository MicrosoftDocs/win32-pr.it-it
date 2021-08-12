---
title: Voci del Registro di sistema per tenere traccia dello stato dell'installazione
description: Voci del Registro di sistema per tenere traccia dello stato dell'installazione
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player,monitoraggio dello stato dell'installazione
- Windows Media Player,verifica dello stato dell'installazione
- Windows Media Player,verifica dello stato di avanzamento delle installazioni
- Windows Media Player,registro
- Registro di sistema, rilevamento dello stato dell'installazione
- Registro di sistema, rilevamento dello stato di avanzamento dell'installazione
- Registro di sistema, rilevamento dello stato di avanzamento delle installazioni
- Registro di sistema, impostazioni per Windows Media Player
- rilevamento dello stato di avanzamento dell'installazione
- installazione del rilevamento dello stato
- rilevamento dello stato di avanzamento delle installazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7febb9f25a04c5e4358e891f963ab6a8569cfd6facef7e4f2072807bd09e2605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570302"
---
# <a name="registry-entries-for-tracking-installation-progress"></a>Voci del Registro di sistema per tenere traccia dello stato dell'installazione

Il programma di installazione di Windows Media Player 11, setupwm.exe, scrive le voci seguenti nel Registro di sistema in modo che i programmi di installazione possano tenere traccia dello stato di avanzamento del programma di installazione di Windows Media Player durante \_ l'esecuzione.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



Nella sintassi del Registro di sistema precedente *value* è un segnaposto per un valore integer.

Progress \_ CurrentDialog indica quale finestra di dialogo Windows Media Player'installazione è attualmente visualizzata. Progress MaxDialog indica il numero totale di finestre di dialogo \_ che Windows media. Ad esempio, se Progress \_ CurrentDialog = 2 e Progress MaxDialog = 5, Windows Media Player visualizza attualmente la seconda finestra di dialogo in una sequenza \_ di cinque.

Progress \_ CurrentInstall e Progress \_ MaxInstall, insieme, indicano la percentuale di completamento della finestra di dialogo corrente. Ad esempio, se Progress CurrentInstall = 6 e Progress MaxInstall = 25, la finestra di dialogo corrente è \_ \_ completata 6/25 (ovvero il 24%).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Registro di sistema Impostazioni**](registry-settings.md)
</dt> </dl>

 

 




