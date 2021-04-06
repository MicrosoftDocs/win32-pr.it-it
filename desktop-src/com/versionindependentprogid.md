---
title: VersionIndependentProgID
description: Associa un ProgID a un CLSID. Questo valore viene utilizzato per determinare la versione più recente di un'applicazione dell'oggetto.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- VersionIndependentProgID chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045361"
---
# <a name="versionindependentprogid"></a>VersionIndependentProgID

Associa un ProgID a un CLSID. Questo valore viene utilizzato per determinare la versione più recente di un'applicazione dell'oggetto.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** che specifica la versione più recente dell'applicazione dell'oggetto.

Il ProgID indipendente dalla versione viene archiviato e gestito esclusivamente dal codice dell'applicazione. Quando viene specificato il ProgID indipendente dalla versione, la funzione [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) restituisce il CLSID della versione corrente.

È possibile usare [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) per eseguire la conversione tra queste due rappresentazioni.

 

 




