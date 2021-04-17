---
description: L' \_ associazione della SOTTOSESSIONE Win32 definisce le relazioni tra le sessioni in cui una sessione fa parte o utilizza un'altra sessione, ad esempio quando una sessione terminal utilizza una sessione di accesso.
ms.assetid: 2269de22-b086-4f71-8b19-bc53e1c88dc7
ms.tgt_platform: multiple
title: Classe Win32_SubSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubSession
- Win32_SubSession.Antecedent
- Win32_SubSession.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 540cfb4c00b5df64e4ff11a1cc462eaed03be434
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524089"
---
# <a name="win32_subsession-class"></a><span data-ttu-id="eec03-103">\_Classe di SOTTOSESSIONE Win32</span><span class="sxs-lookup"><span data-stu-id="eec03-103">Win32\_SubSession class</span></span>

<span data-ttu-id="eec03-104">L' \_ associazione della SOTTOSESSIONE Win32 definisce le relazioni tra le sessioni in cui una sessione fa parte o utilizza un'altra sessione, ad esempio quando una sessione terminal utilizza una sessione di accesso.</span><span class="sxs-lookup"><span data-stu-id="eec03-104">The Win32\_SubSession association defines relationships between sessions where one session is a part of or utilizes another session for example where a Terminal session uses a Logon Session.</span></span>

<span data-ttu-id="eec03-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="eec03-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec03-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eec03-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SubSession : CIM_Dependency
{
  Win32_Session REF Antecedent;
  Win32_Session REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="eec03-107">Members</span><span class="sxs-lookup"><span data-stu-id="eec03-107">Members</span></span>

<span data-ttu-id="eec03-108">La classe della **\_ SOTTOSESSIONE Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="eec03-108">The **Win32\_SubSession** class has these types of members:</span></span>

-   [<span data-ttu-id="eec03-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eec03-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eec03-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eec03-110">Properties</span></span>

<span data-ttu-id="eec03-111">La classe della **\_ SOTTOSESSIONE Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="eec03-111">The **Win32\_SubSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eec03-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="eec03-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eec03-113">Tipo di dati **: \_ sessione Win32**</span><span class="sxs-lookup"><span data-stu-id="eec03-113">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="eec03-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eec03-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eec03-115">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) (precedente)</span><span class="sxs-lookup"><span data-stu-id="eec03-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="eec03-116">[**\_ Sessione Win32**](win32-session.md) che descrive la sessione in cui è presente una sottosessione.</span><span class="sxs-lookup"><span data-stu-id="eec03-116">A [**Win32\_Session**](win32-session.md) that describes the session that has a subsession.</span></span>

</dd> <dt>

<span data-ttu-id="eec03-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="eec03-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eec03-118">Tipo di dati **: \_ sessione Win32**</span><span class="sxs-lookup"><span data-stu-id="eec03-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="eec03-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eec03-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eec03-120">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) (dipendente)</span><span class="sxs-lookup"><span data-stu-id="eec03-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Dependent)</span></span>
</dt> </dl>

<span data-ttu-id="eec03-121">[**\_ Sessione Win32**](win32-session.md) che descrive la sessione che rappresenta la sottosessione.</span><span class="sxs-lookup"><span data-stu-id="eec03-121">A [**Win32\_Session**](win32-session.md) that describes the session that is the subsession.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eec03-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eec03-122">Requirements</span></span>



| <span data-ttu-id="eec03-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="eec03-123">Requirement</span></span> | <span data-ttu-id="eec03-124">Valore</span><span class="sxs-lookup"><span data-stu-id="eec03-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eec03-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eec03-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eec03-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eec03-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eec03-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eec03-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eec03-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eec03-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eec03-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eec03-129">Namespace</span></span><br/>                | <span data-ttu-id="eec03-130">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="eec03-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eec03-131">MOF</span><span class="sxs-lookup"><span data-stu-id="eec03-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eec03-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eec03-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eec03-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eec03-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eec03-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eec03-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec03-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eec03-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec03-136">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="eec03-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
