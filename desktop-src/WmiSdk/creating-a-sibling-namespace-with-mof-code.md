---
description: Un altro modo per creare uno spazio dei nomi consiste nell'usare il codice Managed Object Format (MOF) per creare uno spazio dei nomi di pari livello. Uno spazio dei nomi di pari livello è uno spazio dei nomi che non esiste come elemento figlio dello spazio dei nomi corrente.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Creazione di uno spazio dei nomi di pari livello con codice MOF
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317565"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a>Creazione di uno spazio dei nomi di pari livello con codice MOF

Un altro modo per creare uno spazio dei nomi consiste nell'usare il codice Managed Object Format (MOF) per creare uno spazio dei nomi di pari livello. Uno spazio dei nomi di pari livello è uno spazio dei nomi che non esiste come elemento figlio dello spazio dei nomi corrente.

Nella procedura seguente viene descritto come creare uno spazio dei nomi di pari livello con codice MOF.

**Per creare uno spazio dei nomi di pari livello con codice MOF**

1.  Inserire il comando [**\# pragma namespace**](pragma-namespace.md) nel codice MOF prima della dichiarazione dello spazio dei nomi.

    Il comando [**\# pragma namespace**](pragma-namespace.md) indica a WMI dove creare le istanze dopo la direttiva.

2.  Creare un'istanza della classe dello [**\_ \_ spazio dei nomi**](--namespace.md) .
3.  Compilare il codice con l'utilità [mofcomp](mofcomp.md) o l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

Nell'esempio di codice MOF seguente viene descritto come creare uno spazio dei nomi come elemento di pari livello per lo \\ spazio dei nomi "root CIMv2".

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



