---
title: v1_enum (attributo)
description: L'attributo \ V1 \_ enum \ indica che il tipo enumerato specificato deve essere trasmesso come entità a 32 bit, anziché come valore predefinito a 16 bit.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- attributo v1_enum MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857438"
---
# <a name="v1_enum-attribute"></a><span data-ttu-id="bd875-104">\_attributo enum V1</span><span class="sxs-lookup"><span data-stu-id="bd875-104">v1\_enum attribute</span></span>

<span data-ttu-id="bd875-105">L'attributo **\[ \_ enum \] V1** indica che il tipo enumerato specificato deve essere trasmesso come entità a 32 bit, anziché come valore predefinito a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="bd875-105">The **\[v1\_enum\]** attribute directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="bd875-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd875-106">Parameters</span></span>

<span data-ttu-id="bd875-107">Questo attributo non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="bd875-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd875-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd875-108">Remarks</span></span>

<span data-ttu-id="bd875-109">L'utilizzo dell'attributo **\[ \_ enum \] V1** per la trasmissione di un tipo enumerato come entità a 32 bit aumenta l'efficienza del marshalling e dell'unmarshalling dei dati quando tale enumerazione è incorporata in strutture o unioni.</span><span class="sxs-lookup"><span data-stu-id="bd875-109">Using the **\[v1\_enum\]** attribute to transmit an enumerated type as a 32-bit entity increases the efficiency of marshaling and unmarshaling data when such an enumeration is embedded in structures or unions.</span></span>

<span data-ttu-id="bd875-110">Per migliorare le prestazioni, è consigliabile applicare l'attributo **\[ \_ enum \] V1** agli enumeratori nelle applicazioni a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="bd875-110">For improved performance, we recommend applying the **\[v1\_enum\]** attribute to enumerators in 32-bit applications.</span></span> <span data-ttu-id="bd875-111">Tenere presente, tuttavia, che nelle piattaforme a 16 bit il compilatore C considera un tipo enumerato come [**int**](int.md)a 16 bit. Pertanto, le applicazioni client a 16 bit devono convertire i tipi [**enum**](enum.md) in [**Long**](long.md) per la trasmissione remota, in modo da evitare la sovrascrittura dei dati o l'invio di valori non corretti.</span><span class="sxs-lookup"><span data-stu-id="bd875-111">Keep in mind, however, that on 16-bit platforms the C compiler treats an enumerated type as a 16-bit [**int**](int.md). Therefore 16-bit client applications need to convert [**enum**](enum.md) types to [**long**](long.md) for remote transmission in order to avoid overwriting data or sending incorrect values.</span></span>

## <a name="examples"></a><span data-ttu-id="bd875-112">Esempi</span><span class="sxs-lookup"><span data-stu-id="bd875-112">Examples</span></span>

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a><span data-ttu-id="bd875-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bd875-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd875-114">**enum**</span><span class="sxs-lookup"><span data-stu-id="bd875-114">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="bd875-115">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="bd875-115">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="bd875-116">**long**</span><span class="sxs-lookup"><span data-stu-id="bd875-116">**long**</span></span>](long.md)
</dt> </dl>

 

 




