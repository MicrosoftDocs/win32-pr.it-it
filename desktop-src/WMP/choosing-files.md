---
title: Scelta di file
description: Scelta di file
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- creazione di interfacce, scelta di file
- Windows Media Player Skins, scelta di file
- interfacce, scelta di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221876"
---
# <a name="choosing-files"></a>Scelta di file

Se si vuole scegliere un file, è possibile usare codice simile a quello dell'esempio della playlist, ma sostituire quanto segue per la sezione PLAYelement:


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



Questa riga userà il metodo **openDialog** del **tema** per definire un **URL** per il lettore. Questa operazione può essere usata per scegliere i file che non sono presenti in playlist.

Nella sezione di esempio dell'SDK è possibile vedere un esempio di **openDialog** funzionante simile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




