---
title: opzione/prefix
description: L'opzione/prefix indica al compilatore MIDL di aggiungere stringhe di prefisso ai nomi di routine dello stub client e/o server.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- /prefix switch MIDL
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516354"
---
# <a name="prefix-switch"></a>opzione/prefix

L'opzione **/Prefix** indica al compilatore MIDL di aggiungere stringhe di prefisso ai nomi di routine dello stub client e/o server. Questo può essere usato per consentire a un singolo programma di essere sia un client che un server della stessa interfaccia, senza che i nomi di routine lato client e lato server siano in conflitto tra loro.

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span id="client"></span><span id="CLIENT"></span>client * * * *


</dt> <dd>

Influiscono solo sui nomi delle routine stub del client.

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span id="cstub"></span><span id="CSTUB"></span>cstub****


</dt> <dd>

Uguale a *client*. Influiscono solo sui nomi delle routine stub del client.

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span id="server"></span><span id="SERVER"></span>Server * * * *


</dt> <dd>

Influiscono solo sui nomi di routine chiamati dalla routine stub del server.

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span id="sstub"></span><span id="SSTUB"></span>sstub * * * *


</dt> <dd>

Uguale a *Server*. Influiscono solo sui nomi di routine chiamati dalla routine stub del server.

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span id="switch"></span><span id="SWITCH"></span>Switch * * * *


</dt> <dd>

Influiscono su un prototipo aggiuntivo aggiunto al file di intestazione.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>tutti i * * * *


</dt> <dd>

Influiscono sui nomi delle routine stub client e server.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Se il prefisso per le routine sul lato client è diverso dal prefisso per le routine lato server, il file di intestazione generato avrà sia i prototipi di routine lato client che i prototipi di routine lato server.

L'opzione **/Prefix** è utile quando si usa un singolo file di intestazione con stub di più esecuzioni del compilatore MIDL. In questo modo vengono forzati i prototipi di routine aggiuntivi nel file di intestazione.

In tutti i casi, i prefissi client, server e switch eseguiranno l'override di un prefisso all.

## <a name="examples"></a>Esempio

**"c \_ " Server "s \_ " del client MIDL/prefix**

**MIDL/Prefix All "Moo \_ "**

**client MIDL/prefix "Bark \_ "**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




