---
title: attributo ncacn_at_dsp
description: La \_ \_ parola chiave ncacn at DSP identifica AppleTalk DSP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- attributo ncacn_at_dsp MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963045"
---
# <a name="ncacn_at_dsp-attribute"></a><span data-ttu-id="e63e8-105">ncacn \_ nell' \_ attributo DSP</span><span class="sxs-lookup"><span data-stu-id="e63e8-105">ncacn\_at\_dsp attribute</span></span>

<span data-ttu-id="e63e8-106">La parola chiave **ncacn \_ at \_ DSP** identifica AppleTalk DSP come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e63e8-106">The **ncacn\_at\_dsp** keyword identifies AppleTalk DSP as the protocol family for the endpoint.</span></span> <span data-ttu-id="e63e8-107">Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e63e8-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="e63e8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e63e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e63e8-109">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="e63e8-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e63e8-110">Specifica una stringa di caratteri con lunghezza fino a 22 byte.</span><span class="sxs-lookup"><span data-stu-id="e63e8-110">Specifies a character string up to 22 bytes long.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e63e8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e63e8-111">Remarks</span></span>

<span data-ttu-id="e63e8-112">La sintassi della stringa di porta AppleTalk DSP, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="e63e8-112">The syntax of the AppleTalk DSP port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="e63e8-113">Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="e63e8-113">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="e63e8-114">Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="e63e8-114">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="e63e8-115">Esempi</span><span class="sxs-lookup"><span data-stu-id="e63e8-115">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="e63e8-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e63e8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e63e8-117">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="e63e8-117">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="e63e8-118">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="e63e8-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e63e8-119">**Associazione stringa**</span><span class="sxs-lookup"><span data-stu-id="e63e8-119">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 