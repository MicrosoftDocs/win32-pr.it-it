---
description: La funzione CreateHandoffTable crea una tabella che include le informazioni sul set di continuità archiviate nel file INI del parser.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Funzione CreateHandoffTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311629"
---
# <a name="createhandofftable-function"></a><span data-ttu-id="b4c9e-103">CreateHandoffTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="b4c9e-103">CreateHandoffTable function</span></span>

<span data-ttu-id="b4c9e-104">La funzione **CreateHandoffTable** crea una [*tabella*](h.md) che include le informazioni sul set di continuità archiviate nel file ini del parser.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-104">The **CreateHandoffTable** function creates a [*handoff table*](h.md) that includes the handoff set information stored in the INI file of the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4c9e-105">Syntax</span></span>


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a><span data-ttu-id="b4c9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4c9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4c9e-107">*Secname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4c9e-107">*secName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c9e-108">Stringa che indica la sezione del file INI in cui si trovano le informazioni sul set di continuità.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-108">String that indicates the section of the INI file where the handoff set information is located.</span></span>

</dd> <dt>

<span data-ttu-id="b4c9e-109">*iniFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4c9e-109">*iniFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c9e-110">Stringa che include il nome del file INI del parser.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-110">String that includes the name of the parser INI file.</span></span>

</dd> <dt>

<span data-ttu-id="b4c9e-111">*hTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b4c9e-111">*hTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c9e-112">Handle per una struttura **HANDOFFTABLE** creata e gestita da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-112">Handle to a **HANDOFFTABLE** structure created and maintained by Network Monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b4c9e-113">*nMaxProtocolEntries* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4c9e-113">*nMaxProtocolEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c9e-114">Numero che specifica il numero massimo di voci che possono essere elaborate dalla tabella di continuità.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-114">Number that specifies the maximum number of entries that the handoff table can process.</span></span>

</dd> <dt>

<span data-ttu-id="b4c9e-115">di *base* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4c9e-115">*base* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c9e-116">Base numerica dei numeri di set di continuità archiviati nel file INI.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-116">Numerical base of handoff set numbers stored in the INI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4c9e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4c9e-117">Return value</span></span>

<span data-ttu-id="b4c9e-118">Se la funzione ha esito positivo, il valore restituito è il numero di voci nella tabella con continuità.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-118">If the function is successful, the return value is the number of entries in the handoff table.</span></span>

<span data-ttu-id="b4c9e-119">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-119">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4c9e-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4c9e-120">Remarks</span></span>

<span data-ttu-id="b4c9e-121">La tabella uniforme creata da Network Monitor si basa sulle informazioni fornite nell'INI del parser.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-121">The handoff table created by Network Monitor is based on information provided in the parser INI.</span></span> <span data-ttu-id="b4c9e-122">Per ottenere un handle per uno dei protocolli inclusi nella tabella, è quindi possibile usare l'handle restituito alla tabella di continuità.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-122">The returned handle to the handoff table can then be used to obtain a handle to one of the protocols included in the table.</span></span> <span data-ttu-id="b4c9e-123">Per ottenere un handle di uno di questi protocolli, chiamare [GetProtocolFromTable](getprotocolfromtable.md).</span><span class="sxs-lookup"><span data-stu-id="b4c9e-123">To obtain a handle of one of these protocols, call [GetProtocolFromTable](getprotocolfromtable.md).</span></span>

<span data-ttu-id="b4c9e-124">Si noti che l'applicazione del parser non accede mai direttamente alla struttura **HANDOFFTABLE** .</span><span class="sxs-lookup"><span data-stu-id="b4c9e-124">Notice that the parser application never accesses the **HANDOFFTABLE** structure directly.</span></span> <span data-ttu-id="b4c9e-125">Questa struttura viene creata e gestita da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="b4c9e-125">This structure is created and maintained by Network Monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4c9e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4c9e-126">Requirements</span></span>



| <span data-ttu-id="b4c9e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4c9e-127">Requirement</span></span> | <span data-ttu-id="b4c9e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b4c9e-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c9e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4c9e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b4c9e-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b4c9e-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b4c9e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4c9e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b4c9e-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b4c9e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b4c9e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4c9e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4c9e-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4c9e-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b4c9e-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="b4c9e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4c9e-136"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4c9e-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b4c9e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b4c9e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4c9e-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4c9e-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4c9e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4c9e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c9e-140">GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="b4c9e-140">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> <dt>

[<span data-ttu-id="b4c9e-141">HANDOFFTABLE</span><span class="sxs-lookup"><span data-stu-id="b4c9e-141">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




