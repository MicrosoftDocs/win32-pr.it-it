---
title: opzione/RPCSS
description: L'opzione/RPCSS, se specificata, funge da se l' \_ attributo Enable allocate è stato specificato in tutte le operazioni dell'interfaccia. L'utilizzo di questo attributo non è consigliato.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- /RPCSS switch MIDL
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045590"
---
# <a name="rpcss-switch"></a><span data-ttu-id="9399b-105">opzione/RPCSS</span><span class="sxs-lookup"><span data-stu-id="9399b-105">/rpcss switch</span></span>

<span data-ttu-id="9399b-106">L'opzione **/RPCSS** , se specificata, funge da se l'attributo [**enable \_ allocate**](enable-allocate.md) è stato specificato in tutte le operazioni dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="9399b-106">The **/rpcss** switch, when specified, acts as though the [**enable\_allocate**](enable-allocate.md) attribute was specified on all operations of the interface.</span></span> <span data-ttu-id="9399b-107">L'utilizzo di questo attributo non è consigliato.</span><span class="sxs-lookup"><span data-stu-id="9399b-107">The usage of this attribute is not recommended.</span></span>

``` syntax
midl /rpcss
```

## <a name="switch-options"></a><span data-ttu-id="9399b-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="9399b-108">Switch Options</span></span>

<span data-ttu-id="9399b-109">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="9399b-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9399b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9399b-110">Remarks</span></span>

<span data-ttu-id="9399b-111">In modalità predefinita, il pacchetto RpcSs è abilitato solo se la procedura o l'interfaccia ha l'attributo [**enable \_ allocate**](enable-allocate.md) o l'opzione **/RPCSS** è specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9399b-111">In default mode, the RpcSs package is enabled only if either the procedure or interface has the [**enable\_allocate**](enable-allocate.md) attribute or the **/rpcss** switch is specified on the command line.</span></span> <span data-ttu-id="9399b-112">In modalità **/OSF** , lo stub sul lato server Abilita il pacchetto di allocazione RPCSS.</span><span class="sxs-lookup"><span data-stu-id="9399b-112">In **/osf** mode, the server-side stub enables the RpcSs allocation package.</span></span>

## <a name="examples"></a><span data-ttu-id="9399b-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="9399b-113">Examples</span></span>

<span data-ttu-id="9399b-114">**MIDL/RPCSS nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="9399b-114">**midl /rpcss filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="9399b-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9399b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9399b-116">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="9399b-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="9399b-117">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="9399b-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9399b-118">**Abilita \_ allocazione**</span><span class="sxs-lookup"><span data-stu-id="9399b-118">**enable\_allocate**</span></span>](enable-allocate.md)
</dt> <dt>

[<span data-ttu-id="9399b-119">**/osf**</span><span class="sxs-lookup"><span data-stu-id="9399b-119">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




