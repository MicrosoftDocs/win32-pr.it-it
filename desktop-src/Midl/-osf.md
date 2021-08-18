---
title: Opzione /osf
description: L'opzione /osf forza la rigida compatibilità con DCE di OSF.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- Opzione /osf MIDL
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb887997642b0d0ff81314d6cf81dc148e57547727a09b1fe646f04d0391f967
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014119"
---
# <a name="osf-switch"></a>Opzione /osf

**L'opzione /osf** impone una rigida compatibilità con DCE OSF.

``` syntax
midl /osf
```

## <a name="switch-options"></a>Opzioni di cambio

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Usare questa opzione se l'applicazione richiede una compatibilità rigorosa con DCE OSF per motivi di portabilità.

In **modalità /osf** il pacchetto RpcSs viene abilitato automaticamente quando si usano puntatori completi, gli argomenti richiedono l'allocazione della memoria o quando si usa l'attributo [**enable \_ allocate.**](enable-allocate.md) Ciò significa che non è necessario fornire le funzioni [**midl \_ user \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) e [**midl \_ user \_ free**](/windows/desktop/Rpc/the-midl-user-free-function) nell'applicazione client e server.

Le funzionalità estese di Microsoft seguenti non sono disponibili quando si esegue la compilazione con **l'opzione /osf:**

-   Dichiaratori astratti (parametri senza nome) nel file IDL.
-   Definizioni di interfaccia per gli oggetti COM.
-   Nomi di interfaccia con più di 17 caratteri.
-   Attributi solo MIDL, ad esempio [**wire \_ marshal,**](wire-marshal.md) [**user \_ marshal**](user-marshal.md)e typelib (ODL).
-   Uso di parole chiave ACF in un file IDL (opzione MIDL **/app \_ config).**
-   Funzioni di callback statiche nel client.
-   Attributo [**asincrono.**](async.md)
-   [**Virgolette \_ cpp**](cpp-quote.md) e **\# pragma midl \_ echo**.
-   [**wchar \_ t**](wchar-t.md) tipi di caratteri wide, costanti e stringhe.
-   [**Inizializzazione dell'enumerazione**](enum.md) (enumeratori di tipo sparse).
-   [**specifica**](out-idl.md)delle dimensioni out-only.
-   Puntatori a dimensioni miste e matrici di dimensioni.
-   Espressioni usate per gli identificatori di dimensioni e discriminanti.
-   Parametri di handle espliciti in qualsiasi posizione nell'elenco di argomenti. In **modalità /osf** il compilatore MIDL cerca un handle di associazione esplicito come primo parametro. Quando il primo parametro non è un handle di associazione e vengono specificati uno o più handle di contesto, come handle di associazione viene usato l'handle di contesto più a sinistra. Quando il primo parametro non è un handle e non sono presenti handle di contesto, la procedura usa l'associazione implicita usando [**\_ l'handle implicito**](implicit-handle.md) dell'attributo ACF o [**l'handle \_ automatico**](auto-handle.md).
-   Ereditarietà del tipo di attributo pointer. OSF DCE non consente puntatori senza attributi. Pertanto, in **modalità /osf** ogni file IDL deve definire attributi per i relativi puntatori. Se un puntatore non ha un attributo esplicito, il file IDL deve avere una specifica predefinita del puntatore per impostare il tipo di puntatore. [**\_**](pointer-default.md)
-   Più interfacce in un file IDL.
-   Definizioni all'esterno del blocco di interfaccia.
-   Qualificatori di tipo, ad **esempio far** e **stdcall**.
-   Omissione di attributi direzionali.

Le estensioni del linguaggio C/C++ seguenti non sono disponibili quando si esegue la compilazione con **l'opzione /osf:**

-   Campi di bit in strutture e unioni.
-   Commenti a riga singola delimitati da due caratteri barra (//).
-   Dichiarazioni esterne.
-   Procedure con puntini di sospensione nell'elenco di parametri.
-   Digitare [**int**](int.md).
-   Digitare **void \** _ (ad eccezione dell'attributo [_ context *\_ handle).* *](context-handle.md)
-   I qualificatori di tipo, incluso il formato con il prefisso conforme a ANSI, contengono due caratteri di sottolineatura: **\_ \_ cdecl**, **cdecl**, const , **const**, **\_ \_ export**, export , **\_ \_ far**, **far**, **loadds**, [](const.md) **\_ \_ loadds**, **\_ \_ near** **,** near , **\_ \_ pascal**, **\_ \_ stdcall**, **stdcall**, **\_ \_ volatile** e **volatile**. 
-   Qualsiasi \# [**avviso pragma**](pragma.md) o **\# commento pragma.**
-   Serializzazione del tipo.
-   Tipo [**\_ \_ di dati int3264.**](--int3264.md)
-   Opzione [**/protocol e**](-protocol.md) sintassi di trasferimento ndr64.

## <a name="examples"></a>Esempio

**midl /osf filename.idl**

**midl /osf /app \_ config filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/app \_ config**](-app-config.md)
</dt> <dt>

[**/ms \_ ext**](-ms-ext.md)
</dt> <dt>

[Pacchetto di gestione della memoria Rpcss](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 