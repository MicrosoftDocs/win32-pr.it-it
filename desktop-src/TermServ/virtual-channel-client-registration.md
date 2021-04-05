---
title: Registrazione client del canale virtuale
description: È necessario archiviare il nome della DLL client nel registro di sistema.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727895"
---
# <a name="virtual-channel-client-registration"></a><span data-ttu-id="8e279-103">Registrazione client del canale virtuale</span><span class="sxs-lookup"><span data-stu-id="8e279-103">Virtual Channel Client Registration</span></span>

<span data-ttu-id="8e279-104">È necessario archiviare il nome della DLL client nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8e279-104">You must store the name of the client DLL in the registry.</span></span>

<span data-ttu-id="8e279-105">Nel registro di sistema aggiungere una sottochiave a una delle seguenti posizioni:</span><span class="sxs-lookup"><span data-stu-id="8e279-105">In the registry, add a subkey to one of the following locations:</span></span>

<span data-ttu-id="8e279-106">**HKEY \_ Software \_ utente corrente** \\  \\ **Microsoft** \\ **Terminal Server** \\  \\ **componenti aggiuntivi** predefiniti client</span><span class="sxs-lookup"><span data-stu-id="8e279-106">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**Addins**</span></span>

<span data-ttu-id="8e279-107">**HKEY \_ Software \_ utente corrente** \\ **software** \\ **Microsoft** \\ **Terminal Server** \\  \\ **componenti aggiuntivi** connessione client</span><span class="sxs-lookup"><span data-stu-id="8e279-107">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**connection**\\**Addins**</span></span>

> [!Note]  
> <span data-ttu-id="8e279-108">Nel percorso del registro di sistema, *Connection* rappresenta il nome di una connessione nella gestione connessione.</span><span class="sxs-lookup"><span data-stu-id="8e279-108">In the registry path, *connection* represents the name of a connection in Connection Manager.</span></span>

 

<span data-ttu-id="8e279-109">Le voci sotto il tasto **\\ \\ componenti aggiuntivi predefiniti** si applicano a tutte le connessioni.</span><span class="sxs-lookup"><span data-stu-id="8e279-109">Entries under the **\\Default\\Addins** key apply to all connections.</span></span> <span data-ttu-id="8e279-110">Le voci nella chiave dei **\\  \\ componenti aggiuntivi della connessione** si applicano solo alla connessione identificata dalla *connessione*.</span><span class="sxs-lookup"><span data-stu-id="8e279-110">Entries under the **\\***connection***\\Addins** key apply only to the connection identified by *connection*.</span></span> <span data-ttu-id="8e279-111">È possibile creare e gestire le connessioni mediante gestione connessione.</span><span class="sxs-lookup"><span data-stu-id="8e279-111">Connections can be created and managed by using Connection Manager.</span></span>

<span data-ttu-id="8e279-112">Alla sottochiave può essere assegnato qualsiasi nome.</span><span class="sxs-lookup"><span data-stu-id="8e279-112">The subkey can be given any name.</span></span> <span data-ttu-id="8e279-113">Deve contenere un valore **reg \_ SZ** o **reg \_ expand \_ SZ** e può includere facoltativamente un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8e279-113">It must contain a **REG\_SZ** or **REG\_EXPAND\_SZ** value and may optionally contain a **REG\_DWORD** value.</span></span> <span data-ttu-id="8e279-114">La sintassi del valore **reg \_ SZ** o **reg \_ expand \_ SZ** è la seguente.</span><span class="sxs-lookup"><span data-stu-id="8e279-114">The syntax of the **REG\_SZ** or **REG\_EXPAND\_SZ** value is as follows.</span></span>

``` syntax
Name = DLLname
```

<span data-ttu-id="8e279-115">Se **Name** è un valore **reg \_ expand \_ SZ** , può contenere variabili di ambiente non espanse che vengono espanse in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8e279-115">If **Name** is a **REG\_EXPAND\_SZ** value, it can contain unexpanded environment variables that are expanded at runtime.</span></span>

<span data-ttu-id="8e279-116">Il valore di *dllname* può essere un percorso completo.</span><span class="sxs-lookup"><span data-stu-id="8e279-116">The value of *DLLname* can be a fully qualified path.</span></span> <span data-ttu-id="8e279-117">Se *dllname* non contiene un percorso, viene utilizzata la strategia di ricerca dll standard.</span><span class="sxs-lookup"><span data-stu-id="8e279-117">If *DLLname* does not contain a path, the standard DLL search strategy is used.</span></span> <span data-ttu-id="8e279-118">Per ulteriori informazioni, vedere la sezione Osservazioni per [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="8e279-118">For more information, see the Remarks section for [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

 

 