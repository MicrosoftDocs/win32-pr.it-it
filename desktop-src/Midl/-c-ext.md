---
title: /c_ext opzione
description: Questa opzione è obsoleta a partire dalla versione 3,0 del compilatore MIDL. Tuttavia, l'utilizzo dell' \_ opzione c ext non genererà un errore del compilatore, pertanto non è necessario rimuovere i riferimenti a/MS \_ ext o/c \_ ext da un makefile esistente.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext switch MIDL
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299217"
---
# <a name="c_ext-switch"></a>\_opzione/c EXT

Questa opzione è obsoleta a partire dalla versione 3,0 del compilatore MIDL. Tuttavia, l'utilizzo dell'opzione **c \_ ext** non genererà un errore del compilatore, pertanto non è necessario rimuovere i riferimenti a [**/MS \_ ext**](-ms-ext.md) o **/c \_ ext** da un makefile esistente.

``` syntax
midl /c_ext
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Le funzionalità seguenti sono ora disponibili per impostazione predefinita:

-   Molti file di intestazione esistenti definiscono i tipi con qualificatori, ad esempio **lontano** e **stdcall**, che non fanno parte dell'IDL DCE. Tali compilatori (e il compilatore MIDL in modalità di compatibilità DCE) generano errori quando tentano di elaborare questi qualificatori. Il compilatore MIDL consente di compilare file IDL che contengono questi qualificatori. I qualificatori di tipo non influiscono sulla modalità di trasmissione dei dati sulla rete.
-   È possibile omettere gli attributi direzionali, ad esempio [**\[ all'interno o all' \]**](in.md) [**\[ esterno \]**](out-idl.md).

Le estensioni del linguaggio C seguenti sono supportate in modalità predefinita:

-   Campi di bit in strutture e unioni
-   Commenti che iniziano con due barre (//)
-   Dichiarazioni esterne
-   Procedure con ellissi nell'elenco di parametri (...)
-   Sulle piattaforme a 32 bit, [**int**](int.md) è un tipo di base a 32 bit nativo; nelle piattaforme a 16 bit, **int** è riconosciuto ma non è un tipo utilizzabile in remoto
-   Tipo [**void \***](void.md) non usato nelle operazioni remote
-   I qualificatori di tipo, incluso il form con il prefisso ANSI-conforme, contengono due caratteri di sottolineatura: **cdecl**, **\_ \_ cdecl**, [**const**](const.md), **\_ \_ const**, **Export**, **\_ \_ Export**, **lontano**, **\_ \_ faraway**, **loadds**, **\_ \_ loadds**, **near**, **\_ \_ near**, **Pascal**, **\_ \_ Pascal**, **stdcall**, **\_ \_ stdcall**, **volatile** e **\_ \_ volatile**.

Per ulteriori informazioni sui qualificatori di dichiarazione, vedere la documentazione di Microsoft C/C++.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**configurazione di/app \_**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




