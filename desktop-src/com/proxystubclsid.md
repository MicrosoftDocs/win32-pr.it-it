---
title: ProxyStubClsid
description: Mappe un IID a un CLSID nelle DLL proxy a 16 bit.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Valore del Registro di sistema ProxyStubClsid COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f86db768979a72d2d2f0b8c7a137d6b105f4a52d082ec50c6e78ba271fbca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129993"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

Mappe un IID a un CLSID nelle DLL proxy a 16 bit.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Commenti

Si tratta di **un \_ valore REG SZ** che specifica il CLSID per l'IID.

Se si aggiungono interfacce, è necessario usare questa voce per registrarle (sistemi a 16 bit) in modo che OLE possa trovare il codice remoto appropriato per stabilire la comunicazione interprocesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




