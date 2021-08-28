---
title: LoadUserSettings
description: Determina se COM carica il profilo utente per i server COM in esecuzione come identità dell'applicazione utente di avvio.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- Valore del Registro di sistema LoadUserSettings COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b82bd89015baa4c73c9200013e49c76523951218dfde62bbe39300eefdfe0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731041"
---
# <a name="loadusersettings"></a>LoadUserSettings

Determina se COM carica il profilo utente per i server COM in esecuzione come identità dell'applicazione utente di avvio.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.** Se *il* valore è diverso da zero, COM carica il profilo dell'account utente con cui avvia il server COM. Se *il* valore è zero o non è presente, COM non carica il profilo dell'account utente con cui avvia il server COM.

Questa impostazione viene ignorata se è presente una voce [**RunAs.**](runas.md)

 

 




