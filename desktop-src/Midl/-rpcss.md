---
title: opzione/RPCSS
description: L'opzione/RPCSS, se specificata, funge da se l' \_ attributo Enable allocate è stato specificato in tutte le operazioni dell'interfaccia. L'utilizzo di questo attributo non è consigliato.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- /RPCSS switch MIDL
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045590"
---
# <a name="rpcss-switch"></a>opzione/RPCSS

L'opzione **/RPCSS** , se specificata, funge da se l'attributo [**enable \_ allocate**](enable-allocate.md) è stato specificato in tutte le operazioni dell'interfaccia. L'utilizzo di questo attributo non è consigliato.

``` syntax
midl /rpcss
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

In modalità predefinita, il pacchetto RpcSs è abilitato solo se la procedura o l'interfaccia ha l'attributo [**enable \_ allocate**](enable-allocate.md) o l'opzione **/RPCSS** è specificata nella riga di comando. In modalità **/OSF** , lo stub sul lato server Abilita il pacchetto di allocazione RPCSS.

## <a name="examples"></a>Esempio

**MIDL/RPCSS nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Abilita \_ allocazione**](enable-allocate.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




