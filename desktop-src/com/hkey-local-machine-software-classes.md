---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: Le sottochiavi e i valori del registro di sistema associati alla \_ \_ chiave delle classi software del computer locale HKEY \\ \\ contengono informazioni su un'applicazione necessaria per supportare la funzionalità com.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c16fdbc97b32d01af9c96b5670cb5a19c09c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714098"
---
# <a name="hkey_local_machinesoftwareclasses"></a><span data-ttu-id="0e14e-103">\_ \_ Classi software del computer locale \\ HKEY \\</span><span class="sxs-lookup"><span data-stu-id="0e14e-103">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes</span></span>

<span data-ttu-id="0e14e-104">Le sottochiavi e i valori del registro di sistema associati alla chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** contengono informazioni su un'applicazione necessaria per supportare la funzionalità com.</span><span class="sxs-lookup"><span data-stu-id="0e14e-104">The subkeys and registry values associated with the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key contain information about an application that is needed to support COM functionality.</span></span> <span data-ttu-id="0e14e-105">Queste informazioni includono argomenti quali i formati di dati supportati, le informazioni sulla compatibilità, gli identificatori programmatici, DCOM e i controlli.</span><span class="sxs-lookup"><span data-stu-id="0e14e-105">This information includes such topics as supported data formats, compatibility information, programmatic identifiers, DCOM, and controls.</span></span>



| <span data-ttu-id="0e14e-106">Sottochiave</span><span class="sxs-lookup"><span data-stu-id="0e14e-106">Subkey</span></span>                                                                         | <span data-ttu-id="0e14e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e14e-107">Description</span></span>                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e14e-108">**AppID**</span><span class="sxs-lookup"><span data-stu-id="0e14e-108">**AppID**</span></span>](appid-key.md)                                                     | <span data-ttu-id="0e14e-109">Opzioni di configurazione per le applicazioni basate su COM.</span><span class="sxs-lookup"><span data-stu-id="0e14e-109">Configuration options for COM-based applications.</span></span>                                                                 |
| [<span data-ttu-id="0e14e-110">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="0e14e-110">**CLSID**</span></span>](clsid-key-hklm.md)                                                | <span data-ttu-id="0e14e-111">Opzioni di configurazione per le classi COM.</span><span class="sxs-lookup"><span data-stu-id="0e14e-111">Configuration options for COM classes.</span></span>                                                                            |
| [<span data-ttu-id="0e14e-112">**<estensione di file \_>**</span><span class="sxs-lookup"><span data-stu-id="0e14e-112">**<file\_extension>**</span></span>](-file-extension--key.md)                        | <span data-ttu-id="0e14e-113">Associa un'estensione di file a un ProgID.</span><span class="sxs-lookup"><span data-stu-id="0e14e-113">Associates a file name extension with a ProgID.</span></span>                                                                   |
| [<span data-ttu-id="0e14e-114">**FileType**</span><span class="sxs-lookup"><span data-stu-id="0e14e-114">**FileType**</span></span>](filetype-key.md)                                               | <span data-ttu-id="0e14e-115">Usato da [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) per trovare la corrispondenza dei modelli con diversi byte di file in un file non composto.</span><span class="sxs-lookup"><span data-stu-id="0e14e-115">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span> |
| [<span data-ttu-id="0e14e-116">**Interfaccia**</span><span class="sxs-lookup"><span data-stu-id="0e14e-116">**Interface**</span></span>](interface-key.md)                                             | <span data-ttu-id="0e14e-117">Associa un nome di interfaccia a un ID di interfaccia (IID).</span><span class="sxs-lookup"><span data-stu-id="0e14e-117">Associates an interface name with an interface ID (IID).</span></span>                                                          |
| [**<ProgID>**](-progid--key.md)                                         | <span data-ttu-id="0e14e-118">Identifica una classe.</span><span class="sxs-lookup"><span data-stu-id="0e14e-118">Identifies a class.</span></span> <span data-ttu-id="0e14e-119">Si noti che non è garantito che il ProgID sia univoco a livello globale, a differenza di un CLSID.</span><span class="sxs-lookup"><span data-stu-id="0e14e-119">Note that the ProgID is not guaranteed to be globally unique, unlike a CLSID.</span></span>                 |
| [<span data-ttu-id="0e14e-120">**<ProgID indipendente dalla versione>**</span><span class="sxs-lookup"><span data-stu-id="0e14e-120">**<version-independent ProgID>**</span></span>](-version-independent-progid--key.md) | <span data-ttu-id="0e14e-121">Utilizzato per determinare la versione più recente di un'applicazione per oggetti.</span><span class="sxs-lookup"><span data-stu-id="0e14e-121">Used to determine the latest version of an object application.</span></span>                                                    |



 

 

 




