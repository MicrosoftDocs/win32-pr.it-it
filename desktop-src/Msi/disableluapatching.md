---
description: Se il criterio di sistema per computer è impostato su &\# 0034; 1&\# 0034;, il programma di installazione impedisce agli utenti non amministratori di usare l'applicazione di patch per il controllo dell'account utente (UAC) per qualsiasi applicazione installata nel computer.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319969"
---
# <a name="disableluapatching"></a>DisableLUAPatching

Se il criterio di sistema per computer è impostato su "1", il programma di installazione impedisce agli utenti non amministratori di usare l'applicazione di patch per il [controllo dell'account utente (UAC)](user-account-control--uac--patching.md) per qualsiasi applicazione installata nel computer. Quando il criterio di sistema per computer non è impostato o è impostato su 0, gli utenti non amministratori possono applicare patch utente con privilegi minimi alle applicazioni abilitate per l'applicazione di patch a un account utente con privilegi minimi.

Utilizzare la proprietà [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) per impedire l'applicazione di patch con privilegi minimi.

Il criterio DisableLUAPatching è disponibile a partire dalla versione Windows Installer 3,0.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



