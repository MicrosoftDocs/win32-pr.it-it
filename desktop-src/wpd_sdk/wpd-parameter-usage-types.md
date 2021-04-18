---
description: Il \_ \_ \_ tipo di enumerazione dei tipi di utilizzo del parametro WPD descrive la modalità di utilizzo di un parametro di metodo in un determinato metodo.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: Enumerazione WPD_PARAMETER_USAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326953"
---
# <a name="wpd_parameter_usage_types-enumeration"></a><span data-ttu-id="a9cb0-103">Enumerazione per i tipi di utilizzo del \_ parametro WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="a9cb0-103">WPD\_PARAMETER\_USAGE\_TYPES enumeration</span></span>

<span data-ttu-id="a9cb0-104">Il tipo di enumerazione dei [**\_ tipi di \_ utilizzo \_ del parametro WPD**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) descrive la modalità di utilizzo di un parametro di metodo in un determinato metodo.</span><span class="sxs-lookup"><span data-stu-id="a9cb0-104">The [**WPD\_PARAMETER\_USAGE\_TYPES**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) enumeration type describes how a method parameter is used in a given method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9cb0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9cb0-105">Syntax</span></span>


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="a9cb0-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="a9cb0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a9cb0-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_restituzione \_ utilizzo parametri WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a9cb0-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**WPD\_PARAMETER\_USAGE\_RETURN**</span></span>
</dt> <dd>

<span data-ttu-id="a9cb0-108">Il parametro riceve il valore restituito, se specificato dal metodo.</span><span class="sxs-lookup"><span data-stu-id="a9cb0-108">The parameter receives the return value, if specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="a9cb0-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_utilizzo parametri \_ WPD \_ in**</span><span class="sxs-lookup"><span data-stu-id="a9cb0-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**WPD\_PARAMETER\_USAGE\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="a9cb0-110">Il parametro contiene un valore di input prima della chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="a9cb0-110">The parameter contains an input value before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="a9cb0-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**\_utilizzo parametri \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a9cb0-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**WPD\_PARAMETER\_USAGE\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="a9cb0-112">Il parametro contiene un valore di output quando il metodo restituisce.</span><span class="sxs-lookup"><span data-stu-id="a9cb0-112">The parameter contains an output value when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="a9cb0-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_utilizzo del parametro WPD \_ \_ InOut**</span><span class="sxs-lookup"><span data-stu-id="a9cb0-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**WPD\_PARAMETER\_USAGE\_INOUT**</span></span>
</dt> <dd>

<span data-ttu-id="a9cb0-114">Il parametro contiene un valore di input prima che venga chiamato il metodo e un valore di output quando viene restituito.</span><span class="sxs-lookup"><span data-stu-id="a9cb0-114">The parameter contains an input value before the method is called and an output value when it returns.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9cb0-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9cb0-115">Requirements</span></span>



| <span data-ttu-id="a9cb0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9cb0-116">Requirement</span></span> | <span data-ttu-id="a9cb0-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a9cb0-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9cb0-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9cb0-118">Header</span></span><br/> | <dl> <span data-ttu-id="a9cb0-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9cb0-119"><dt>PortableDevice.h</dt></span></span> </dl> |



 

