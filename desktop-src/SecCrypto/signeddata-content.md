---
description: Imposta o recupera i dati da firmare. Si tratta della proprietà predefinita.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: Proprietà SignedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332834"
---
# <a name="signeddatacontent-property"></a><span data-ttu-id="1d967-104">Proprietà SignedData. Content</span><span class="sxs-lookup"><span data-stu-id="1d967-104">SignedData.Content property</span></span>

<span data-ttu-id="1d967-105">\[La proprietà **Content** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="1d967-105">\[The **Content** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1d967-106">Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="1d967-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="1d967-107">La proprietà **Content** imposta o recupera i dati da firmare.</span><span class="sxs-lookup"><span data-stu-id="1d967-107">The **Content** property sets or retrieves the data to be signed.</span></span> <span data-ttu-id="1d967-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="1d967-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d967-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d967-109">Syntax</span></span>


```VB
SignedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="1d967-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1d967-110">Property value</span></span>

<span data-ttu-id="1d967-111">Dati da firmare.</span><span class="sxs-lookup"><span data-stu-id="1d967-111">The data to be signed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d967-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d967-112">Remarks</span></span>

<span data-ttu-id="1d967-113">Questa proprietà deve essere inizializzata prima che venga chiamato il metodo [**Sign**](signeddata-sign.md) .</span><span class="sxs-lookup"><span data-stu-id="1d967-113">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span> <span data-ttu-id="1d967-114">Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto e tutte le firme associate all'oggetto prima della modifica della proprietà vengono perse.</span><span class="sxs-lookup"><span data-stu-id="1d967-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d967-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d967-115">Requirements</span></span>



| <span data-ttu-id="1d967-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d967-116">Requirement</span></span> | <span data-ttu-id="1d967-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1d967-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d967-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="1d967-118">Redistributable</span></span><br/> | <span data-ttu-id="1d967-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d967-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1d967-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1d967-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="1d967-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d967-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d967-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d967-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d967-123">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="1d967-123">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
