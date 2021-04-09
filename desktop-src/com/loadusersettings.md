---
title: LoadUserSettings
description: Determina se COM caricherà il profilo utente per i server COM in esecuzione come identità dell'applicazione di avvio dell'utente.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- Valore LoadUserSettings del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e14282b00bc2c2d9b989e19480047f115623d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955666"
---
# <a name="loadusersettings"></a>LoadUserSettings

Determina se COM caricherà il profilo utente per i server COM in esecuzione come identità dell'applicazione di avvio dell'utente.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** . Se il *valore* è diverso da zero, com carica il profilo dell'account utente con il quale avvia il server com. Se il *valore* è zero o non è presente, com non caricherà il profilo dell'account utente con cui viene avviato il server com.

Questa impostazione viene ignorata se è presente una voce [**RunAs**](runas.md) .

 

 




