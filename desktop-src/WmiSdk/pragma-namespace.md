---
description: Richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come NamespacePath. Se vengono usati sia l'opzione dello spazio dei nomi del compilatore MOF-n che lo \# spazio dei nomi pragma&\# 32; il comando NamespacePath, il comando ha la priorità sull'opzione.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: spazio dei nomi pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753687"
---
# <a name="pragma-namespace"></a><span data-ttu-id="968af-104">spazio dei nomi pragma</span><span class="sxs-lookup"><span data-stu-id="968af-104">pragma namespace</span></span>

<span data-ttu-id="968af-105">Il comando per il preprocessore **pragma namespace** richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come *namespacePath*.</span><span class="sxs-lookup"><span data-stu-id="968af-105">The **pragma namespace** preprocessor command requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="968af-106">Se vengono usati sia l'opzione dello spazio dei nomi del compilatore MOF **-n** che il comando **\# pragma namespace** *namespacePath* , il comando ha la priorità sull'opzione.</span><span class="sxs-lookup"><span data-stu-id="968af-106">If both the MOF compiler **-n** namespace switch and the **\#pragma namespace** *namespacepath* command are used, the command takes priority over the switch.</span></span>

<span data-ttu-id="968af-107">Di seguito viene descritta la sintassi:</span><span class="sxs-lookup"><span data-stu-id="968af-107">The following describes the syntax:</span></span>


```mof
#pragma namespace ("[Namespace]")
```



<span data-ttu-id="968af-108">Lo spazio dei *\[ nomi \]* è lo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="968af-108">*\[Namespace\]* is the specified namespace.</span></span>

<span data-ttu-id="968af-109">Se non si specifica questo comando o l'opzione della riga di comando equivalente, il compilatore MOF utilizzerà lo \\ spazio dei nomi predefinito radice per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="968af-109">If you do not specify this command or the equivalent command-line switch, the MOF compiler uses the root\\default namespace by default.</span></span>

## <a name="remarks"></a><span data-ttu-id="968af-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="968af-110">Remarks</span></span>

<span data-ttu-id="968af-111">È possibile richiedere che le applicazioni e gli script client usino una connessione crittografata per l'autenticazione aggiungendo il qualificatore **RequiresEncryption** al file MOF che crea lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="968af-111">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="968af-112">È anche possibile modificare uno spazio dei nomi esistente aggiungendo questo attributo e compilare di nuovo il file MOF.</span><span class="sxs-lookup"><span data-stu-id="968af-112">You can also modify an existing namespace by adding this attribute and compile the MOF file again.</span></span> <span data-ttu-id="968af-113">Per ulteriori informazioni sull'utilizzo di **RequiresEncryption**, vedere la pagina relativa alla [richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="968af-113">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="examples"></a><span data-ttu-id="968af-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="968af-114">Examples</span></span>

<span data-ttu-id="968af-115">Nell'esempio seguente viene illustrato come posizionare le classi o le istanze nello \\ spazio dei nomi "root test".</span><span class="sxs-lookup"><span data-stu-id="968af-115">The following example shows how place classes or instances in the "Root\\Test" namespace.</span></span>


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a><span data-ttu-id="968af-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="968af-116">Requirements</span></span>



| <span data-ttu-id="968af-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="968af-117">Requirement</span></span> | <span data-ttu-id="968af-118">Valore</span><span class="sxs-lookup"><span data-stu-id="968af-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="968af-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="968af-119">Minimum supported client</span></span><br/> | <span data-ttu-id="968af-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="968af-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="968af-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="968af-121">Minimum supported server</span></span><br/> | <span data-ttu-id="968af-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="968af-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="968af-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="968af-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968af-124">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="968af-124">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="968af-125">**Qualificatori WMI standard**</span><span class="sxs-lookup"><span data-stu-id="968af-125">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="968af-126">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="968af-126">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




