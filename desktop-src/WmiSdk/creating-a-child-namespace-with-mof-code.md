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
# <a name="creating-a-child-namespace-with-mof-code"></a><span data-ttu-id="dad40-104">Creazione di uno spazio dei nomi figlio con codice MOF</span><span class="sxs-lookup"><span data-stu-id="dad40-104">Creating a Child Namespace with MOF Code</span></span>

<span data-ttu-id="dad40-105">Il modo più semplice per creare uno spazio dei nomi consiste nell'usare il codice Managed Object Format (MOF) per creare lo spazio dei nomi all'interno della directory corrente.</span><span class="sxs-lookup"><span data-stu-id="dad40-105">The simplest way of creating a namespace is to use Managed Object Format (MOF) code to create the namespace inside the current directory.</span></span> <span data-ttu-id="dad40-106">La directory corrente viene definita al momento dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="dad40-106">The current directory is defined when you log on.</span></span>

<span data-ttu-id="dad40-107">Nella procedura riportata di seguito viene descritto come creare uno spazio dei nomi figlio utilizzando il codice MOF.</span><span class="sxs-lookup"><span data-stu-id="dad40-107">The following procedure describes how to create a child namespace using MOF code.</span></span>

<span data-ttu-id="dad40-108">**Per creare uno spazio dei nomi figlio utilizzando il codice MOF**</span><span class="sxs-lookup"><span data-stu-id="dad40-108">**To create a child namespace using MOF code**</span></span>

1.  <span data-ttu-id="dad40-109">Creare un'istanza della classe dello [**\_ \_ spazio dei nomi**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="dad40-109">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>

    <span data-ttu-id="dad40-110">Nell'esempio di codice seguente viene illustrato come creare uno spazio dei nomi figlio.</span><span class="sxs-lookup"><span data-stu-id="dad40-110">The following code example shows how to create a child namespace.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  <span data-ttu-id="dad40-111">Se si desidera richiedere all'utente di effettuare una connessione crittografata allo spazio dei nomi, utilizzare il qualificatore **RequiresEncryption** .</span><span class="sxs-lookup"><span data-stu-id="dad40-111">If you want to require the user to make an encrypted connection to the namespace, use the **RequiresEncryption** qualifier.</span></span> <span data-ttu-id="dad40-112">Per ulteriori informazioni, vedere la pagina relativa [alla richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="dad40-112">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

    <span data-ttu-id="dad40-113">Nell'esempio di codice seguente viene illustrato come richiedere una connessione crittografata.</span><span class="sxs-lookup"><span data-stu-id="dad40-113">The following code example shows how to require an encrypted connection.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  <span data-ttu-id="dad40-114">Se si desidera impostare un descrittore di sicurezza nello spazio dei nomi anziché utilizzare la sicurezza predefinita dello spazio dei nomi, utilizzare il qualificatore **NamespaceSecuritySDDL** .</span><span class="sxs-lookup"><span data-stu-id="dad40-114">If you want to set a security descriptor on the namespace rather than using the default namespace security, use the **NamespaceSecuritySDDL** qualifier.</span></span> <span data-ttu-id="dad40-115">Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei nomi](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="dad40-115">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

    <span data-ttu-id="dad40-116">Nell'esempio di codice riportato di seguito viene illustrato come impostare un descrittore di sicurezza nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dad40-116">The following code example shows how to set a security descriptor on the namespace.</span></span>

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  <span data-ttu-id="dad40-117">Compilare e caricare l'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) utilizzando l'utilità [mofcomp](mofcomp.md) o l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="dad40-117">Compile and load the [**\_\_Namespace**](--namespace.md) instance using the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span> <span data-ttu-id="dad40-118">Sia mofcomp che l'interfaccia **IMOFCompiler** caricano automaticamente lo spazio dei nomi nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="dad40-118">Both mofcomp and the **IMofCompiler** interface automatically load the namespace into the current directory.</span></span> <span data-ttu-id="dad40-119">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="dad40-119">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dad40-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dad40-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dad40-121">**Qualificatori WMI standard**</span><span class="sxs-lookup"><span data-stu-id="dad40-121">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



