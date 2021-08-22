---
description: Se questo criterio di sistema per computer non è impostato, solo gli amministratori possono applicare patch ai prodotti esistenti installati con privilegi elevati.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c827b23f8beecf02d3312358d7ece6b835619111428349850f4e597ce379cd53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145904"
---
# <a name="allowlockdownpatch"></a>AllowLockdownPatch

Se questo criterio di [sistema](system-policy.md) per computer non è impostato, solo gli amministratori possono applicare patch ai prodotti esistenti installati con privilegi elevati. Se AllowLockdownPatch è impostato su "1", gli utenti non amministratori possono, in alcuni casi, applicare patch ai prodotti durante l'esecuzione di un'installazione con privilegi elevati. Con il criterio impostato, [](minor-upgrades.md) la patch può installare aggiornamenti secondari durante l'esecuzione di un'installazione con privilegi elevati, la patch non può installare [gli aggiornamenti principali](major-upgrades.md). L'impostazione di questo criterio consente anche agli utenti non amministratori di eseguire programmi con privilegi LocalSystem durante un'installazione con privilegi elevati.

L'impostazione predefinita è consigliata per garantire un ambiente sicuro.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del computer** \\  \\ **locale** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

Qualsiasi utente può applicare una patch durante un'installazione non elevata. L'impostazione di [](system-policy.md) questo criterio di sistema per computer su "1" offre agli utenti non amministratori la flessibilità aggiuntiva di applicare patch a qualsiasi prodotto durante un'installazione con privilegi elevati. Se questo criterio non è impostato, gli utenti non amministratori non possono applicare una patch alle applicazioni assegnate o pubblicate.

L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi arbitrari con privilegi LocalSystem se dispongono di un pacchetto patch del programma di installazione di Windows che installa o avvia tali programmi.

 

 



