---
title: Windows Strumenti del registro eventi
description: Windows Registro eventi offre gli strumenti seguenti che consentono di compilare il provider.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7a0aef85e85e096381b65d41458f1cb955ba9701452498d21c45ff25cb3058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587258"
---
# <a name="windows-event-log-tools"></a>Windows Strumenti del registro eventi

Windows Registro eventi offre gli strumenti seguenti che consentono di compilare il provider.



| Strumento                                                           | Descrizione                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md)  | Utilità della riga di comando utilizzata per compilare manifesti di strumentazione e file di testo dei messaggi. |
| WevtUtil.exe                                                   | Utilità della riga di comando usata principalmente per registrare il provider nel computer. È anche possibile usarlo per ottenere informazioni sui metadati sul provider, i relativi eventi e i canali in cui registra gli eventi e per eseguire query sugli eventi da un canale o da un file di log. Lo WevtUtil.exe è incluso in %windir% \\ System32. Per informazioni sull'utilizzo, immettere "wevtutil /?" al prompt dei comandi.<br/> Questo comando è limitato ai membri del gruppo Administrators e deve essere eseguito con privilegi elevati.|
