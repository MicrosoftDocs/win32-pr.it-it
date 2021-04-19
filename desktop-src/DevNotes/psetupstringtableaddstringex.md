---
description: Aggiunge una stringa e dati aggiuntivi a una tabella.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: pSetupStringTableAddStringEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326440"
---
# <a name="psetupstringtableaddstringex-function"></a><span data-ttu-id="2074b-103">pSetupStringTableAddStringEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="2074b-103">pSetupStringTableAddStringEx function</span></span>

<span data-ttu-id="2074b-104">\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="2074b-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="2074b-105">Aggiunge una stringa e dati aggiuntivi a una tabella.</span><span class="sxs-lookup"><span data-stu-id="2074b-105">Adds a string and extra data to a table.</span></span>

## <a name="syntax"></a><span data-ttu-id="2074b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2074b-106">Syntax</span></span>


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a><span data-ttu-id="2074b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2074b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2074b-108">*Un'STRINGTABLE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2074b-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2074b-109">Puntatore alla tabella delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="2074b-109">A pointer to the string table.</span></span>

</dd> <dt>

<span data-ttu-id="2074b-110">*Stringa* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2074b-110">*String* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2074b-111">Puntatore alla stringa da aggiungere alla tabella.</span><span class="sxs-lookup"><span data-stu-id="2074b-111">A pointer to string to be added to the table.</span></span>

</dd> <dt>

<span data-ttu-id="2074b-112">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2074b-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2074b-113">Il valore di questo parametro può essere `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .</span><span class="sxs-lookup"><span data-stu-id="2074b-113">The value of this parameter can be `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA`.</span></span>



| <span data-ttu-id="2074b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2074b-114">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="2074b-115">Significato</span><span class="sxs-lookup"><span data-stu-id="2074b-115">Meaning</span></span>                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <span data-ttu-id="2074b-116"><dt>**STRTAB \_ 0x001 \_ maiuscole/minuscole**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2074b-116"><dt>**STRTAB\_CASE\_SENSITIVE**</dt> <dt>0x001</dt></span></span> </dl> | <span data-ttu-id="2074b-117">La stringa fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2074b-117">String is case sensitive.</span></span><br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <span data-ttu-id="2074b-118"><dt>**STRTAB \_ NUOVO \_**</dt> <dt>0x004</dt> di dati</span><span class="sxs-lookup"><span data-stu-id="2074b-118"><dt>**STRTAB\_NEW\_EXTRADATA**</dt> <dt>0x004</dt></span></span> </dl>    | <span data-ttu-id="2074b-119">Sono presenti dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="2074b-119">There is extra data.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="2074b-120">*Dati* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2074b-120">*ExtraData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2074b-121">Puntatore facoltativo a un oggetto dati aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="2074b-121">A optional pointer to an extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="2074b-122">*ExtraDataSize* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2074b-122">*ExtraDataSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2074b-123">Dimensione dei dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="2074b-123">The size of the extra data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2074b-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="2074b-124">Remarks</span></span>

<span data-ttu-id="2074b-125">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2074b-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2074b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2074b-126">Requirements</span></span>



| <span data-ttu-id="2074b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2074b-127">Requirement</span></span> | <span data-ttu-id="2074b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2074b-128">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2074b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2074b-129">DLL</span></span><br/> | <dl> <span data-ttu-id="2074b-130"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2074b-130"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
