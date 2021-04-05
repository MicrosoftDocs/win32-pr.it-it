---
title: LocalServer
description: Specifica il percorso completo di un'applicazione server locale a 16 bit.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- LocalServer chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045058"
---
# <a name="localserver"></a>LocalServer

Specifica il percorso completo di un'applicazione server locale a 16 bit.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** che specifica il percorso completo e può includere qualsiasi argomento della riga di comando.

COM aggiunge il flag "-Embedding" alla stringa, quindi l'applicazione che usa i flag deve analizzare l'intera stringa e verificare la presenza del flag-Embedding.

Per eseguire un server oggetto COM in uno spazio di memoria separato, modificare il valore di **LocalServer** come indicato di seguito:

**cmd/c avviare/separate** *percorso * * *. exe**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**LocalServer32**](localserver32.md)
</dt> </dl>

 

 




