---
description: Il modo più semplice per creare uno spazio dei nomi consiste nell'usare il codice Managed Object Format (MOF) per creare lo spazio dei nomi all'interno della directory corrente. La directory corrente viene definita al momento dell'accesso.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Creazione di uno spazio dei nomi figlio con codice MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058476"
---
# <a name="creating-a-child-namespace-with-mof-code"></a>Creazione di uno spazio dei nomi figlio con codice MOF

Il modo più semplice per creare uno spazio dei nomi consiste nell'usare il codice Managed Object Format (MOF) per creare lo spazio dei nomi all'interno della directory corrente. La directory corrente viene definita al momento dell'accesso.

Nella procedura riportata di seguito viene descritto come creare uno spazio dei nomi figlio utilizzando il codice MOF.

**Per creare uno spazio dei nomi figlio utilizzando il codice MOF**

1.  Creare un'istanza della classe dello [**\_ \_ spazio dei nomi**](--namespace.md) .

    Nell'esempio di codice seguente viene illustrato come creare uno spazio dei nomi figlio.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  Se si desidera richiedere all'utente di effettuare una connessione crittografata allo spazio dei nomi, utilizzare il qualificatore **RequiresEncryption** . Per ulteriori informazioni, vedere la pagina relativa [alla richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).

    Nell'esempio di codice seguente viene illustrato come richiedere una connessione crittografata.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  Se si desidera impostare un descrittore di sicurezza nello spazio dei nomi anziché utilizzare la sicurezza predefinita dello spazio dei nomi, utilizzare il qualificatore **NamespaceSecuritySDDL** . Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei nomi](setting-namespace-security-when-the-namespace-is-created.md).

    Nell'esempio di codice riportato di seguito viene illustrato come impostare un descrittore di sicurezza nello spazio dei nomi.

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  Compilare e caricare l'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) utilizzando l'utilità [mofcomp](mofcomp.md) o l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) . Sia mofcomp che l'interfaccia **IMOFCompiler** caricano automaticamente lo spazio dei nomi nella directory corrente. Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Qualificatori WMI standard**](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



