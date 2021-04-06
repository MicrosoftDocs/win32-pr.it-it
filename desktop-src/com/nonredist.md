---
title: NONREDIST
description: Aggiunge nomi all'elenco di file che non devono essere esportati quando le applicazioni COM+ sono assemblate per l'installazione in altri computer. Si noti che si tratta di una sottochiave, non di un valore.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- Valore del registro di sistema non REDIST COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045405"
---
# <a name="nonredist"></a>NONREDIST

Aggiunge nomi all'elenco di file che non devono essere esportati quando le applicazioni COM+ sono assemblate per l'installazione in altri computer. Si noti che si tratta di una sottochiave, non di un valore.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a>Commenti

I file aggiunti all'elenco sono rappresentati da coppie nome/valore archiviate in questa chiave. In ogni coppia nome/valore il nome è il nome del file e il valore è riservato.

 

 




