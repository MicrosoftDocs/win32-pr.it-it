---
title: Autotreats
description: Imposta automaticamente il CLSID per la chiave Treats sul valore specificato.
ms.assetid: 5adf7bc5-a4d6-444d-bd56-0c4e6eee5111
keywords:
- Chiave del registro di sistema autotreats COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9ff717e17f08e5d37885f3994d03671bddaa9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395238"
---
# <a name="autotreatas"></a>Autotreats

Imposta automaticamente il CLSID per la chiave [**Treats**](treatas.md) sul valore specificato.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoTreatAs = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** che specifica l'identificatore di classe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CoTreatAsClass**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




