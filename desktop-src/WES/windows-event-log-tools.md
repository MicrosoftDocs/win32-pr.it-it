---
title: Strumenti del registro eventi di Windows
description: Nel registro eventi di Windows sono disponibili gli strumenti seguenti per la compilazione del provider.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104398803"
---
# <a name="windows-event-log-tools"></a>Strumenti del registro eventi di Windows

Nel registro eventi di Windows sono disponibili gli strumenti seguenti per la compilazione del provider.



| Strumento                                                           | Descrizione                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md)  | Utilità della riga di comando utilizzata per compilare manifesti di strumentazione e file di testo del messaggio. |
| WevtUtil.exe                                                   | Utilità della riga di comando utilizzata principalmente per registrare il provider nel computer. È inoltre possibile utilizzarlo per ottenere informazioni sui metadati sul provider, i relativi eventi e i canali in cui vengono registrati gli eventi e per eseguire query sugli eventi da un canale o un file di log. Lo strumento WevtUtil.exe è incluso in% windir% \\ system32. Per informazioni sull'utilizzo, immettere "wevtutil/?" al prompt dei comandi.<br/> Questo comando è limitato ai membri del gruppo Administrators e deve essere eseguito con privilegi elevati.|
