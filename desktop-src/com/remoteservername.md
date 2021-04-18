---
title: RemoteServerName
description: Configura il client per richiedere che l'oggetto venga eseguito in un determinato computer ogni volta che viene chiamata una funzione di attivazione per la quale non è specificata una struttura COSERVERINFO.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- Valore RemoteServerName del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300552"
---
# <a name="remoteservername"></a>RemoteServerName

Configura il client per richiedere che l'oggetto venga eseguito in un determinato computer ogni volta che viene chiamata una funzione di attivazione per la quale non è specificata una struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) .

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a>Commenti

**RemoteServerName** consente una gestione semplificata della configurazione delle applicazioni client. possono essere scritti senza nomi di server hardcoded e possono essere configurati modificando i valori del registro di sistema **RemoteServerName** delle classi di oggetti usati.

Come descritto nella documentazione per l'enumerazione [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) e la struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , uno dei parametri dell'attivazione com distribuita è un puntatore a una struttura **COSERVERINFO** . Quando questo valore non è **null**, le informazioni nella struttura **COSERVERINFO** eseguono l'override dell'impostazione della chiave **RemoteServerName** per la chiamata di funzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> </dl>

 

 