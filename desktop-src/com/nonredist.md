---
title: NONREDIST
description: Aggiunge nomi all'elenco di file che non devono essere esportati quando le applicazioni COM+ vengono in pacchetto per l'installazione in altri computer. Si noti che si tratta di una sottochiave, non di un valore.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- Valore del Registro di sistema NONREDIST COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b303c145ea48a51f72d6ee21078b5f29a6b6d4fabc7184d4a37e980a2bbb2e4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678461"
---
# <a name="nonredist"></a>NONREDIST

Aggiunge nomi all'elenco di file che non devono essere esportati quando le applicazioni COM+ vengono in pacchetto per l'installazione in altri computer. Si noti che si tratta di una sottochiave, non di un valore.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a>Commenti

I file aggiunti all'elenco sono rappresentati da coppie nome/valore archiviate in questa chiave. In ogni coppia nome/valore, il nome è il nome del file e il valore è riservato.

 

 




