---
description: Se questo criterio di sistema per computer non è impostato, solo gli amministratori possono applicare patch ai prodotti esistenti installati con privilegi elevati.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967292"
---
# <a name="allowlockdownpatch"></a>AllowLockdownPatch

Se questo [criterio di sistema](system-policy.md) per computer non è impostato, solo gli amministratori possono applicare patch ai prodotti esistenti installati con privilegi elevati. Se AllowLockdownPatch è impostato su "1", gli utenti non amministratori possono, in alcuni casi, applicare patch ai prodotti durante l'esecuzione di un'installazione con privilegi elevati. Con il set di criteri, la patch può installare [aggiornamenti secondari](minor-upgrades.md) durante l'esecuzione di un'installazione con privilegi elevati, la patch non può installare gli [aggiornamenti principali](major-upgrades.md). L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi con privilegi LocalSystem durante un'installazione con privilegi elevati.

L'impostazione predefinita è consigliata per garantire un ambiente protetto.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

Qualsiasi utente può applicare una patch durante un'installazione non con privilegi elevati. L'impostazione di questo [criterio di sistema](system-policy.md) per computer su "1" offre agli utenti non amministrativi la flessibilità aggiuntiva per l'applicazione di patch a qualsiasi prodotto durante un'installazione con privilegi elevati. Se questo criterio non è impostato, gli utenti non amministratori non possono applicare una patch alle applicazioni assegnate o pubblicate.

L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi arbitrari con privilegi LocalSystem se hanno un pacchetto Windows Installer patch che installa o avvia tali programmi.

 

 



