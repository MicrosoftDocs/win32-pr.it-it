---
title: Provider ADSI WinNT
description: Il provider Microsoft ADSI implementa un set di oggetti ADSI per supportare varie interfacce ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI del provider ADSI WinNT
- ADSI provider di servizi WinNT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395298"
---
# <a name="adsi-winnt-provider"></a>Provider ADSI WinNT

Il provider Microsoft ADSI implementa un set di oggetti ADSI per supportare varie interfacce ADSI. Il nome dello spazio dei nomi per il provider di Windows è "WinNT" e questo provider è comunemente denominato provider WinNT. Per accedere al provider WinNT, eseguire l'associazione a uno degli [oggetti ADSI di WinNT](adsi-objects-of-winnt.md), usando [WinNT ADsPath](winnt-adspath.md).

Il provider WinNT è incluso nel componente di sistema ADSI per Windows e Windows Server.

> [!Note]  
> Il provider WinNT predefinito non può essere considerato completamente thread-safe. I writer di applicazioni multithread devono gestire il multithreading per coordinare correttamente l'accesso tra thread attraverso l'uso corretto di oggetti di sincronizzazione quali semafori, mutex, sezioni critiche e così via.

 

 

 




