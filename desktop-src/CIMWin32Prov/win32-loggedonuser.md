---
description: La \_ classe WMI dell'associazione LoggedOnUser Win32 mette in relazione una sessione e un account utente.
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Classe Win32_LoggedOnUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f851c85563095a66197b0dde8e6cbddc9581f07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878234"
---
# <a name="win32_loggedonuser-class"></a><span data-ttu-id="64be8-103">Win32 \_ LoggedOnUser (classe)</span><span class="sxs-lookup"><span data-stu-id="64be8-103">Win32\_LoggedOnUser class</span></span>

<span data-ttu-id="64be8-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LoggedOnUser Win32** mette in relazione una sessione e un account utente.</span><span class="sxs-lookup"><span data-stu-id="64be8-104">The **Win32\_LoggedOnUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a session and a user account.</span></span>

<span data-ttu-id="64be8-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="64be8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="64be8-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="64be8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="64be8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64be8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="64be8-108">Members</span><span class="sxs-lookup"><span data-stu-id="64be8-108">Members</span></span>

<span data-ttu-id="64be8-109">La classe **Win32 \_ LoggedOnUser** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="64be8-109">The **Win32\_LoggedOnUser** class has these types of members:</span></span>

-   [<span data-ttu-id="64be8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="64be8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64be8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="64be8-111">Properties</span></span>

<span data-ttu-id="64be8-112">La classe **Win32 \_ LoggedOnUser** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="64be8-112">The **Win32\_LoggedOnUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64be8-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="64be8-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64be8-114">Tipo di dati **: \_ account Win32**</span><span class="sxs-lookup"><span data-stu-id="64be8-114">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="64be8-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64be8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64be8-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (precedente), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="64be8-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="64be8-117">[**\_ Account Win32**](win32-account.md) che descrive l'account utilizzato nell'avvio della sessione.</span><span class="sxs-lookup"><span data-stu-id="64be8-117">A [**Win32\_Account**](win32-account.md) that describes the account used in the initiation of this session.</span></span> <span data-ttu-id="64be8-118">L'account può essere un account utente o un account di sistema.</span><span class="sxs-lookup"><span data-stu-id="64be8-118">The account could be either a user account or a system account.</span></span>

</dd> <dt>

<span data-ttu-id="64be8-119">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="64be8-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64be8-120">Tipo di dati: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="64be8-120">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="64be8-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64be8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64be8-122">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (dipendente), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="64be8-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="64be8-123">[**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) che descrive la sessione attualmente utilizzata dall'account.</span><span class="sxs-lookup"><span data-stu-id="64be8-123">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that describes the session that the account is currently using.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64be8-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="64be8-124">Remarks</span></span>

<span data-ttu-id="64be8-125">La classe **Win32 \_ LoggedOnUser** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="64be8-125">The **Win32\_LoggedOnUser** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="examples"></a><span data-ttu-id="64be8-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="64be8-126">Examples</span></span>

<span data-ttu-id="64be8-127">L'esempio di PowerShell per la [funzione Get-loggedonuser](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) ottiene gli utenti connessi in un computer locale o remoto, con le informazioni sulla sessione.</span><span class="sxs-lookup"><span data-stu-id="64be8-127">The [get-loggedonuser function](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) PowerShell sample gets the logged on users on a local or remote computer, with session information.</span></span>

## <a name="requirements"></a><span data-ttu-id="64be8-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64be8-128">Requirements</span></span>



| <span data-ttu-id="64be8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="64be8-129">Requirement</span></span> | <span data-ttu-id="64be8-130">Valore</span><span class="sxs-lookup"><span data-stu-id="64be8-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64be8-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64be8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="64be8-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64be8-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64be8-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64be8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="64be8-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64be8-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64be8-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="64be8-135">Namespace</span></span><br/>                | <span data-ttu-id="64be8-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="64be8-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64be8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="64be8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64be8-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64be8-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64be8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="64be8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64be8-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64be8-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64be8-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64be8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64be8-142">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="64be8-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="64be8-143">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64be8-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

