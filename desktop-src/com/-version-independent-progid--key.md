---
title: Chiave ProgID indipendente dalla versione
description: Associa un ProgID a un CLSID. Questa chiave viene utilizzata per determinare la versione più recente di un'applicazione per oggetti.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474909"
---
# <a name="version-independent-progid-key"></a><span data-ttu-id="02e2f-104">Chiave ProgID indipendente dalla versione</span><span class="sxs-lookup"><span data-stu-id="02e2f-104">version-independent ProgID Key</span></span>

<span data-ttu-id="02e2f-105">Associa un ProgID a un CLSID.</span><span class="sxs-lookup"><span data-stu-id="02e2f-105">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="02e2f-106">Questa chiave viene utilizzata per determinare la versione più recente di un'applicazione per oggetti.</span><span class="sxs-lookup"><span data-stu-id="02e2f-106">This key is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="02e2f-107">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="02e2f-107">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a><span data-ttu-id="02e2f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="02e2f-108">Remarks</span></span>

<span data-ttu-id="02e2f-109">La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.</span><span class="sxs-lookup"><span data-stu-id="02e2f-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

<span data-ttu-id="02e2f-110">Il formato per <*ProgID indipendente dalla versione*> è <*program*>. <*componente*>, separato da punti, senza spazi e nessun numero di versione.</span><span class="sxs-lookup"><span data-stu-id="02e2f-110">The format for <*version-independent ProgID*> is <*program*>.<*component*>, separated by periods, no spaces, and no version number.</span></span> <span data-ttu-id="02e2f-111">Il ProgID indipendente dalla versione, come il ProgID, può essere registrato con un nome leggibile.</span><span class="sxs-lookup"><span data-stu-id="02e2f-111">The version-independent ProgID, like the ProgID, can be registered with a human-readable name.</span></span>

<span data-ttu-id="02e2f-112">*ProgID* è il ProgID della versione installata più recente della classe.</span><span class="sxs-lookup"><span data-stu-id="02e2f-112">*ProgID* is the ProgID of the latest installed version of the class.</span></span>

<span data-ttu-id="02e2f-113">Le applicazioni devono registrare un identificatore programmatico indipendente dalla versione sotto la chiave *ProgID indipendente dalla versione* .</span><span class="sxs-lookup"><span data-stu-id="02e2f-113">Applications must register a version-independent programmatic identifier under the *version-independent ProgID* key.</span></span> <span data-ttu-id="02e2f-114">Il ProgID indipendente dalla versione si riferisce alla classe dell'applicazione e non passa da una versione all'altra, rimanendo invece costante in tutte le versionsâ € ", ad esempio, il documento di Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="02e2f-114">The version-independent ProgID refers to the application's class and does not change from version to version, instead remaining constant across all versionsâ€”for example, Microsoft Word Document.</span></span> <span data-ttu-id="02e2f-115">Viene usato con i linguaggi macro e si riferisce alla versione attualmente installata della classe dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="02e2f-115">It is used with macro languages and refers to the currently installed version of the application's class.</span></span> <span data-ttu-id="02e2f-116">Il ProgID indipendente dalla versione deve corrispondere al nome della versione più recente dell'applicazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="02e2f-116">The version-independent ProgID must correspond to the name of the latest version of the object application.</span></span>

<span data-ttu-id="02e2f-117">Ad esempio, il ProgID indipendente dalla versione viene utilizzato quando un'applicazione contenitore crea un grafico o una tabella con un pulsante della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="02e2f-117">For example, the version-independent ProgID is used when a container application creates a chart or table with a toolbar button.</span></span> <span data-ttu-id="02e2f-118">In questa situazione, l'applicazione può utilizzare il ProgID indipendente dalla versione per determinare la versione più recente dell'applicazione oggetto necessaria.</span><span class="sxs-lookup"><span data-stu-id="02e2f-118">In this situation, the application can use the version-independent ProgID to determine the latest version of the needed object application.</span></span>

<span data-ttu-id="02e2f-119">Il ProgID indipendente dalla versione viene archiviato e gestito esclusivamente dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="02e2f-119">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="02e2f-120">Quando viene specificato il ProgID indipendente dalla versione, la funzione [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) restituisce il CLSID della versione corrente.</span><span class="sxs-lookup"><span data-stu-id="02e2f-120">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="02e2f-121">È possibile usare [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) per eseguire la conversione tra queste due rappresentazioni.</span><span class="sxs-lookup"><span data-stu-id="02e2f-121">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

<span data-ttu-id="02e2f-122">È possibile usare [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) o [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) per modificare l'identificatore in una stringa visualizzabile.</span><span class="sxs-lookup"><span data-stu-id="02e2f-122">You can use [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) or [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) to change the identifier to a displayable string.</span></span>

<span data-ttu-id="02e2f-123">Se non viene usato un gestore personalizzato, la voce deve essere impostata su OLE32.DLL, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="02e2f-123">If a custom handler is not used, the entry should be set to OLE32.DLL, as shown in the following example:</span></span>

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a><span data-ttu-id="02e2f-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02e2f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02e2f-125">**CLSIDFromProgID**</span><span class="sxs-lookup"><span data-stu-id="02e2f-125">**CLSIDFromProgID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[<span data-ttu-id="02e2f-126">**ProgIDFromCLSID**</span><span class="sxs-lookup"><span data-stu-id="02e2f-126">**ProgIDFromCLSID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<span data-ttu-id="02e2f-127"><ProgID> Chiave</span><span class="sxs-lookup"><span data-stu-id="02e2f-127"><ProgID> Key</span></span>](-progid--key.md)
</dt> </dl>

 

 




