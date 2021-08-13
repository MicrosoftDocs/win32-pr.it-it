---
title: Opzione /ms_ext
description: A causa di MIDL versione 3.0, le funzionalità abilitate dall'opzione ms ext sono ora la modalità \_ predefinita per il compilatore MIDL.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext l'opzione MIDL
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73bee998e96d26c0f5bb2a1e0f28446433681a7175ff181556ad7976c58af356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644560"
---
# <a name="ms_ext-switch"></a>Opzione /ms \_ ext

A causa di MIDL versione 3.0, le funzionalità abilitate dall'opzione **ms \_ ext** sono ora la modalità predefinita per il compilatore MIDL.

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>Opzioni di cambio

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

L'uso dell'opzione non genererà un errore del compilatore, pertanto non è necessario rimuovere i riferimenti a **/ms \_ ext** o [**/c \_ ext**](-c-ext.md) da un makefile esistente.

Le estensioni Microsoft seguenti per OSF DCE sono ora disponibili per impostazione predefinita:

-   Definizioni di interfaccia per gli oggetti OLE. Per altre informazioni sui file generati per le interfacce OLE, vedere [File generati per un'interfaccia COM](files-generated-for-a-com-interface.md)
-   Attributo [**\[ di callback \]**](callback.md) che specifica una funzione di callback statica nel client
-   [**Virgolette \_ cpp**](cpp-quote.md)(*stringa tra \_ virgolette*) e [**\# pragma midl \_ echo**](pragma.md)
-   [**wchar \_ t**](wchar-t.md) tipi di caratteri wide, costanti e stringhe
-   [**Inizializzazione dell'enumerazione**](enum.md) (enumeratori di tipo sparse)
-   Espressioni come identificatori di dimensioni e discriminanti
-   [Gestire le estensioni](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [Ereditarietà del tipo di attributo pointer](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [Più interfacce](/windows/desktop/Rpc/registering-interfaces)
-   Definizioni all'esterno del blocco di interfaccia
-   È possibile omettere [gli attributi direzionali](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**in**](in.md), [**out**](out-idl.md)\]

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[Ereditarietà del tipo di attributo pointer](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**/app \_ config**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 