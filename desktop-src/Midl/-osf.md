---
title: opzione/OSF
description: L'opzione/OSF impone una rigida compatibilità con OSF DCE.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- /OSF switch MIDL
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046629"
---
# <a name="osf-switch"></a>opzione/OSF

L'opzione **/OSF** impone una rigida compatibilità con OSF DCE.

``` syntax
midl /osf
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Usare questa opzione se l'applicazione richiede una rigida compatibilità con OSF DCE per motivi di portabilità.

In modalità **/OSF** , il pacchetto RPCSS viene abilitato automaticamente quando si usano i puntatori completi, gli argomenti richiedono l'allocazione di memoria o quando si usa l'attributo [**enable \_ allocate**](enable-allocate.md) . Ciò significa che non è necessario fornire all'utente MIDL le funzioni [**\_ \_ gratuite**](/windows/desktop/Rpc/the-midl-user-free-function) per l' [**\_ \_ assegnazione dell'utente**](/windows/desktop/Rpc/the-midl-user-allocate-function) e l'utente MIDL nell'applicazione client e server.

Le funzionalità estese Microsoft seguenti non sono disponibili quando si esegue la compilazione con l'opzione **/OSF** :

-   Dichiaratori astratti (parametri senza nome) nel file IDL.
-   Definizioni di interfaccia per gli oggetti COM.
-   Nomi di interfaccia con più di 17 caratteri.
-   Attributi solo MIDL, ad esempio [**Wire \_ marshalling**](wire-marshal.md), [**User \_ Marshal**](user-marshal.md)e The TypeLib (FAD) Extensions.
-   Uso delle parole chiave ACF in un file IDL (opzione di **\_ configurazione MIDL/app** ).
-   Funzioni di callback statiche nel client.
-   Attributo [**asincrono**](async.md) .
-   [**\_ virgolette cpp**](cpp-quote.md) e **\# pragma MIDL \_ echo**.
-   tipi di carattere wide, costanti e stringhe [**WCHAR \_ t**](wchar-t.md) .
-   inizializzazione [**enum**](enum.md) (enumeratori sparse).
-   specifica di dimensioni solo in [**uscita**](out-idl.md).
-   Puntatori a dimensione mista e matrici di dimensioni.
-   Espressioni utilizzate per gli identificatori delle dimensioni e del discriminatore.
-   Handle espliciti parametri in qualsiasi posizione nell'elenco di argomenti. In modalità **/OSF** , il compilatore MIDL Cerca un handle di binding esplicito come primo parametro. Quando il primo parametro non è un handle di binding e vengono specificati uno o più handle di contesto, viene utilizzato l'handle del contesto più a sinistra come handle di associazione. Quando il primo parametro non è un handle e non sono presenti handle di contesto, la procedura usa l'associazione implicita usando [**l' \_ handle implicito**](implicit-handle.md) dell'attributo ACF o l' [**\_ handle automatico**](auto-handle.md).
-   Puntatore-ereditarietà del tipo di attributo. OSF DCE non consente puntatori senza attributi. Pertanto, in modalità **/OSF** ogni file IDL deve definire attributi per i relativi puntatori. Se un puntatore non dispone di un attributo esplicito, per impostare il tipo di puntatore è necessario che il file IDL disponga di una specifica [**\_ predefinita del puntatore**](pointer-default.md) .
-   Più interfacce in un file IDL.
-   Definizioni all'esterno del blocco di interfaccia.
-   Qualificatori di tipo, ad esempio **lontano** e **stdcall**.
-   Omissione degli attributi direzionali.

Le estensioni del linguaggio C/C++ seguenti non sono disponibili quando si esegue la compilazione con l'opzione **/OSF** :

-   Campi di bit in strutture e unioni.
-   Commenti a riga singola delimitati da due barre (//).
-   Dichiarazioni esterne.
-   Procedure con ellissi nell'elenco di parametri.
-   Digitare [**int**](int.md).
-   Digitare **void \*** (eccetto l'attributo [**dell' \_ handle di contesto**](context-handle.md) ).
-   I qualificatori di tipo, incluso il form con il prefisso ANSI, contengono due caratteri di sottolineatura: **\_ \_ cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ Export**, **Export**, **\_ \_ lontano**, **lontano**, **\_ \_ loadds**, **loadds**, **\_ \_ near**, **near**, **\_ \_ Pascal**, **Pascal**, **\_ \_ stdcall**, **stdcall**, **\_ \_ volatile** e **volatile**.
-   Qualsiasi \# [**pragma**](pragma.md) Warning o **\# pragma** comment.
-   Serializzazione del tipo.
-   Tipo di dati [**\_ \_ int3264**](--int3264.md) .
-   L'opzione [**/Protocol**](-protocol.md) e la sintassi ndr64 transfer.

## <a name="examples"></a>Esempio

**MIDL/OSF nomefile. idl**

**MIDL/OSF/app \_ config NomeFile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**configurazione di/app \_**](-app-config.md)
</dt> <dt>

[**/MS \_ ext**](-ms-ext.md)
</dt> <dt>

[Pacchetto di gestione della memoria RPCSS](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 