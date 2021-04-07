---
description: Descrive la sessione di accesso o le sessioni associate a un utente connesso a un computer in cui è in esecuzione Windows.
ms.assetid: d09a115b-95a3-47c7-a04d-c810d044ccc8
ms.tgt_platform: multiple
title: Classe Win32_LogonSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSession
- Win32_LogonSession.Caption
- Win32_LogonSession.Description
- Win32_LogonSession.InstallDate
- Win32_LogonSession.Name
- Win32_LogonSession.Status
- Win32_LogonSession.StartTime
- Win32_LogonSession.AuthenticationPackage
- Win32_LogonSession.LogonId
- Win32_LogonSession.LogonType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78e14bbd41c2fd8bb0c10a7bfeeda0dc9d426b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747983"
---
# <a name="win32_logonsession-class"></a><span data-ttu-id="d3872-103">Win32 \_ LogonSession (classe)</span><span class="sxs-lookup"><span data-stu-id="d3872-103">Win32\_LogonSession class</span></span>

<span data-ttu-id="d3872-104">La classe WMI **Win32 \_ LogonSession** (vedere [recupero di una classe WMI](/windows/desktop/wmisdk/retrieving-a-class)) descrive la sessione di accesso o le sessioni associate a un utente connesso a un computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="d3872-104">The **Win32\_LogonSession** WMI class (see [Retrieving a WMI class](/windows/desktop/wmisdk/retrieving-a-class)) describes the logon session or sessions associated with a user logged on to a computer system running Windows.</span></span>

