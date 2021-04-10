---
title: Attributi ACF di ottimizzazione Stub
description: Questi attributi consentono di ottimizzare le dimensioni e la velocità del codice stub.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- ACF MIDL, attributi, Stub-ottimizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855882"
---
# <a name="stub-optimization-acf-attributes"></a><span data-ttu-id="3b915-104">Attributi ACF di ottimizzazione Stub</span><span class="sxs-lookup"><span data-stu-id="3b915-104">Stub Optimization ACF Attributes</span></span>

<span data-ttu-id="3b915-105">Questi attributi consentono di ottimizzare le dimensioni e la velocità del codice stub.</span><span class="sxs-lookup"><span data-stu-id="3b915-105">These attributes enable you to optimize the size and speed of your stub code.</span></span>



| <span data-ttu-id="3b915-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="3b915-106">Attribute</span></span>                                    | <span data-ttu-id="3b915-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="3b915-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b915-108">[**codice**](code.md)[**NoCode**](nocode.md)</span><span class="sxs-lookup"><span data-stu-id="3b915-108">[**code**](code.md)[**nocode**](nocode.md)</span></span> | <span data-ttu-id="3b915-109">Usare insieme gli attributi [**Code**](code.md) e [**NoCode**](nocode.md) per evitare la generazione di codice stub per le funzioni inutilizzate.</span><span class="sxs-lookup"><span data-stu-id="3b915-109">Use the [**code**](code.md) and [**nocode**](nocode.md) attributes together to avoid generating stub code for unused functions.</span></span> <span data-ttu-id="3b915-110">Applicare l'attributo **NoCode** all'intestazione dell'interfaccia e applicare l'attributo **Code** a tali procedure che verranno implementate dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="3b915-110">Apply the **nocode** attribute to the interface header, and apply the **code** attribute to those procedures that the client application will implement.</span></span> <span data-ttu-id="3b915-111">Il codice stub client verrà generato solo per le procedure selezionate.</span><span class="sxs-lookup"><span data-stu-id="3b915-111">Client stub code will be generated only for the selected procedures.</span></span>                                                                |
| [<span data-ttu-id="3b915-112">**ottimizzare**</span><span class="sxs-lookup"><span data-stu-id="3b915-112">**optimize**</span></span>](optimize.md)                 | <span data-ttu-id="3b915-113">Consente di ottimizzare il livello di ottimizzazione eseguito dal compilatore MIDL durante la generazione di codice stub, specificando che è necessario effettuare il marshalling dei dati tramite il metodo misto o interpretato.</span><span class="sxs-lookup"><span data-stu-id="3b915-113">Lets you fine-tune the level of optimization that the MIDL compiler performs when generating stub code, by specifying that data is to be marshaled by either the mixed-mode or interpreted method.</span></span> <span data-ttu-id="3b915-114">È possibile applicare l'attributo [**optimize**](optimize.md) a un'interfaccia o a funzioni selezionate all'interno dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3b915-114">You can apply the [**optimize**](optimize.md) attribute to an interface or to selected functions within the interface.</span></span> <span data-ttu-id="3b915-115">In entrambi i casi, il relativo utilizzo eseguirà l'override delle ottimizzazioni della riga di comando e di eventuali impostazioni predefinite preesistenti.</span><span class="sxs-lookup"><span data-stu-id="3b915-115">In either case, its use will override the command-line optimizations and any pre-existing defaults.</span></span> |



 

 

 




