---
title: Provider LDAP ADSI
description: Il provider LDAP ADSI implementa un set di oggetti ADSI che supportano varie interfacce ADSI. Per accedere al provider LDAP, eseguire l'associazione a uno degli oggetti ADSI LDAP usando il ADsPath LDAP.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- Provider LDAP ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855361"
---
# <a name="adsi-ldap-provider"></a>Provider LDAP ADSI

Il provider LDAP ADSI implementa un set di oggetti ADSI che supportano varie interfacce ADSI. Per accedere al provider LDAP, eseguire l'associazione a uno degli oggetti ADSI LDAP usando il ADsPath LDAP.

Per lavorare con il provider, è necessario che nel computer client siano installati Adsldp.dll, Adsldpc.dll, Adsmsext.dll e Activeds.dll.

> [!Note]  
> Il provider LDAP ADSI predefinito non può essere considerato completamente thread-safe. I writer di applicazioni multithread devono coordinare correttamente l'accesso tra thread attraverso l'uso corretto di oggetti di sincronizzazione, ad esempio semafori, mutex, sezioni critiche e così via.

 

 

 




