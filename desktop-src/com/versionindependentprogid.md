---
title: VersionIndependentProgID
description: Associa un ProgID a un CLSID. Questo valore viene usato per determinare la versione più recente di un'applicazione oggetto.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- VersionIndependentProgID chiave del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe1defaa52df5251d6c021655d6e84c90677e2a2d57f0bfb67f925e0ffa5bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549718"
---
# <a name="versionindependentprogid"></a>VersionIndependentProgID

Associa un ProgID a un CLSID. Questo valore viene usato per determinare la versione più recente di un'applicazione oggetto.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ REG SZ** che specifica la versione più recente dell'applicazione dell'oggetto.

Il ProgID indipendente dalla versione viene archiviato e gestito esclusivamente dal codice dell'applicazione. Quando viene specificato il ProgID indipendente dalla versione, la [**funzione CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) restituisce il CLSID della versione corrente.

È possibile usare [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) per eseguire la conversione tra queste due rappresentazioni.

 

 




