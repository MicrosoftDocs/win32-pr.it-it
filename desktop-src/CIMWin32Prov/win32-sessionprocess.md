---
description: La \_ classe WMI dell'associazione SessionProcess Win32 rappresenta un'associazione tra una sessione di accesso e i processi associati a tale sessione.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Classe Win32_SessionProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304470"
---
# <a name="win32_sessionprocess-class"></a><span data-ttu-id="97ac5-103">Win32 \_ SessionProcess (classe)</span><span class="sxs-lookup"><span data-stu-id="97ac5-103">Win32\_SessionProcess class</span></span>

<span data-ttu-id="97ac5-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SessionProcess Win32** rappresenta un'associazione tra una sessione di accesso e i processi associati a tale sessione.</span><span class="sxs-lookup"><span data-stu-id="97ac5-104">The **Win32\_SessionProcess** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between a logon session and the processes associated with that session.</span></span>

<span data-ttu-id="97ac5-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="97ac5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="97ac5-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="97ac5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="97ac5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97ac5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="97ac5-108">Members</span><span class="sxs-lookup"><span data-stu-id="97ac5-108">Members</span></span>

<span data-ttu-id="97ac5-109">La classe **Win32 \_ SessionProcess** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="97ac5-109">The **Win32\_SessionProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="97ac5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97ac5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97ac5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97ac5-111">Properties</span></span>

<span data-ttu-id="97ac5-112">La classe **Win32 \_ SessionProcess** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="97ac5-112">The **Win32\_SessionProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97ac5-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="97ac5-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97ac5-114">Tipo di dati: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="97ac5-114">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="97ac5-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97ac5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97ac5-116">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**chiave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="97ac5-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="97ac5-117">[**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) che rappresenta la sessione correlata al processo.</span><span class="sxs-lookup"><span data-stu-id="97ac5-117">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that represents the session which is related to the process.</span></span>

</dd> <dt>

<span data-ttu-id="97ac5-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="97ac5-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97ac5-119">Tipo di dati **: \_ processo Win32**</span><span class="sxs-lookup"><span data-stu-id="97ac5-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="97ac5-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97ac5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97ac5-121">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**chiave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="97ac5-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="97ac5-122">[**\_ Processo Win32**](win32-processor.md) che rappresenta il processo associato alla sessione.</span><span class="sxs-lookup"><span data-stu-id="97ac5-122">A [**Win32\_Process**](win32-processor.md) that represents the process associated with the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97ac5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="97ac5-123">Remarks</span></span>

<span data-ttu-id="97ac5-124">**Win32 \_ SessionProcess** restituisce tutte le sessioni per l'amministratore in caso di accesso con privilegi elevati o quando viene eseguito in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="97ac5-124">**Win32\_SessionProcess** returns all session for the administrator when logged in elevated or when run remotely.</span></span> <span data-ttu-id="97ac5-125">Si tratta di un'estensione del comportamento della classe.</span><span class="sxs-lookup"><span data-stu-id="97ac5-125">This is an extension to the behavior of the class.</span></span>

## <a name="requirements"></a><span data-ttu-id="97ac5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97ac5-126">Requirements</span></span>



| <span data-ttu-id="97ac5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="97ac5-127">Requirement</span></span> | <span data-ttu-id="97ac5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="97ac5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97ac5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97ac5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="97ac5-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97ac5-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97ac5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97ac5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="97ac5-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97ac5-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97ac5-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="97ac5-133">Namespace</span></span><br/>                | <span data-ttu-id="97ac5-134">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="97ac5-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="97ac5-135">MOF</span><span class="sxs-lookup"><span data-stu-id="97ac5-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97ac5-136"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97ac5-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="97ac5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="97ac5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97ac5-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97ac5-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97ac5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97ac5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ac5-140">**\_SessionResource Win32**</span><span class="sxs-lookup"><span data-stu-id="97ac5-140">**Win32\_SessionResource**</span></span>](win32-sessionresource.md)
</dt> <dt>

[<span data-ttu-id="97ac5-141">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="97ac5-141">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
