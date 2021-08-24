---
description: Per mantenere un'installazione sicura del software nei computer bloccati, attenersi a queste linee guida quando si crea il pacchetto Windows installer.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Protezione dei pacchetti nei computer bloccati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bcdb2770e165a8b0d99fbc2088ec4c3b113e5befa180a7d6d2598eee866a5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315301"
---
# <a name="securing-packages-on-locked-down-computers"></a>Protezione dei pacchetti nei computer bloccati

L'aderenza alle linee guida seguenti quando si crea un pacchetto Windows Installer che verrà usato nei computer bloccati consente di mantenere un ambiente sicuro durante l'installazione:

-   Testare il pacchetto per verificare la compatibilità con i Windows di sistema del computer del programma [di installazione.](system-policy.md)
-   Assicurarsi che il pacchetto venga eseguito con tutti [i livelli dell'interfaccia](user-interface-levels.md)utente , nessuno, basic, limitato e completo.
-   Testare il pacchetto in partizioni NTFS, sia [*con*](e-gly.md) privilegi elevati che con privilegi non elevati.
-   A partire da Windows Installer 3.0, l'applicazione di patch al controllo [dell'account](user-account-control--uac--patching.md) utente consente agli utenti non amministratori di applicare patch alle applicazioni installate nel contesto per computer. Testare il pacchetto di patch in Windows Vista e Windows XP per l'installazione da parte di utenti con accesso amministratore e da utenti non amministratori.

 

 



