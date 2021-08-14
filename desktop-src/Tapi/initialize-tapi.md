---
description: Nell'esempio di codice seguente viene illustrata la creazione dell'oggetto TAPI.
ms.assetid: f8566e53-51c9-4424-a8bb-369455f35706
title: Inizializzare TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6b354267bccffc96eed9f1e3457e41eeee9937bef73716768762db05bed67b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762528"
---
# <a name="initialize-tapi"></a>Inizializzare TAPI

Nell'esempio di codice seguente viene illustrata la creazione dell'oggetto TAPI.

```cpp
const auto result = ITTAPI::Initialize();

if (result != S_OK) {
    switch (result) {
        case S_FALSE: {
            std::cerr << "TAPI has already been initialized.\n";
        } break;

        [[fallthrough]]
        case E_OUTOFMEMORY: {
            std::cerr << "Insufficient memory exists to perform the operation.\n";
        }

        default: {
            // TODO: Handle unrecoverable error here
        }
    }
}
```

## <a name="see-also"></a>Vedere anche

- [ITTAPI::Initialize](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-initialize)
- [Valori HRESULT comuni](../seccrypto/common-hresult-values.md)
