---
title: File UUID dell'interfaccia
description: Il file UUID dell'interfaccia raccoglie le definizioni degli identificatori di interfaccia da tutte le interfacce del file IDL elaborato.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL e COM MIDL, interfacce, file UUID proxy
- file UUID dell'interfaccia MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713456"
---
# <a name="the-interface-uuid-file"></a>File UUID dell'interfaccia

Il file UUID dell'interfaccia raccoglie le definizioni degli identificatori di interfaccia da tutte le interfacce del file IDL elaborato. Analogamente al file stub e al file di intestazione, la chiusura del flusso di input è definita dal file IDL corrente e dai file inclusi. Ad esempio, per l'interfaccia IFace, il compilatore genera un IID costante \_ IFace e lo inizializza sull'UUID dell'interfaccia specificato nel file IDL. Le applicazioni client e la DLL proxy utilizzano questa costante per identificare l'interfaccia.

Il nome predefinito per un file IID di interfaccia generato da un file. idl è il file \_ i.c. L'opzione del compilatore MIDL [**/IID**](-iid.md) sostituisce il nome predefinito del file UUID dell'interfaccia.

 

 




