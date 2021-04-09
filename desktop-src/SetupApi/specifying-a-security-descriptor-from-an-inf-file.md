---
description: È possibile controllare la capacità di un processo di accedere agli oggetti a protezione diretta o di eseguire attività di amministrazione del sistema.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Specifica di un descrittore di sicurezza da un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968500"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a><span data-ttu-id="e791b-103">Specifica di un descrittore di sicurezza da un file INF</span><span class="sxs-lookup"><span data-stu-id="e791b-103">Specifying a Security Descriptor From an INF File</span></span>

<span data-ttu-id="e791b-104">È possibile controllare la capacità di un processo di accedere agli oggetti a protezione diretta o di eseguire attività di amministrazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="e791b-104">You can control the ability of a process to access securable objects or to perform system administration tasks.</span></span> <span data-ttu-id="e791b-105">Un oggetto a protezione diretta è un oggetto che può disporre di un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e791b-105">A securable object is an object that can have a security descriptor.</span></span> <span data-ttu-id="e791b-106">Tutti gli oggetti denominati sono entità a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="e791b-106">All named objects are securable.</span></span> <span data-ttu-id="e791b-107">Alcuni oggetti senza nome, ad esempio gli oggetti processo e thread, possono avere anche descrittori di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e791b-107">Some unnamed objects, such as process and thread objects, can have security descriptors too.</span></span> <span data-ttu-id="e791b-108">Per ulteriori informazioni sul controllo dell'accesso agli oggetti a protezione diretta, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="e791b-108">For more information about controlling access to securable objects see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="e791b-109">I [descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) contengono le informazioni di sicurezza associate agli oggetti a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="e791b-109">[Security descriptors](/windows/desktop/SecAuthZ/security-descriptors) contain the security information associated with securable objects.</span></span> <span data-ttu-id="e791b-110">Per la maggior parte degli oggetti a protezione diretta, è possibile specificare un descrittore di sicurezza di un oggetto nella chiamata di funzione che crea l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e791b-110">For most securable objects, you can specify an object's security descriptor in the function call that creates the object.</span></span> <span data-ttu-id="e791b-111">È ad esempio possibile specificare un descrittore di sicurezza nelle funzioni [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="e791b-111">For example, you can specify a security descriptor in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) functions.</span></span>

<span data-ttu-id="e791b-112">Per impostare un descrittore di sicurezza da un file INF, aggiungere una sezione sicurezza creata dal writer INF immediatamente dopo la sezione che consente di installare il file, la chiave del registro di sistema o il componente.</span><span class="sxs-lookup"><span data-stu-id="e791b-112">To set a security descriptor from an INF file, add an INF-writer authored Security section immediately following the section that installs the file, registry key, or component.</span></span> <span data-ttu-id="e791b-113">La sezione Security deve contenere una riga con il descrittore di sicurezza della stringa scritta usando il formato per le [stringhe del descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-strings).</span><span class="sxs-lookup"><span data-stu-id="e791b-113">The Security section should contain one line with the string security descriptor written on it using the format for [Security Descriptor Strings](/windows/desktop/SecAuthZ/security-descriptor-strings).</span></span> <span data-ttu-id="e791b-114">La riga deve anche essere racchiusa tra virgolette (").</span><span class="sxs-lookup"><span data-stu-id="e791b-114">The line should also be enclosed by quotation marks (").</span></span>

<span data-ttu-id="e791b-115">Il frammento di file INF seguente, ad esempio, creerà una chiave del registro di sistema a cui possono accedere solo gli amministratori e il sistema.</span><span class="sxs-lookup"><span data-stu-id="e791b-115">For example, the following INF file snippet would create a registry key to which only administrators and the system have access.</span></span> <span data-ttu-id="e791b-116">Si noti che questo esempio richiede privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="e791b-116">Note that this example requires administrative privileges.</span></span>

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

<span data-ttu-id="e791b-117">In questo caso, il significato della stringa è che gli amministratori hanno il controllo completo, il sistema dispone di controllo completo e l'accesso è ereditabile a tutte le sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="e791b-117">In this case, the meaning of the string is that administrators have full control, system has full control, and access is inheritable to all subkeys.</span></span> <span data-ttu-id="e791b-118">Per ulteriori informazioni, vedere [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="e791b-118">For more information see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span>

 

 
