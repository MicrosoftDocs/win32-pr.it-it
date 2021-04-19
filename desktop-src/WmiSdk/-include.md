---
description: Include il contenuto di un file MOF in un altro file MOF.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5eb3d203cff5bca7e5096082cca7ba531580ae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317580"
---
# <a name="include"></a>' #include '
/* Titolo: MyMof. mof                           *//*   title: MyMof2. mof */

Il \# comando Includi preprocessore include il contenuto di un file MOF in un altro file MOF. Nell'esempio di codice riportato di seguito viene illustrata la sintassi per il \# comando Includi.

``` syntax
#include ("Moffile.mof")
```

Nell'esempio precedente, Moffile. MOF è il nome del file MOF da includere.

Nell'esempio seguente vengono illustrati due file MOF. Quando si compila il primo file MOF, il compilatore compila automaticamente il secondo file MOF (Mymof2. MOF) nel percorso in cui si inserisce l' \# istruzione include.

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

Il file MOF seguente è incluso nell'esempio precedente:

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 



