---
description: Un'applicazione può troncare o estendere un file chiamando SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Troncamento o estensione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316763"
---
# <a name="truncating-or-extending-files"></a>Troncamento o estensione di file

Un'applicazione può troncare o estendere un file chiamando [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile). Questa funzione imposta il marcatore di fine file sulla posizione corrente del puntatore del file.

Si noti che quando un file viene esteso, il contenuto tra i percorsi di fine file obsoleti e nuovi non è definito.

 

 



