---
description: L'interfaccia IX509EndorsementKey espone le proprietà seguenti.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Proprietà di IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314165"
---
# <a name="ix509endorsementkey-properties"></a><span data-ttu-id="f1755-103">Proprietà di IX509EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="f1755-103">IX509EndorsementKey Properties</span></span>

<span data-ttu-id="f1755-104">L'interfaccia [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="f1755-104">The [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f1755-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f1755-105">In this section</span></span>



| <span data-ttu-id="f1755-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="f1755-106">Topic</span></span>                                                                        | <span data-ttu-id="f1755-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1755-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1755-108">**Proprietà length**</span><span class="sxs-lookup"><span data-stu-id="f1755-108">**Length property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | <span data-ttu-id="f1755-109">Lunghezza in bit della chiave di verifica dell'autenticità.</span><span class="sxs-lookup"><span data-stu-id="f1755-109">The bit length of the endorsement key.</span></span> <span data-ttu-id="f1755-110">È possibile accedere a questa proprietà solo dopo che è stato chiamato il metodo [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="f1755-110">You can only access this property after the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been called.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="f1755-111">**Opened (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="f1755-111">**Opened property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | <span data-ttu-id="f1755-112">Indica se il metodo [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) è stato chiamato correttamente.</span><span class="sxs-lookup"><span data-stu-id="f1755-112">Indicates whether the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been successfully called.</span></span><br/>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="f1755-113">**Proprietà ProviderName**</span><span class="sxs-lookup"><span data-stu-id="f1755-113">**ProviderName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | <span data-ttu-id="f1755-114">Nome del provider di crittografia.</span><span class="sxs-lookup"><span data-stu-id="f1755-114">The name of the encryption provider.</span></span> <span data-ttu-id="f1755-115">Il valore predefinito è il provider di crittografia della piattaforma Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f1755-115">The default is the Microsoft Platform Crypto Provider.</span></span> <span data-ttu-id="f1755-116">È necessario impostare la proprietà [**providerName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) prima di chiamare il metodo [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="f1755-116">You must set the [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) property before you call the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method.</span></span> <span data-ttu-id="f1755-117">Non è possibile modificare la proprietà **providerName** dopo aver chiamato il metodo **Open** .</span><span class="sxs-lookup"><span data-stu-id="f1755-117">You cannot change the **ProviderName** property after you have called the **Open** method.</span></span><br/> |



 

 

 




