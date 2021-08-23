---
description: Questi criteri di sistema per computer possono essere usati per specificare che il programma di installazione di Windows passi tutte le proprietà pubbliche sul lato server durante un'installazione gestita usando privilegi elevati.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d8c56b1ea4d161030b252141e1930bd8298cea98b52b09511175d132e6a2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637007"
---
# <a name="enableusercontrol"></a>EnableUserControl

Nel caso di un'installazione gestita, l'autore del pacchetto potrebbe dover limitare le proprietà pubbliche che vengono passate al lato server e possono essere modificate da un utente che non è un amministratore di sistema. Alcune restrizioni sono in genere necessarie per mantenere un ambiente sicuro quando l'installazione richiede che il programma di installazione usi privilegi elevati.

Se questo criterio di [sistema](system-policy.md) per computer è impostato su "1", il programma di installazione può passare tutte le proprietà pubbliche sul lato server durante un'installazione gestita usando privilegi elevati. [](public-properties.md) L'impostazione di questo criterio ha lo stesso effetto dell'impostazione **della proprietà EnableUserControl.** L'impostazione di questo criterio consente di passare tutte le proprietà pubbliche al servizio e di essere modificabili dagli utenti non amministratori. Per impostazione predefinita, questo criterio non è abilitato. solo le proprietà pubbliche con restrizioni vengono passate al lato server e modificabili da un utente non amministrativo. Tutte le altre proprietà pubbliche vengono ignorate.

Se il sistema operativo è Windows 2000, l'utente non è un amministratore di sistema e l'applicazione o il prodotto viene installato con privilegi elevati, un utente che non è un amministratore di sistema può eseguire l'override solo di un elenco approvato di proprietà pubbliche con restrizioni. Per altre informazioni, vedere [Proprietà pubbliche con restrizioni.](restricted-public-properties.md)

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del** \\ **computer** \\ **locale Programma** di installazione \\  \\ **Windows** \\ **Microsoft**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



