---
description: Questo criterio di sistema per computer può essere usato per specificare che il Windows Installer passare tutte le proprietà pubbliche al lato server durante un'installazione gestita usando privilegi elevati.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130686"
---
# <a name="enableusercontrol"></a>EnableUserControl

Nel caso di un'installazione gestita, l'autore del pacchetto potrebbe dover limitare le proprietà pubbliche che vengono passate al lato server e possono essere modificate da un utente che non è un amministratore di sistema. Alcune restrizioni sono in genere necessarie per mantenere un ambiente protetto quando l'installazione richiede che il programma di installazione utilizzi privilegi elevati.

Se il [criterio di sistema](system-policy.md) per computer è impostato su "1", il programma di installazione può passare tutte le [proprietà pubbliche](public-properties.md) al lato server durante un'installazione gestita utilizzando privilegi elevati. L'impostazione di questo criterio ha lo stesso effetto dell'impostazione della proprietà **EnableUserControl** . L'impostazione di questo criterio consente di passare tutte le proprietà pubbliche al servizio e di modificarle dagli utenti non amministrativi. Per impostazione predefinita, questo criterio non è abilitato. solo le proprietà pubbliche con restrizioni vengono passate al lato server e possono essere modificate da un utente non amministratore. Tutte le altre proprietà pubbliche vengono ignorate.

Se il sistema operativo è Windows 2000, l'utente non è un amministratore di sistema e l'applicazione o il prodotto viene installato con privilegi elevati, un utente che non è un amministratore di sistema può solo eseguire l'override di un elenco approvato di proprietà pubbliche limitate. Per ulteriori informazioni, vedere [proprietà pubbliche limitate](restricted-public-properties.md).

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



