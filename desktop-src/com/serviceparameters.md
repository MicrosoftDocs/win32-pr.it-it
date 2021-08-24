---
title: ServiceParameters
description: Specifica i parametri della riga di comando da passare a un oggetto installato per l'uso da parte di COM tramite il valore del Registro di sistema LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Valore del Registro di sistema ServiceParameters COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103b55269b700beaf5c85e3408e3597e63fb9140e4dc79fe4bb895ff6767bfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129963"
---
# <a name="serviceparameters"></a>ServiceParameters

Specifica i parametri della riga di comando da passare a un oggetto installato per l'uso da parte di COM tramite il valore del Registro di sistema [**LocalService.**](localservice.md)

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ REG SZ.** Questa stringa viene passata al servizio come argomento della riga di comando durante l'avvio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**LocalService**](localservice.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> </dl>

 

 




