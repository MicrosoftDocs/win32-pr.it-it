---
title: RemoteServerName
description: Configura il client per richiedere l'esecuzione dell'oggetto in un computer specifico ogni volta che viene chiamata una funzione di attivazione per cui non è specificata una struttura COSERVERINFO.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- Valore del Registro di sistema RemoteServerName COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0204b63e6b8d74eabd4f9e01f36aeea0deea9220a2d0ffacaa46f09d0d625426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104515"
---
# <a name="remoteservername"></a>RemoteServerName

Configura il client per richiedere l'esecuzione dell'oggetto in un computer specifico ogni volta che viene chiamata una funzione di attivazione per cui non è specificata una struttura [**COSERVERINFO.**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a>Commenti

**RemoteServerName consente** una semplice gestione della configurazione delle applicazioni client. possono essere scritti senza nomi di server hard-coded e possono essere configurati modificando i valori del Registro di sistema **RemoteServerName** delle classi di oggetti che usano.

Come descritto nella documentazione relativa [**all'enumerazione CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) e alla struttura [**COSERVERINFO,**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) uno dei parametri dell'attivazione COM distribuita è un puntatore a **una struttura COSERVERINFO.** Quando questo valore non è **NULL,** le informazioni nella **struttura COSERVERINFO** eseguono l'override dell'impostazione della chiave **RemoteServerName** per la chiamata di funzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> </dl>

 

 