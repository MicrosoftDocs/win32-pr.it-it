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
ms.openlocfilehash: 3b7577639bd215fc051c2f1303e74fe946341a31c4b6708f881c3c9fabae2372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557778"
---
# <a name="include"></a>'#include'
/* Titolo: MyMof.Mof//Title: MyMof2.Mof */ 

Il \# comando include preprocessore include il contenuto di un file MOF in un altro file MOF. Nell'esempio di codice seguente viene descritta la sintassi per il \# comando include.

``` syntax
#include ("Moffile.mof")
```

Nell'esempio precedente Moffile.mof è il nome del file MOF da includere.

Nell'esempio seguente vengono illustrati due file MOF. Quando si compila il primo file MOF, il compilatore compila automaticamente il secondo file MOF (Mymof2.mof) nel percorso in cui si posiziona \# l'istruzione include.

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

Nell'esempio precedente è incluso il file MOF seguente:

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

[Comandi per il preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 



