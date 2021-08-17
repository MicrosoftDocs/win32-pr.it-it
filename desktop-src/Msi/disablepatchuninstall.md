---
description: Se questo criterio di sistema per computer è impostato su 1, le patch non possono essere rimosse dal computer da un utente o un amministratore.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5531d5afd7fa98883a3e07dc7c47db625db9051fa223ea7cd6f70e4ceb5aee03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378569"
---
# <a name="disablepatchuninstall"></a>DisablePatchUninstall

Se questo criterio di [sistema](system-policy.md) per computer è impostato su 1, le patch non possono essere rimosse dal computer da un utente o un amministratore. Il Windows installer può comunque rimuovere una patch che non è più applicabile a un prodotto. Se questo criterio non è impostato, un utente può rimuovere una patch dal computer solo se all'utente sono stati concessi privilegi per rimuovere la patch. Ciò può dipendere dal fatto che l'utente sia un amministratore, se le impostazioni dei criteri [DisableMsi](disablemsi.md) e [AlwaysInstallElevated](alwaysinstallelevated.md) siano impostate e se la patch è stata installata in un contesto gestito per utente, per utente non gestito o per computer.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software di LOCAL MACHINE** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



