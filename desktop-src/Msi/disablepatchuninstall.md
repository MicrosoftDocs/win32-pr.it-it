---
description: Se il criterio di sistema per computer è impostato su 1, le patch non possono essere rimosse dal computer da un utente o da un amministratore.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879686"
---
# <a name="disablepatchuninstall"></a>DisablePatchUninstall

Se il [criterio di sistema](system-policy.md) per computer è impostato su 1, le patch non possono essere rimosse dal computer da un utente o da un amministratore. Il Windows Installer può comunque rimuovere una patch che non è più applicabile a un prodotto. Se questo criterio non è impostato, un utente può rimuovere una patch dal computer solo se l'utente dispone dei privilegi necessari per rimuovere la patch. Questo può dipendere dal fatto che l'utente sia un amministratore, che siano impostate le impostazioni dei criteri [DisableMsi](disablemsi.md) e [AlwaysInstallElevated](alwaysinstallelevated.md) e che la patch sia stata installata in un contesto gestito per utente, per utente non gestito o per computer.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



