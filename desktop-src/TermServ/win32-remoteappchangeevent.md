---
title: Classe Win32_RemoteAppChangeEvent
description: Rappresenta una modifica alle impostazioni di Windows Server 2008 R2 RemoteApp nel server host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 3434ee4e-283e-4147-a73b-c131e8af6c57
ms.tgt_platform: multiple
keywords:
- Classe Win32_RemoteAppChangeEvent Servizi Desktop remoto
- Classe Win32_RemoteAppChangeEvent Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RemoteAppChangeEvent
- Win32_RemoteAppChangeEvent.SECURITY_DESCRIPTOR
- Win32_RemoteAppChangeEvent.TIME_CREATED
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5355d057038e97e9f381646134ff6487541f67f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119767"
---
# <a name="win32_remoteappchangeevent-class"></a><span data-ttu-id="53704-105">Win32 \_ RemoteAppChangeEvent (classe)</span><span class="sxs-lookup"><span data-stu-id="53704-105">Win32\_RemoteAppChangeEvent class</span></span>

<span data-ttu-id="53704-106">Rappresenta una modifica alle impostazioni di Windows Server 2008 R2 RemoteApp nel server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="53704-106">Represents a change to Windows Server 2008 R2 RemoteApp settings on the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="53704-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53704-107">Syntax</span></span>

``` syntax
class Win32_RemoteAppChangeEvent : ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="53704-108">Members</span><span class="sxs-lookup"><span data-stu-id="53704-108">Members</span></span>

<span data-ttu-id="53704-109">La classe **Win32 \_ RemoteAppChangeEvent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="53704-109">The **Win32\_RemoteAppChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="53704-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53704-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53704-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53704-111">Properties</span></span>

<span data-ttu-id="53704-112">La classe **Win32 \_ RemoteAppChangeEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="53704-112">The **Win32\_RemoteAppChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53704-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="53704-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53704-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="53704-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="53704-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="53704-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53704-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="53704-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="53704-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="53704-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="53704-118">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="53704-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="53704-119">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="53704-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53704-120">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="53704-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="53704-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="53704-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53704-122">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="53704-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="53704-123">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="53704-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="53704-124">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="53704-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="53704-125">Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="53704-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="53704-126">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53704-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53704-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="53704-127">Remarks</span></span>

<span data-ttu-id="53704-128">Per connettersi allo \\ \\ spazio dei nomi "root cimv2 TerminalServices", il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="53704-128">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="53704-129">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_**, che può essere impostato tramite la funzione com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="53704-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="53704-130">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="53704-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="53704-131">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="53704-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="53704-132">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="53704-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="53704-133">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="53704-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="53704-134">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="53704-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="53704-135">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="53704-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="53704-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53704-136">Requirements</span></span>



| <span data-ttu-id="53704-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="53704-137">Requirement</span></span> | <span data-ttu-id="53704-138">Valore</span><span class="sxs-lookup"><span data-stu-id="53704-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53704-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53704-139">Minimum supported client</span></span><br/> | <span data-ttu-id="53704-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="53704-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="53704-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53704-141">Minimum supported server</span></span><br/> | <span data-ttu-id="53704-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53704-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53704-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="53704-143">Namespace</span></span><br/>                | <span data-ttu-id="53704-144">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="53704-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="53704-145">MOF</span><span class="sxs-lookup"><span data-stu-id="53704-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53704-146"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53704-146"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="53704-147">DLL</span><span class="sxs-lookup"><span data-stu-id="53704-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53704-148"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53704-148"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

