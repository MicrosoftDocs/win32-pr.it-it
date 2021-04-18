---
description: La funzione LoadDWORD viene chiamata dal monitoraggio per impostare una variabile DWORD con un valore tratto da una variabile di stringa di configurazione HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Funzione LoadDWORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318971"
---
# <a name="loaddword-function"></a><span data-ttu-id="f4165-103">LoadDWORD (funzione)</span><span class="sxs-lookup"><span data-stu-id="f4165-103">LoadDWORD function</span></span>

<span data-ttu-id="f4165-104">La funzione **LoadDWORD** viene chiamata dal monitoraggio per impostare una variabile **DWORD** con un valore tratto da una variabile di stringa di configurazione HTML.</span><span class="sxs-lookup"><span data-stu-id="f4165-104">The **LoadDWORD** function is called by the monitor to set a **DWORD** variable with a value taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4165-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4165-105">Syntax</span></span>


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="f4165-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4165-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4165-107">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4165-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4165-108">Puntatore alla stringa di configurazione HTML passata al monitoraggio tramite il metodo [Imonitor::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="f4165-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f4165-109">*pVarName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4165-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4165-110">Puntatore al nome della variabile nella stringa di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f4165-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="f4165-111">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4165-111">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4165-112">Puntatore alla variabile **DWORD** impostata sul valore della variabile della stringa di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f4165-112">Pointer to the **DWORD** variable that is set to the value of the configuration string variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4165-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4165-113">Return value</span></span>

<span data-ttu-id="f4165-114">Se la funzione ha esito positivo (se il nome della variabile è stato trovato e ha una stringa di lunghezza diversa da zero), viene inserito il valore **DWORD** e il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="f4165-114">If the function is successful (if the variable name was found and had a non-zero-length string), the **DWORD** is inserted, and the return value is **TRUE**.</span></span>

<span data-ttu-id="f4165-115">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="f4165-115">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4165-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4165-116">Requirements</span></span>



| <span data-ttu-id="f4165-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4165-117">Requirement</span></span> | <span data-ttu-id="f4165-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f4165-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f4165-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4165-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f4165-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f4165-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f4165-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4165-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f4165-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f4165-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f4165-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4165-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4165-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4165-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f4165-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f4165-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4165-126"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4165-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f4165-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f4165-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4165-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4165-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




