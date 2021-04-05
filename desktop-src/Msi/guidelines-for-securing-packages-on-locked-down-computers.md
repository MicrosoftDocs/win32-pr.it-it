---
description: Per mantenere un'installazione software protetta nei computer bloccati, attenersi a queste linee guida quando si crea il pacchetto di Windows Installer.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Protezione dei pacchetti nei computer bloccati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8380ad7e342d35bff80da4d4d86c37759a80a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882958"
---
# <a name="securing-packages-on-locked-down-computers"></a>Protezione dei pacchetti nei computer bloccati

Rispetto alle linee guida seguenti quando si crea un pacchetto di Windows Installer che verrà usato nei computer bloccati consente di mantenere un ambiente protetto durante l'installazione:

-   Testare il pacchetto per la compatibilità con i [criteri di sistema](system-policy.md)del computer Windows Installer.
-   Assicurarsi di eseguire il pacchetto con tutti i [livelli di interfaccia utente](user-interface-levels.md), nessuno, Basic, Limited e Full.
-   Testare il pacchetto in partizioni NTFS, con privilegi [*elevati*](e-gly.md) e non elevati.
-   A partire da Windows Installer 3,0, il [controllo dell'account utente (UAC)](user-account-control--uac--patching.md) consente agli utenti non amministratori di applicare patch alle applicazioni installate nel contesto per computer. Testare il pacchetto di patch in Windows Vista e Windows XP per l'installazione da parte di utenti con accesso amministratore e da utenti non amministratori.

 

 



