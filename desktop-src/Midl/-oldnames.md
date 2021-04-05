---
title: opzione/OLDNAMES
description: L'opzione/OLDNAMES indica al compilatore MIDL di generare nomi di interfaccia che non includono il numero di versione.
ms.assetid: 3a79c399-e115-46fd-9559-681b85cd872d
keywords:
- /OLDNAMES switch MIDL
topic_type:
- apiref
api_name:
- /oldnames
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cf861d2bf4f4123d7a1ee103e6966e5d404946
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725447"
---
# <a name="oldnames-switch"></a>opzione/OLDNAMES

L'opzione **/oldnames** indica al compilatore MIDL di generare nomi di interfaccia che non includono il numero di versione.

``` syntax
midl /oldnames
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Il compilatore MIDL incorpora il numero di versione dell'interfaccia nel nome dell'interfaccia generato nello stub, ad esempio iface \_ V1 \_ 0 \_ ServerIfHandle. Questo formato di denominazione è coerente con il formato usato dal compilatore IDL OSF DCE. Tuttavia, differisce dal formato di denominazione usato dal compilatore MIDL 1,0. Il compilatore MIDL 1,0 non include i numeri di versione nei nomi di interfaccia (ad esempio, iface \_ ServerIfHandle). L'opzione **/oldnames** consente di indicare al compilatore MIDL di generare nomi di interfaccia che non includono il numero di versione. In questo modo, il formato è coerente con i nomi generati dal compilatore MIDL 1,0.

Se il codice dell'applicazione server è stato scritto per l'uso con uno stub generato dal compilatore MIDL 1,0 e si riferisce al nome dell'interfaccia generata da MIDL (ad esempio, in una chiamata a [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)), è necessario modificarlo in modo che faccia riferimento allo stile del nome di interfaccia supportato dalla versione 2,0 o successiva del compilatore MIDL. In alternativa, è possibile usare l'opzione **/oldnames** quando si richiama il compilatore MIDL.

## <a name="examples"></a>Esempio

**MIDL/OLDNAMES nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 