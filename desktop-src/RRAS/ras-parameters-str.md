---
title: Struttura RAS_PARAMETERS (rassapi. h)
description: La \_ struttura dei parametri RAS viene utilizzata dalla funzione RasAdminPortGetInfo per restituire il nome e il valore di un parametro specifico del supporto associato a una porta su un server RAS.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS struttura RAS_PARAMETERS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518520"
---
# <a name="ras_parameters-structure"></a><span data-ttu-id="1d922-104">\_Struttura dei parametri RAS</span><span class="sxs-lookup"><span data-stu-id="1d922-104">RAS\_PARAMETERS structure</span></span>

<span data-ttu-id="1d922-105">\[La struttura dei **\_ parametri RAS** non è supportata a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="1d922-105">\[The **RAS\_PARAMETERS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="1d922-106">La struttura dei **\_ parametri RAS** viene utilizzata dalla funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) per restituire il nome e il valore di un parametro specifico del supporto associato a una porta su un server RAS.</span><span class="sxs-lookup"><span data-stu-id="1d922-106">The **RAS\_PARAMETERS** structure is used by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function to return the name and value of a media-specific parameter associated with a port on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d922-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d922-107">Syntax</span></span>


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="1d922-108">Members</span><span class="sxs-lookup"><span data-stu-id="1d922-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d922-109">**\_Tasto P**</span><span class="sxs-lookup"><span data-stu-id="1d922-109">**P\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="1d922-110">Specifica il nome della chiave che rappresenta il parametro specifico del supporto, ad esempio MAXCONNECTBPS.</span><span class="sxs-lookup"><span data-stu-id="1d922-110">Specifies the name of the key that represents the media-specific parameter, such as MAXCONNECTBPS.</span></span>

</dd> <dt>

<span data-ttu-id="1d922-111">**\_Tipo P**</span><span class="sxs-lookup"><span data-stu-id="1d922-111">**P\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="1d922-112">Identifica il tipo di dati associato al parametro.</span><span class="sxs-lookup"><span data-stu-id="1d922-112">Identifies the type of data associated with the parameter.</span></span> <span data-ttu-id="1d922-113">Questo membro può essere uno dei valori seguenti dall'enumerazione del [**\_ \_ formato RAS params**](ras-params-format-str.md) .</span><span class="sxs-lookup"><span data-stu-id="1d922-113">This member can be one of the following values from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration.</span></span>



| <span data-ttu-id="1d922-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1d922-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="1d922-115">Significato</span><span class="sxs-lookup"><span data-stu-id="1d922-115">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <span data-ttu-id="1d922-116"><dt>**ParamNumber**</dt></span><span class="sxs-lookup"><span data-stu-id="1d922-116"><dt>**ParamNumber**</dt></span></span> </dl> | <span data-ttu-id="1d922-117">Indica che i dati associati alla chiave sono numerici.</span><span class="sxs-lookup"><span data-stu-id="1d922-117">Indicates that the data associated with the key is a number.</span></span><br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <span data-ttu-id="1d922-118"><dt>**ParamString**</dt></span><span class="sxs-lookup"><span data-stu-id="1d922-118"><dt>**ParamString**</dt></span></span> </dl> | <span data-ttu-id="1d922-119">Indica che i dati associati alla chiave sono una stringa.</span><span class="sxs-lookup"><span data-stu-id="1d922-119">Indicates that the data associated with the key is a string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1d922-120">**\_Attributi P**</span><span class="sxs-lookup"><span data-stu-id="1d922-120">**P\_Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="1d922-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="1d922-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1d922-122">**\_Valore P**</span><span class="sxs-lookup"><span data-stu-id="1d922-122">**P\_Value**</span></span>
</dt> <dd>

<span data-ttu-id="1d922-123">Specifica il valore associato al parametro.</span><span class="sxs-lookup"><span data-stu-id="1d922-123">Specifies the value associated with the parameter.</span></span> <span data-ttu-id="1d922-124">Questo membro è un'Unione del [**\_ \_ valore params RAS**](ras-params-value-str.md) .</span><span class="sxs-lookup"><span data-stu-id="1d922-124">This member is a [**RAS\_PARAMS\_VALUE**](ras-params-value-str.md) union.</span></span> <span data-ttu-id="1d922-125">Se il membro di **\_ tipo P** è ParamNumber, il membro **Number** dell'Unione contiene il valore.</span><span class="sxs-lookup"><span data-stu-id="1d922-125">If the **P\_Type** member is ParamNumber, the **Number** member of the union contains the value.</span></span> <span data-ttu-id="1d922-126">Se **P \_ Type** è ParamString, il membro di **stringa** dell'Unione contiene il valore.</span><span class="sxs-lookup"><span data-stu-id="1d922-126">If **P\_Type** is ParamString, the **String** member of the union contains the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d922-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d922-127">Requirements</span></span>



| <span data-ttu-id="1d922-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d922-128">Requirement</span></span> | <span data-ttu-id="1d922-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1d922-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1d922-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d922-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1d922-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d922-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1d922-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d922-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1d922-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d922-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1d922-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1d922-134">End of client support</span></span><br/>    | <span data-ttu-id="1d922-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d922-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="1d922-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="1d922-136">End of server support</span></span><br/>    | <span data-ttu-id="1d922-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d922-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="1d922-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d922-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d922-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d922-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d922-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d922-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d922-141">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="1d922-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="1d922-142">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="1d922-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="1d922-143">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="1d922-143">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="1d922-144">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="1d922-144">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="1d922-145">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="1d922-145">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





