---
description: Converte l'ora locale del computer in Coordinated Universal Time (ora di Greenwich).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Utilities. LocalTimeToUTCTime, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323942"
---
# <a name="utilitieslocaltimetoutctime-method"></a><span data-ttu-id="39819-103">Utilities. LocalTimeToUTCTime, metodo</span><span class="sxs-lookup"><span data-stu-id="39819-103">Utilities.LocalTimeToUTCTime method</span></span>

<span data-ttu-id="39819-104">\[Il metodo **LocalTimeToUTCTime** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]</span><span class="sxs-lookup"><span data-stu-id="39819-104">\[The **LocalTimeToUTCTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="39819-105">Il metodo **LocalTimeToUTCTime** converte l'ora locale del computer in Coordinated Universal Time (ora di Greenwich).</span><span class="sxs-lookup"><span data-stu-id="39819-105">The **LocalTimeToUTCTime** method converts the computer's local time to Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="syntax"></a><span data-ttu-id="39819-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39819-106">Syntax</span></span>


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a><span data-ttu-id="39819-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="39819-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39819-108">*Localtime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39819-108">*LocalTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39819-109">Ora locale da convertire nell'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="39819-109">The local time to be converted to Coordinated Universal Time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39819-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39819-110">Return value</span></span>

<span data-ttu-id="39819-111">Ora UTC (Coordinated Universal Time) corrispondente all'ora locale specificata.</span><span class="sxs-lookup"><span data-stu-id="39819-111">The Coordinated Universal Time that corresponds to the specified local time.</span></span>

## <a name="remarks"></a><span data-ttu-id="39819-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="39819-112">Remarks</span></span>

<span data-ttu-id="39819-113">Sebbene il sistema usi internamente l'ora UTC (Coordinated Universal Time), in genere le applicazioni visualizzano l'ora locale, ovvero la data e l'ora del giorno per il fuso orario locale del computer.</span><span class="sxs-lookup"><span data-stu-id="39819-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="39819-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39819-114">Requirements</span></span>



| <span data-ttu-id="39819-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="39819-115">Requirement</span></span> | <span data-ttu-id="39819-116">Valore</span><span class="sxs-lookup"><span data-stu-id="39819-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39819-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="39819-117">Redistributable</span></span><br/> | <span data-ttu-id="39819-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="39819-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="39819-119">DLL</span><span class="sxs-lookup"><span data-stu-id="39819-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="39819-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39819-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39819-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39819-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39819-122">**Utilità**</span><span class="sxs-lookup"><span data-stu-id="39819-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




