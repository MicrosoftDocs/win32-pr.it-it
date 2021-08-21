---
title: ADSI WinNT Provider
description: Il provider Microsoft ADSI implementa un set di oggetti ADSI per supportare varie interfacce ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- adsi winnt provider ADSI
- ADSI del provider di servizi WinNT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb0984b150355099e1609481432f01d9b00be110b64bb82d08a938c02acb7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692791"
---
# <a name="adsi-winnt-provider"></a>ADSI WinNT Provider

Il provider Microsoft ADSI implementa un set di oggetti ADSI per supportare varie interfacce ADSI. Il nome dello spazio dei nomi Windows provider è "WinNT" e questo provider viene comunemente definito provider WinNT. Per accedere al provider WinNT, eseguire il binding a uno degli oggetti [ADSI](adsi-objects-of-winnt.md)di WinNT usando [WinNT AdsPath.](winnt-adspath.md)

Il provider WinNT è incluso nel componente di sistema ADSI per Windows e Windows Server.

> [!Note]  
> Il provider WinNT predefinito non può essere considerato completamente thread-safe. I writer di applicazioni multithreading devono gestire il multithreading per coordinare correttamente qualsiasi accesso tra thread tramite l'uso corretto di oggetti di sincronizzazione, ad esempio semafori, mutex, sezioni critiche e così via.

 

 

 




