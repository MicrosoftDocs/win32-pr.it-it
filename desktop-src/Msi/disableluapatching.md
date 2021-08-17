---
description: Se questo criterio di sistema per computer è impostato su &\# 0034;1&0034;, il programma di installazione impedisce agli utenti non amministratori di usare l'applicazione di patch controllo dell'account utente per qualsiasi applicazione installata \# nel computer.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821eb480ac09a2fc0416d7b3a54c0df5699a7096b45e56a843afe691886296f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637778"
---
# <a name="disableluapatching"></a>DisableLUAPatching

Se questo criterio di sistema per computer è impostato su "1", il programma di installazione impedisce agli utenti non amministratori di usare l'applicazione di [patch](user-account-control--uac--patching.md) di Controllo dell'account utente per qualsiasi applicazione installata nel computer. Quando i criteri di sistema per computer non sono impostati o impostati su 0, gli utenti non amministratori possono applicare patch utente con privilegi minimi alle applicazioni abilitate per l'applicazione di patch agli account utente con privilegi minimi.

Usare la [**proprietà MSIDISABLELUAPATCHING**](msidisableluapatching.md) per impedire l'applicazione di patch con privilegi minimi di un'applicazione.

Il criterio DisableLUAPatching è disponibile a partire da Windows Installer versione 3.0.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del** \\ **computer** \\ **locale Programma** di installazione \\  \\ **Windows** \\ **Microsoft**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



