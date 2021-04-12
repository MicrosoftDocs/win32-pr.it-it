---
title: ServiceParameters
description: Specifica i parametri della riga di comando da passare a un oggetto installato per l'uso da parte di COM tramite il valore del registro di sistema LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Valore ServiceParameters del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330164"
---
# <a name="serviceparameters"></a>ServiceParameters

Specifica i parametri della riga di comando da passare a un oggetto installato per l'uso da parte di COM tramite il valore del registro di sistema [**LocalService**](localservice.md) .

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** . Questa stringa viene passata al servizio come argomento della riga di comando mentre viene avviata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**LocalService**](localservice.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> </dl>

 

 




