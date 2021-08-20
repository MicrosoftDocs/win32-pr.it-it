---
description: Un'applicazione può troncare o estendere un file chiamando SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Troncamento o estensione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cce4f5383a723c4fe12c9c25630bbba8b1c8bd9fa9ce5dec1c7e7872af41745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996337"
---
# <a name="truncating-or-extending-files"></a>Troncamento o estensione di file

Un'applicazione può troncare o estendere un file chiamando [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile). Questa funzione imposta il marcatore di fine file sulla posizione corrente del puntatore al file.

Si noti che quando un file viene esteso, il contenuto tra i percorsi di fine file precedente e nuovo non viene definito.

 

 



