---
title: Handle di binding MIDL
description: Gli handle di associazione sono oggetti dati che rappresentano l'associazione tra il client e il server.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- tipi di dati MIDL, handle di associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046576"
---
# <a name="midl-binding-handles"></a>Handle di binding MIDL

Gli handle di associazione sono oggetti dati che rappresentano l'associazione tra il client e il server.

MIDL supporta il tipo di base [**handle \_ t**](handle-t.md). Gli handle di questo tipo sono noti come "handle primitivi".

È possibile definire tipi di handle personalizzati usando l'attributo **\[ handle \]** . Gli handle definiti in questo modo sono noti come handle "definiti dall'utente" o "personalizzati" o "generici".

È anche possibile definire un handle che mantiene le informazioni sullo stato usando l'attributo dell' **\[** [**\_ handle di contesto**](context-handle.md) **\]** . Gli handle definiti in questo modo sono noti come handle "context".

Se non sono necessarie informazioni sullo stato e non si sceglie di chiamare le librerie di runtime RPC per gestire l'handle, è possibile richiedere che le librerie di runtime forniscano l'associazione automatica. Questa operazione viene eseguita tramite la parola chiave ACF **\[** [**auto \_ handle**](auto-handle.md) **\]** .

È possibile specificare una variabile globale come handle di associazione usando l' **\[** [**\_ handle implicito**](implicit-handle.md)della parola chiave ACF **\]** . La parola chiave **\[ \_ handle \] esplicita** viene usata per indicare che ogni funzione remota dispone di un handle specificato in modo esplicito.

Per ulteriori informazioni, vedere [Binding e handle](/windows/desktop/Rpc/binding-and-handles).

 

 