---
description: I timestamp vengono in genere inclusi quando un file viene firmato usando SignTool con l'opzione -t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Aggiunta di timestamp ai file firmati in precedenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988f63e7b5c58f5d8346d074d3ec98d31dc87443670480f7ded2e72f2272275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880231"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Aggiunta di timestamp ai file firmati in precedenza

I timestamp vengono in genere inclusi quando un file viene firmato usando SignTool con **l'opzione -t.** Inoltre, i timestamp possono essere aggiunti ai file firmati senza timestamp. Il comando seguente aggiunge un timestamp a un file firmato in precedenza:

**timestamp signtool -t https: \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> Il file da impostare come timestamp deve essere stato firmato in precedenza.

 

Per altre informazioni su SignTool, vedere [SignTool.](signtool.md)

 

 



