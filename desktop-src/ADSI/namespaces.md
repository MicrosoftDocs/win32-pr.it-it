---
title: Spazi dei nomi
description: Gli oggetti che risiedono all'interno di un determinato spazio dei nomi sono identificati da un nome univoco.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- spazi dei nomi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395282"
---
# <a name="namespaces"></a><span data-ttu-id="053ca-104">Spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="053ca-104">Namespaces</span></span>

<span data-ttu-id="053ca-105">Gli oggetti che risiedono all'interno di un determinato spazio dei nomi sono identificati da un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="053ca-105">Objects that reside within a given namespace are identified by a unique name.</span></span> <span data-ttu-id="053ca-106">Ad esempio, i file archiviati in un'unità disco del PC si trovano nello spazio dei nomi file system.</span><span class="sxs-lookup"><span data-stu-id="053ca-106">For example, files stored on a PC disk drive reside in the file system namespace.</span></span> <span data-ttu-id="053ca-107">Il nome univoco di un file è basato sulla posizione in cui è archiviato nello spazio dei nomi file system.</span><span class="sxs-lookup"><span data-stu-id="053ca-107">The unique name of a file is based on where it is stored in the file system namespace.</span></span> <span data-ttu-id="053ca-108">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="053ca-108">For example:</span></span>


```C++
C:\public\documents\adsi\adsi_spec.doc
```



<span data-ttu-id="053ca-109">Gli spazi dei nomi del servizio directory identificano inoltre gli oggetti in essi contenuti in base a nomi univoci, che in genere sono basati sul percorso nella directory in cui è possibile trovare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="053ca-109">Directory service namespaces also identify the objects they contain by unique names which are usually based on the location in the directory where the object can be found.</span></span> <span data-ttu-id="053ca-110">Ad esempio, in una directory X. 500, un oggetto specificato potrebbe avere un nome simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="053ca-110">For example, in an X.500 directory, a given object might have a name like this:</span></span>


```C++
CN=John,OU=Marketing,O=Fabrikam
```



<span data-ttu-id="053ca-111">Servizi directory diversi utilizzano moduli diversi per la denominazione degli oggetti in essi contenuti.</span><span class="sxs-lookup"><span data-stu-id="053ca-111">Different directory services use different forms for naming the objects they contain.</span></span> <span data-ttu-id="053ca-112">In questo modo è possibile affrontare diversi spazi dei nomi, in particolare per gli sviluppatori, considerando tutti i diversi ambienti in cui il codice potrebbe essere in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="053ca-112">This makes dealing with different namespaces challenging, especially for developers, considering all of the different environments on which the code might be running.</span></span>

<span data-ttu-id="053ca-113">Uno degli obiettivi di Active Directory Service Interfaces (ADSI) consiste nel fornire un Framework di denominazione che consenta l'accesso agli spazi dei nomi dei diversi provider di servizi di directory.</span><span class="sxs-lookup"><span data-stu-id="053ca-113">A goal of Active Directory Service Interfaces (ADSI) is to provide a naming framework that allows access to namespaces of different directory service providers.</span></span>

<span data-ttu-id="053ca-114">ADSI definisce una convenzione di denominazione che può identificare in modo univoco un oggetto in un ambiente eterogeneo.</span><span class="sxs-lookup"><span data-stu-id="053ca-114">ADSI defines a naming convention that can uniquely identify an object in a heterogeneous environment.</span></span> <span data-ttu-id="053ca-115">Questi nomi sono denominati stringhe ADsPath.</span><span class="sxs-lookup"><span data-stu-id="053ca-115">These names are called ADsPath strings.</span></span> <span data-ttu-id="053ca-116">Le stringhe ADsPath accettano diverse forme:</span><span class="sxs-lookup"><span data-stu-id="053ca-116">ADsPath strings take several forms:</span></span>


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



<span data-ttu-id="053ca-117">È possibile introdurre formati ADsPath aggiuntivi da provider ADSI diversi, ad esempio il provider ADSI per il server Internet Information Services, che supportano "IIS://" ADsPaths).</span><span class="sxs-lookup"><span data-stu-id="053ca-117">Additional ADsPath formats can be introduced by different ADSI providers (such as the ADSI provider for the Internet Information Services server, which support the "IIS://" ADsPaths).</span></span>

 

 




