---
description: Il modo più semplice per creare uno spazio dei nomi è usare Managed Object Format (MOF) per creare lo spazio dei nomi all'interno della directory corrente. La directory corrente viene definita quando si esegue l'accesso.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Creazione di uno spazio dei nomi figlio con codice MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d29edf493cb94c92715214dd2d7e7622ae12e831e71322afa8ad590272c6dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244641"
---
# <a name="creating-a-child-namespace-with-mof-code"></a>Creazione di uno spazio dei nomi figlio con codice MOF

Il modo più semplice per creare uno spazio dei nomi è usare Managed Object Format (MOF) per creare lo spazio dei nomi all'interno della directory corrente. La directory corrente viene definita quando si esegue l'accesso.

La procedura seguente descrive come creare uno spazio dei nomi figlio usando il codice MOF.

**Per creare uno spazio dei nomi figlio usando il codice MOF**

1.  Creare un'istanza della [**\_ \_ classe Namespace.**](--namespace.md)

    Nell'esempio di codice seguente viene illustrato come creare uno spazio dei nomi figlio.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  Se si vuole richiedere all'utente di stabilire una connessione crittografata allo spazio dei nomi, usare il qualificatore **RequiresEncryption.** Per altre informazioni, vedere [Richiesta di una connessione crittografata a uno spazio dei nomi.](requiring-an-encrypted-connection-to-a-namespace.md)

    Nell'esempio di codice seguente viene illustrato come richiedere una connessione crittografata.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  Se si vuole impostare un descrittore di sicurezza nello spazio dei nomi anziché usare la sicurezza dello spazio dei nomi predefinita, usare il qualificatore **NamespaceSecuritySDDL.** Per altre informazioni, vedere [Impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei nomi.](setting-namespace-security-when-the-namespace-is-created.md)

    Nell'esempio di codice seguente viene illustrato come impostare un descrittore di sicurezza nello spazio dei nomi .

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  Compilare e caricare [**\_ \_ l'istanza dello**](--namespace.md) spazio dei nomi [usando l'utilità mofcomp](mofcomp.md) o [**l'interfaccia IMofCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) Mofcomp e **l'interfaccia IMofCompiler** caricano automaticamente lo spazio dei nomi nella directory corrente. Per altre informazioni, vedere [Compilazione di file MOF.](compiling-mof-files.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Qualificatori WMI standard**](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



