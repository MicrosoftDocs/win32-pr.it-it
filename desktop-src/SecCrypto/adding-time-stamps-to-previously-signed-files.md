---
description: I timestamp vengono in genere inclusi quando un file viene firmato usando SignTool con l'opzione-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Aggiunta di timestamp ai file firmati in precedenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322039"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Aggiunta di timestamp ai file firmati in precedenza

I timestamp vengono in genere inclusi quando un file viene firmato usando SignTool con l'opzione **-t** . Inoltre, è possibile aggiungere timestamp ai file firmati senza un timestamp. Il seguente comando aggiunge un timestamp a un file firmato in precedenza:

**timestamp di SignTool-t https: \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> Il file per il quale è stato contrassegnato il timestamp deve essere stato precedentemente firmato.

 

Per ulteriori informazioni su SignTool, vedere [SignTool](signtool.md).

 

 



