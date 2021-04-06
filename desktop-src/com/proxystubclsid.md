---
title: ProxyStubClsid
description: Esegue il mapping di un IID a un CLSID nelle DLL proxy a 16 bit.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Valore ProxyStubClsid del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045119"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

Esegue il mapping di un IID a un CLSID nelle DLL proxy a 16 bit.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** che specifica il CLSID per l'IID.

Se si aggiungono interfacce, è necessario utilizzare questa voce per registrarle (sistemi a 16 bit) in modo che OLE possa trovare il codice remoto appropriato per stabilire la comunicazione interprocesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




