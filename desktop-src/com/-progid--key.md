---
title: Chiave ProgID
description: Un identificatore a livello di codice (ProgID) è una voce del registro di sistema che può essere associata a un CLSID. Analogamente al CLSID, ProgID identifica una classe ma con minore precisione perché non è garantita l'univocità globale.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047730"
---
# <a name="progid-key"></a><span data-ttu-id="03957-104">Chiave ProgID</span><span class="sxs-lookup"><span data-stu-id="03957-104">ProgID Key</span></span>

<span data-ttu-id="03957-105">Un identificatore a livello di codice (ProgID) è una voce del registro di sistema che può essere associata a un CLSID.</span><span class="sxs-lookup"><span data-stu-id="03957-105">A programmatic identifier (ProgID) is a registry entry that can be associated with a CLSID.</span></span> <span data-ttu-id="03957-106">Analogamente al CLSID, ProgID identifica una classe ma con minore precisione perché non è garantita l'univocità globale.</span><span class="sxs-lookup"><span data-stu-id="03957-106">Like the CLSID, the ProgID identifies a class but with less precision because it is not guaranteed to be globally unique.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="03957-107">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="03957-107">Registry Entry</span></span>

<span data-ttu-id="03957-108">**HKEY \_ \_ \\ \\ Classi software del computer locale** \\ *{* ProgID *}*</span><span class="sxs-lookup"><span data-stu-id="03957-108">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**\\ *{* ProgID *}*</span></span>



| <span data-ttu-id="03957-109">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="03957-109">Registry key</span></span>                            | <span data-ttu-id="03957-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03957-110">Description</span></span>                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="03957-111">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="03957-111">**CLSID**</span></span>](clsid.md)                  | <span data-ttu-id="03957-112">Associa un ProgID a un CLSID.</span><span class="sxs-lookup"><span data-stu-id="03957-112">Associates a ProgID with a CLSID.</span></span>                                  |
| [<span data-ttu-id="03957-113">**Inseribile**</span><span class="sxs-lookup"><span data-stu-id="03957-113">**Insertable**</span></span>](insertable-progid.md) | <span data-ttu-id="03957-114">Indica che questa classe è inseribile nei contenitori OLE 2.</span><span class="sxs-lookup"><span data-stu-id="03957-114">Indicates that this class is insertable in OLE 2 containers.</span></span>       |
| [<span data-ttu-id="03957-115">**Protocollo**</span><span class="sxs-lookup"><span data-stu-id="03957-115">**Protocol**</span></span>](protocol.md)            | <span data-ttu-id="03957-116">Indica che questa classe OLE 2 è inseribile nei contenitori OLE 1.</span><span class="sxs-lookup"><span data-stu-id="03957-116">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span> |
| [<span data-ttu-id="03957-117">**Shell**</span><span class="sxs-lookup"><span data-stu-id="03957-117">**Shell**</span></span>](shell.md)                  | <span data-ttu-id="03957-118">Fornisce informazioni sulla stampa della shell di Windows 3,1 e sui **file aperti** .</span><span class="sxs-lookup"><span data-stu-id="03957-118">Provides Windows 3.1 shell printing and **File Open** information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="03957-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="03957-119">Remarks</span></span>

<span data-ttu-id="03957-120">È possibile usare un ProgID in situazioni di programmazione in cui non è possibile usare un CLSID.</span><span class="sxs-lookup"><span data-stu-id="03957-120">You can use a ProgID in programming situations where it is not possible to use a CLSID.</span></span> <span data-ttu-id="03957-121">I ProgID non devono essere visualizzati nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="03957-121">ProgIDs should not appear in the user interface.</span></span> <span data-ttu-id="03957-122">Non è garantito che i ProgID siano univoci, quindi possono essere usati solo quando i conflitti di nomi sono gestibili.</span><span class="sxs-lookup"><span data-stu-id="03957-122">ProgIDs are not guaranteed to be unique, so they can be used only where name collisions are manageable.</span></span>

<span data-ttu-id="03957-123">Il formato di un ProgID è <*Program*>. <*Component*>. <*versione*>, separati da punti e senza spazi, come in Word.Document. 6.</span><span class="sxs-lookup"><span data-stu-id="03957-123">The format of a ProgID is <*Program*>.<*Component*>.<*Version*>, separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="03957-124">Il ProgID deve essere conforme ai requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="03957-124">The ProgID must comply with the following requirements:</span></span>

-   <span data-ttu-id="03957-125">Non sono presenti più di 39 caratteri.</span><span class="sxs-lookup"><span data-stu-id="03957-125">Have no more than 39 characters.</span></span>
-   <span data-ttu-id="03957-126">Non contengono segni di punteggiatura (inclusi i caratteri di sottolineatura) tranne uno o più punti.</span><span class="sxs-lookup"><span data-stu-id="03957-126">Contain no punctuation (including underscores) except one or more periods.</span></span>
-   <span data-ttu-id="03957-127">Non iniziare con una cifra.</span><span class="sxs-lookup"><span data-stu-id="03957-127">Not start with a digit.</span></span>
-   <span data-ttu-id="03957-128">Essere diverso dal nome della classe di qualsiasi applicazione OLE 1, inclusa la versione OLE 1 della stessa applicazione, se presente.</span><span class="sxs-lookup"><span data-stu-id="03957-128">Be different from the class name of any OLE 1 application, including the OLE 1 version of the same application, if there is one.</span></span>

<span data-ttu-id="03957-129">Poiché il ProgID non dovrebbe essere visualizzato nell'interfaccia utente, è possibile ottenere un nome visualizzabile chiamando [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span><span class="sxs-lookup"><span data-stu-id="03957-129">Because the ProgID should not appear in the user interface, you can obtain a displayable name by calling [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span></span> <span data-ttu-id="03957-130">Vedere anche [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="03957-130">Also, see [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span>

<span data-ttu-id="03957-131">La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.</span><span class="sxs-lookup"><span data-stu-id="03957-131">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03957-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03957-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03957-133">**IOleObject:: GetUserType**</span><span class="sxs-lookup"><span data-stu-id="03957-133">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[<span data-ttu-id="03957-134">**OleRegGetUserType**</span><span class="sxs-lookup"><span data-stu-id="03957-134">**OleRegGetUserType**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




