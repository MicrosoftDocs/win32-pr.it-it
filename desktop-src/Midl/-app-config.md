---
title: /app_config opzione
description: L'opzione di configurazione/app \_ Seleziona la modalità di configurazione dell'applicazione, che consente di usare alcune parole chiave di ACF nel file IDL. Con questa opzione del compilatore MIDL è possibile omettere l'ACF e specificare un'interfaccia in un unico file IDL.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config switch MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397887"
---
# <a name="app_config-switch"></a><span data-ttu-id="530b0-105">\_opzione di configurazione/app</span><span class="sxs-lookup"><span data-stu-id="530b0-105">/app\_config switch</span></span>

<span data-ttu-id="530b0-106">L' **opzione \_ di configurazione/app** seleziona la modalità di configurazione dell'applicazione, che consente di usare alcune parole chiave di ACF nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="530b0-106">The **/app\_config** switch selects application-configuration mode, which allows you to use some ACF keywords in the IDL file.</span></span> <span data-ttu-id="530b0-107">Con questa opzione del compilatore MIDL è possibile omettere l'ACF e specificare un'interfaccia in un unico file IDL.</span><span class="sxs-lookup"><span data-stu-id="530b0-107">With this MIDL compiler switch, you can omit the ACF and specify an interface in a single IDL file.</span></span>

``` syntax
midl /app_config
```

## <a name="switch-options"></a><span data-ttu-id="530b0-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="530b0-108">Switch Options</span></span>

<span data-ttu-id="530b0-109">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="530b0-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="530b0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="530b0-110">Remarks</span></span>

<span data-ttu-id="530b0-111">Microsoft RPC supporta l'utilizzo degli attributi ACF seguenti nel file IDL:</span><span class="sxs-lookup"><span data-stu-id="530b0-111">Microsoft RPC supports the use of the following ACF attributes in the IDL file:</span></span>

-   <span data-ttu-id="530b0-112">Handle implicito \_</span><span class="sxs-lookup"><span data-stu-id="530b0-112">Implicit\_handle</span></span>
-   <span data-ttu-id="530b0-113">\_Handle automatico</span><span class="sxs-lookup"><span data-stu-id="530b0-113">Auto\_handle</span></span>
-   <span data-ttu-id="530b0-114">Handle esplicito \_</span><span class="sxs-lookup"><span data-stu-id="530b0-114">Explicit\_handle</span></span>

<span data-ttu-id="530b0-115">Le versioni future di Microsoft RPC possono supportare l'utilizzo di altri attributi ACF nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="530b0-115">Future releases of Microsoft RPC may support the use of other ACF attributes in the IDL file.</span></span> <span data-ttu-id="530b0-116">L'opzione di **\_ configurazione/app** rappresenta un'estensione Microsoft per la specifica OSF-DCE e, di conseguenza, si escludono a vicenda con l'opzione [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="530b0-116">The **/app\_config** option represents a Microsoft extension to the OSF-DCE specification and, as such, is mutually exclusive with the [**/osf**](-osf.md) option.</span></span>

<span data-ttu-id="530b0-117">Per ulteriori informazioni relative all'opzione **di \_ configurazione/app** , vedere file di [configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md) e file di [definizione di interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="530b0-117">For more information related to the **/app\_config** switch, see [Application Configuration File (ACF)](application-configuration-file-acf-.md) and [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="530b0-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="530b0-118">Examples</span></span>

<span data-ttu-id="530b0-119">**nome file di MIDL/app \_ config. idl**</span><span class="sxs-lookup"><span data-stu-id="530b0-119">**midl /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="530b0-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="530b0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530b0-121">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="530b0-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




