---
description: HKLM \\ software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable.
ms.assetid: 68ba8219-7ed2-44a9-9fd5-f6dfa57891c0
title: CEIPEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7b86a726af95e7ec9fb764d5e752057a24b3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225617"
---
# <a name="ceipenable"></a>CEIPEnable

**HKLM \\ software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**



| Tipo di dati  | Range                     | Valore predefinito |
|------------|---------------------------|---------------|
| REG \_ DWORD | 0 (Disabilita) o 1 (Abilita) | 0             |



 

## <a name="description"></a>Descrizione

Abilita il programma Analisi utilizzo software Windows.

## <a name="change-method"></a>Cambia metodo

Per modificare il valore di questa voce, nel pannello di controllo selezionare **sistema e manutenzione**, quindi **segnalazioni di problemi e soluzioni**. Fare clic su **Impostazioni analisi utilizzo** software nella sezione vedere anche.

## <a name="activation-method"></a>Metodo di attivazione

Le modifiche apportate a questa voce sono effettive immediatamente. L'abilitazione di questa chiave del registro di sistema causa l'abilitazione di Windows Analisi utilizzo software per l'intero computer. La disabilitazione di questa chiave del registro di sistema causa la disabilitazione di Windows Analisi utilizzo software per l'intero computer.

Questa voce può essere sostituita da un'impostazione di Criteri di gruppo nei sistemi che supportano Criteri di gruppo. Mentre l'impostazione Abilita Criteri di gruppo di Windows Analisi utilizzo software analisi utilizzo software è abilitata, il sistema ignora questa voce. La configurazione di questa impostazione dei criteri è archiviata nella sezione **criteri** in **HKLM \\ software \\ Policies \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**.

 

 



