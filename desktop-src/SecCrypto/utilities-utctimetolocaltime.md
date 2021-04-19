---
description: Converte l'ora UTC (Coordinated Universal Time) nell'ora locale del computer.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Utilities. UTCTimeToLocalTime, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323941"
---
# <a name="utilitiesutctimetolocaltime-method"></a><span data-ttu-id="a5d68-103">Utilities. UTCTimeToLocalTime, metodo</span><span class="sxs-lookup"><span data-stu-id="a5d68-103">Utilities.UTCTimeToLocalTime method</span></span>

<span data-ttu-id="a5d68-104">\[Il metodo **UTCTimeToLocalTime** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]</span><span class="sxs-lookup"><span data-stu-id="a5d68-104">\[The **UTCTimeToLocalTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="a5d68-105">Il metodo **UTCTimeToLocalTime** converte l'ora UTC (Coordinated Universal Time) nell'ora locale del computer.</span><span class="sxs-lookup"><span data-stu-id="a5d68-105">The **UTCTimeToLocalTime** method converts Coordinated Universal Time (Greenwich Mean Time) to the computer's local time.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d68-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5d68-106">Syntax</span></span>


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a><span data-ttu-id="a5d68-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5d68-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5d68-108">*UTCTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5d68-108">*UTCTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5d68-109">Ora UTC (Coordinated Universal Time) da convertire nell'ora locale del computer.</span><span class="sxs-lookup"><span data-stu-id="a5d68-109">The Coordinated Universal Time to be converted to the computer's local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5d68-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5d68-110">Return value</span></span>

<span data-ttu-id="a5d68-111">Ora locale corrispondente all'ora UTC (Coordinated Universal Time) specificata.</span><span class="sxs-lookup"><span data-stu-id="a5d68-111">The local time that corresponds to the specified Coordinated Universal Time.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5d68-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5d68-112">Remarks</span></span>

<span data-ttu-id="a5d68-113">Sebbene il sistema usi internamente l'ora UTC (Coordinated Universal Time), in genere le applicazioni visualizzano l'ora locale, ovvero la data e l'ora del giorno per il fuso orario locale del computer.</span><span class="sxs-lookup"><span data-stu-id="a5d68-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5d68-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5d68-114">Requirements</span></span>



| <span data-ttu-id="a5d68-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d68-115">Requirement</span></span> | <span data-ttu-id="a5d68-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a5d68-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d68-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a5d68-117">Redistributable</span></span><br/> | <span data-ttu-id="a5d68-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="a5d68-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a5d68-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a5d68-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="a5d68-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5d68-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d68-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5d68-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d68-122">**Utilità**</span><span class="sxs-lookup"><span data-stu-id="a5d68-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




