---
title: ProxyStubClsid32
description: Esegue il mapping di un IID a un CLSID in DLL proxy a 32 bit.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- Valore ProxyStubClsid32 del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339367"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Esegue il mapping di un IID a un CLSID in DLL proxy a 32 bit.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** che specifica il CLSID per l'IID.

Si tratta di una voce obbligatoria perché il mapping da IID a CLSID può essere diverso per le interfacce a 16 bit e a 32 bit. Il mapping da IID a CLSID dipende dal modo in cui i proxy di interfaccia vengono inseriti in un set di DLL proxy.

Se si aggiungono interfacce, è necessario utilizzare questa voce per registrarle (sistemi a 32 bit) in modo che OLE possa trovare il codice remoto appropriato per stabilire la comunicazione interprocesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Interfaccia**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid**](proxystubclsid.md)
</dt> </dl>

 

 