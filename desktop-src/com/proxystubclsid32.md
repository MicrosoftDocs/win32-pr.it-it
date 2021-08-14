---
title: ProxyStubClsid32
description: Mappe un IID a un CLSID nelle DLL proxy a 32 bit.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- Valore del Registro di sistema ProxyStubClsid32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9098ffc7771d3f900489292694ade462a2214e733294a1ed18e6ddb9817692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309897"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Mappe un IID a un CLSID nelle DLL proxy a 32 bit.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Commenti

Si tratta di **un \_ valore REG SZ** che specifica il CLSID per l'IID.

Si tratta di una voce obbligatoria perché il mapping da IID a CLSID può essere diverso per le interfacce a 16 bit e a 32 bit. Il mapping da IID a CLSID dipende dal modo in cui i proxy di interfaccia vengono suddivisi in un set di DLL proxy.

Se si aggiungono interfacce, è necessario utilizzare questa voce per registrarle (sistemi a 32 bit) in modo che OLE possa trovare il codice remoto appropriato per stabilire la comunicazione interprocesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Interfaccia**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid**](proxystubclsid.md)
</dt> </dl>

 

 