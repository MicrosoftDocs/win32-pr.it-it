---
title: /ms_ext opzione
description: A partire da MIDL versione 3,0, le funzionalità abilitate dall' \_ opzione MS EXT sono ora la modalità predefinita per il compilatore MIDL.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext switch MIDL
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046600"
---
# <a name="ms_ext-switch"></a>\_Switch EXT/MS

A partire da MIDL versione 3,0, le funzionalità abilitate dall'opzione **MS \_ ext** sono ora la modalità predefinita per il compilatore MIDL.

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Se si usa l'opzione, non verrà generato un errore del compilatore, pertanto non è necessario rimuovere i riferimenti a **/MS \_ ext** o [**/c \_ ext**](-c-ext.md) da un makefile esistente.

Le estensioni Microsoft seguenti per OSF DCE sono ora disponibili per impostazione predefinita:

-   Definizioni di interfaccia per gli oggetti OLE. Per ulteriori informazioni sui file generati per le interfacce OLE, vedere [file generati per un'interfaccia com](files-generated-for-a-com-interface.md) .
-   Un attributo di [**\[ callback \]**](callback.md) che specifica una funzione di callback statica sul client
-   [**\_ virgolette cpp**](cpp-quote.md)(*\_ stringa tra virgolette*) e [**\# pragma MIDL \_ echo**](pragma.md)
-   tipi di caratteri wide, costanti e stringhe [**WCHAR \_ t**](wchar-t.md)
-   [**inizializzazione enum**](enum.md) (enumeratori sparse)
-   Espressioni come identificatori di dimensioni e discriminatori
-   [Gestisci estensioni](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [Puntatore-ereditarietà del tipo di attributo](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [Interfacce multiple](/windows/desktop/Rpc/registering-interfaces)
-   Definizioni all'esterno del blocco Interface
-   È possibile omettere [gli attributi direzionali](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**in**](in.md), [**out**](out-idl.md)\]

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[Puntatore-ereditarietà del tipo di attributo](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**configurazione di/app \_**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 