<span data-ttu-id="d3872-105">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d3872-105">The following syntax is simplified from Managed Object Format (MOF) code, and includes all of the inherited properties.</span></span> <span data-ttu-id="d3872-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d3872-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3872-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3872-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{9083C21E-7D58-4e0e-BC30-0BC8922AFB8B}"), AMENDMENT]
class Win32_LogonSession : Win32_Session
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
  string   AuthenticationPackage;
  string   LogonId;
  uint32   LogonType;
};
```

## <a name="members"></a><span data-ttu-id="d3872-108">Members</span><span class="sxs-lookup"><span data-stu-id="d3872-108">Members</span></span>

<span data-ttu-id="d3872-109">La classe **Win32 \_ LogonSession** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d3872-109">The **Win32\_LogonSession** class has these types of members:</span></span>

-   [<span data-ttu-id="d3872-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d3872-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3872-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d3872-111">Properties</span></span>

<span data-ttu-id="d3872-112">La classe **Win32 \_ LogonSession** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3872-112">The **Win32\_LogonSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3872-113">**AuthenticationPackage**</span><span class="sxs-lookup"><span data-stu-id="d3872-113">**AuthenticationPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3872-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3872-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3872-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3872-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3872-116">Nome del sottosistema usato per autenticare la sessione di accesso.</span><span class="sxs-lookup"><span data-stu-id="d3872-116">Name of the subsystem used to authenticate the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="d3872-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d3872-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3872-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3872-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3872-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3872-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3872-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d3872-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d3872-121">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d3872-121">A short textual description of the object.</span></span>

<span data-ttu-id="d3872-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d3872-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3872-123">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d3872-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3872-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3872-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3872-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3872-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3872-126">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d3872-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d3872-127">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d3872-127">A textual description of the object.</span></span>

<span data-ttu-id="d3872-128">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d3872-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3872-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d3872-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3872-130">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d3872-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d3872-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3872-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3872-132">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="d3872-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d3872-133">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="d3872-133">Indicates when the object was installed.</span></span> <span data-ttu-id="d3872-134">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="d3872-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d3872-135">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d3872-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3872-136">**IDaccesso**</span><span class="sxs-lookup"><span data-stu-id="d3872-136">**LogonId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3872-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3872-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3872-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3872-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3872-139">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d3872-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d3872-140">ID assegnato alla sessione di accesso.</span><span class="sxs-lookup"><span data-stu-id="d3872-140">ID assigned to the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="d3872-141">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="d3872-141">**LogonType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3872-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3872-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3872-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3872-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3872-144">Valore numerico che indica il tipo di sessione di accesso.</span><span class="sxs-lookup"><span data-stu-id="d3872-144">Numeric value that indicates the type of logon session.</span></span>

<dt>

<span data-ttu-id="d3872-145">0</span><span class="sxs-lookup"><span data-stu-id="d3872-145">0</span></span>
</dt> <dd>

<span data-ttu-id="d3872-146">Utilizzato solo dall'account di sistema.</span><span class="sxs-lookup"><span data-stu-id="d3872-146">Used only by the System account.</span></span>

</dd> <dt>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>

<span data-ttu-id="d3872-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="d3872-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interactive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-148">Destinato agli utenti che usano in modo interattivo il computer, ad esempio un utente che ha eseguito l'accesso da un server terminal, una shell remota o un processo simile.</span><span class="sxs-lookup"><span data-stu-id="d3872-148">Intended for users who are interactively using the machine, such as a user being logged on by a terminal server, remote shell, or similar process.</span></span>

</dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="d3872-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Rete** (3)</span><span class="sxs-lookup"><span data-stu-id="d3872-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Network** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-150">Destinata ai server ad alte prestazioni per l'autenticazione di password in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="d3872-150">Intended for high-performance servers to authenticate clear text passwords.</span></span> <span data-ttu-id="d3872-151">LogonUser non memorizza nella cache le credenziali per questo tipo di accesso.</span><span class="sxs-lookup"><span data-stu-id="d3872-151">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>

<span data-ttu-id="d3872-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)</span><span class="sxs-lookup"><span data-stu-id="d3872-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-153">Destinato ai server batch, in cui i processi possono essere eseguiti per conto di un utente senza l'intervento diretto; o per server con prestazioni più elevate che elaborano molti tentativi di autenticazione in testo non crittografato alla volta, ad esempio posta elettronica o server Web.</span><span class="sxs-lookup"><span data-stu-id="d3872-153">Intended for batch servers, where processes can be executed on behalf of a user without their direct intervention; or for higher performance servers that process many clear-text authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="d3872-154">LogonUser non memorizza nella cache le credenziali per questo tipo di accesso.</span><span class="sxs-lookup"><span data-stu-id="d3872-154">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d3872-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (5)</span><span class="sxs-lookup"><span data-stu-id="d3872-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-156">Indica un accesso del tipo di servizio.</span><span class="sxs-lookup"><span data-stu-id="d3872-156">Indicates a service-type logon.</span></span> <span data-ttu-id="d3872-157">Per l'account specificato deve essere abilitato il privilegio servizio.</span><span class="sxs-lookup"><span data-stu-id="d3872-157">The account provided must have the service privilege enabled.</span></span>

</dd> <dt>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>

<span data-ttu-id="d3872-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span><span class="sxs-lookup"><span data-stu-id="d3872-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-159">Indica un accesso di tipo proxy.</span><span class="sxs-lookup"><span data-stu-id="d3872-159">Indicates a proxy-type logon.</span></span>

</dd> <dt>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>

<span data-ttu-id="d3872-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Sblocco** (7)</span><span class="sxs-lookup"><span data-stu-id="d3872-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Unlock** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-161">Questo tipo di accesso è concepito per la registrazione delle DLL GINA sugli utenti che usano il computer in modo interattivo.</span><span class="sxs-lookup"><span data-stu-id="d3872-161">This logon type is intended for GINA DLLs logging on users who are interactively using the machine.</span></span> <span data-ttu-id="d3872-162">Questo tipo di accesso consente la generazione di un record di controllo univoco che indica quando la workstation è stata sbloccata.</span><span class="sxs-lookup"><span data-stu-id="d3872-162">This logon type allows a unique audit record to be generated that shows when the workstation was unlocked.</span></span>

</dd> <dt>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>

<span data-ttu-id="d3872-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span><span class="sxs-lookup"><span data-stu-id="d3872-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-164">Conserva il nome e la password nei pacchetti di autenticazione, consentendo al server di stabilire connessioni ad altri server di rete durante la rappresentazione del client.</span><span class="sxs-lookup"><span data-stu-id="d3872-164">Preserves the name and password in the authentication packages, allowing the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="d3872-165">Questo consente a un server di accettare le credenziali di testo non crittografato da un client, chiamare LogonUser, verificare che l'utente possa accedere al sistema attraverso la rete e comunicare comunque con altri server.</span><span class="sxs-lookup"><span data-stu-id="d3872-165">This allows a server to accept clear text credentials from a client, call LogonUser, verify that the user can access the system across the network, and still communicate with other servers.</span></span>

</dd> <dt>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>

<span data-ttu-id="d3872-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span><span class="sxs-lookup"><span data-stu-id="d3872-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-167">Consente al chiamante di clonare il token corrente e specificare nuove credenziali per le connessioni in uscita.</span><span class="sxs-lookup"><span data-stu-id="d3872-167">Allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="d3872-168">La nuova sessione di accesso ha la stessa identità locale, ma usa credenziali diverse per altre connessioni di rete.</span><span class="sxs-lookup"><span data-stu-id="d3872-168">The new logon session has the same local identify, but uses different credentials for other network connections.</span></span>

</dd> <dt>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>

<span data-ttu-id="d3872-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span><span class="sxs-lookup"><span data-stu-id="d3872-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-170">Sessione Servizi terminal che è sia remota che interattiva.</span><span class="sxs-lookup"><span data-stu-id="d3872-170">Terminal Services session that is both remote and interactive.</span></span>

</dd> <dt>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>

<span data-ttu-id="d3872-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span><span class="sxs-lookup"><span data-stu-id="d3872-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-172">Provare le credenziali memorizzate nella cache senza accedere alla rete.</span><span class="sxs-lookup"><span data-stu-id="d3872-172">Attempt cached credentials without accessing the network.</span></span>

</dd> <dt>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>

<span data-ttu-id="d3872-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span><span class="sxs-lookup"><span data-stu-id="d3872-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-174">Uguale a RemoteInteractive.</span><span class="sxs-lookup"><span data-stu-id="d3872-174">Same as RemoteInteractive.</span></span> <span data-ttu-id="d3872-175">Viene utilizzato per il controllo interno.</span><span class="sxs-lookup"><span data-stu-id="d3872-175">This is used for internal auditing.</span></span>

</dd> <dt>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>

<span data-ttu-id="d3872-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span><span class="sxs-lookup"><span data-stu-id="d3872-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d3872-177">Accesso alla workstation.</span><span class="sxs-lookup"><span data-stu-id="d3872-177">Workstation logon.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d3872-178">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d3872-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3872-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3872-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3872-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3872-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3872-181">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d3872-181">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d3872-182">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="d3872-182">Label by which the object is known.</span></span> <span data-ttu-id="d3872-183">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="d3872-183">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d3872-184">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d3872-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3872-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="d3872-185">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3872-186">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d3872-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d3872-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3872-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3872-188">Ora di inizio della sessione.</span><span class="sxs-lookup"><span data-stu-id="d3872-188">Time at which the session started.</span></span>

<span data-ttu-id="d3872-189">Questa proprietà viene ereditata [**dalla \_ sessione Win32**](win32-session.md).</span><span class="sxs-lookup"><span data-stu-id="d3872-189">This property is inherited from [**Win32\_Session**](win32-session.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3872-190">**Status**</span><span class="sxs-lookup"><span data-stu-id="d3872-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3872-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3872-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3872-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3872-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3872-193">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d3872-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d3872-194">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d3872-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="d3872-195">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="d3872-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d3872-196">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="d3872-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d3872-197">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="d3872-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d3872-198">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="d3872-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d3872-199">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="d3872-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d3872-200">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="d3872-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d3872-201">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d3872-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d3872-202">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="d3872-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d3872-203">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d3872-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d3872-204">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="d3872-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d3872-205">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="d3872-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d3872-206">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="d3872-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d3872-207">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="d3872-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d3872-208">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="d3872-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d3872-209">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="d3872-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d3872-210">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="d3872-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d3872-211">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="d3872-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d3872-212">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="d3872-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d3872-213">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="d3872-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d3872-214">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="d3872-214">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="d3872-215"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d3872-215"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="examples"></a><span data-ttu-id="d3872-216">Esempio</span><span class="sxs-lookup"><span data-stu-id="d3872-216">Examples</span></span>

<span data-ttu-id="d3872-217">L'esempio di [elenco di informazioni sulla sessione di accesso](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) di PowerShell restituisce informazioni sulle sessioni di accesso associate all'utente attualmente connesso a un computer.</span><span class="sxs-lookup"><span data-stu-id="d3872-217">The [List Logon Session Information](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) PowerShell sample returns information about logon sessions associated with the user currently logged on to a computer.</span></span>

<span data-ttu-id="d3872-218">Nell'esempio di PowerShell seguente viene verificata l'apertura di una sessione remota per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="d3872-218">The following PowerShell example checks for remote session open for a specified user.</span></span>


```PowerShell
$user = "<user name>"
$servers = gci servers.txt 

     foreach ($server in $servers){
     $logons = gwmi win32_loggedonuser -computername $server

          foreach ($logon in $logons){
               if ($logon.antecedent -match $user){
               $logonid = $logon.dependent.split("=")[1] 
               $session =gwmi win32_logonsession |? {$_.logonid -match $logonid}
               if ($session.logontype -eq "10"){
               Write-host "You have an active Terminal Server session on server $($server)"
                }
          }
```



## <a name="requirements"></a><span data-ttu-id="d3872-219">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3872-219">Requirements</span></span>



| <span data-ttu-id="d3872-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3872-220">Requirement</span></span> | <span data-ttu-id="d3872-221">Valore</span><span class="sxs-lookup"><span data-stu-id="d3872-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3872-222">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3872-222">Minimum supported client</span></span><br/> | <span data-ttu-id="d3872-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3872-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3872-224">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3872-224">Minimum supported server</span></span><br/> | <span data-ttu-id="d3872-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3872-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3872-226">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d3872-226">Namespace</span></span><br/>                | <span data-ttu-id="d3872-227">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d3872-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d3872-228">MOF</span><span class="sxs-lookup"><span data-stu-id="d3872-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3872-229"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3872-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3872-230">DLL</span><span class="sxs-lookup"><span data-stu-id="d3872-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3872-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3872-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3872-232">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3872-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3872-233">**\_Sessione Win32**</span><span class="sxs-lookup"><span data-stu-id="d3872-233">**Win32\_Session**</span></span>](win32-session.md)
</dt> <dt>

<span data-ttu-id="d3872-234">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3872-234">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

