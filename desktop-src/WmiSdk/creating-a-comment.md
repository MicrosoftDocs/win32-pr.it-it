---
description: Il compilatore Managed Object Format (MOF) supporta due stili di commento usando due stili diversi di delimitatori di commento.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Creazione di un commento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d0e7cf2484fef018c62c8c47d9c55d245191681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310402"
---
# <a name="creating-a-comment"></a>Creazione di un commento

Il compilatore Managed Object Format (MOF) supporta due stili di commento usando due stili diversi di delimitatori di commento.

Nella tabella seguente sono elencati i delimitatori utilizzati per i commenti e l'effetto dei delimitatori nel codice.



| Delimitatore   | Marks                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | Inizio di un commento che termina alla fine della riga.                                    |
| /\* e \*/ | Inizio e fine di un commento che può estendersi su più righe o solo una parte di una riga. |



 

Come nei linguaggi di programmazione C e C++, è necessario utilizzare il delimitatore//con solo commenti a riga singola, ma utilizzare i \* \* delimitatori/e/con i commenti a riga singola o a più righe.

Nell'esempio di codice seguente vengono descritti i due stili di delimitazione.

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



