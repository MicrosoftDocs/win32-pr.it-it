---
description: Specificare un'icona e un'etichetta personalizzate per un'unità.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Assegnare un'etichetta e un'icona personalizzate a una lettera di unità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979631"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a><span data-ttu-id="5f51f-103">Come assegnare un'etichetta e un'icona personalizzate a una lettera di unità</span><span class="sxs-lookup"><span data-stu-id="5f51f-103">How to Assign a Custom Icon and Label to a Drive Letter</span></span>

<span data-ttu-id="5f51f-104">Specificare un'icona e un'etichetta personalizzate per un'unità.</span><span class="sxs-lookup"><span data-stu-id="5f51f-104">Specify a custom icon and label for a drive.</span></span>

## <a name="instructions"></a><span data-ttu-id="5f51f-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="5f51f-105">Instructions</span></span>

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a><span data-ttu-id="5f51f-106">Passaggio 1: sostituzione dell'icona dell'unità standard con un'icona personalizzata in Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5f51f-106">Step 1: Replacing the standard drive icon with a custom icon in Windows 2000</span></span>

<span data-ttu-id="5f51f-107">Per sostituire l'icona dell'unità standard con un'icona personalizzata in Windows 2000, aggiungere una sottochiave denominata per la lettera di unità alla chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="5f51f-107">To replace the standard drive icon with a custom icon in Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

<span data-ttu-id="5f51f-108">Nell'esempio seguente vengono specificate un'icona e un'etichetta personalizzate per l'unità E:.</span><span class="sxs-lookup"><span data-stu-id="5f51f-108">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="5f51f-109">L'icona si trova nel file di \\MyDrive.exe C: mydir \\ con un indice in base zero di tre.</span><span class="sxs-lookup"><span data-stu-id="5f51f-109">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="5f51f-110">Per Windows 2000:</span><span class="sxs-lookup"><span data-stu-id="5f51f-110">For Windows 2000:</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a><span data-ttu-id="5f51f-111">Passaggio 2: sostituzione dell'icona dell'unità standard con un'icona personalizzata in tutte le altre versioni di Windows</span><span class="sxs-lookup"><span data-stu-id="5f51f-111">Step 2: Replacing the standard drive icon with a custom icon in all other versions of Windows</span></span>

<span data-ttu-id="5f51f-112">Per sostituire l'icona dell'unità standard con un'icona personalizzata in tutte le versioni di Windows diverse da Windows 2000, aggiungere una sottochiave denominata per la lettera di unità alla chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="5f51f-112">To replace the standard drive icon with a custom icon in all versions of Windows other than Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

<span data-ttu-id="5f51f-113">Nell'esempio seguente vengono specificate un'icona e un'etichetta personalizzate per l'unità E:.</span><span class="sxs-lookup"><span data-stu-id="5f51f-113">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="5f51f-114">L'icona si trova nel file di \\MyDrive.exe C: mydir \\ con un indice in base zero di tre.</span><span class="sxs-lookup"><span data-stu-id="5f51f-114">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="5f51f-115">Per tutte le altre versioni di Windows:</span><span class="sxs-lookup"><span data-stu-id="5f51f-115">For all other versions of Windows:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a><span data-ttu-id="5f51f-116">Passaggio 3: chiamata all'evento SHUpdateImage</span><span class="sxs-lookup"><span data-stu-id="5f51f-116">Step 3: Calling the SHUpdateImage Event</span></span>

<span data-ttu-id="5f51f-117">In tutte le versioni di Windows, se si modifica un tipo di file o un'icona di unità, è necessario chiamare anche SHUpdateImage per notificare alla shell di aggiornare le icone attualmente visualizzate.</span><span class="sxs-lookup"><span data-stu-id="5f51f-117">In all versions of Windows, if you change a file type or drive icon you must also call SHUpdateImage to notify the Shell to update any icons that are currently displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f51f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f51f-118">Remarks</span></span>

<span data-ttu-id="5f51f-119">La lettera di unità non deve essere seguita da due punti (:).</span><span class="sxs-lookup"><span data-stu-id="5f51f-119">The drive letter should not be followed by a colon (:).</span></span> <span data-ttu-id="5f51f-120">Aggiungere una sottochiave **DefaultIcon** alla sottochiave della lettera di unità e impostare il relativo valore predefinito su una stringa che contiene la posizione dell'icona.</span><span class="sxs-lookup"><span data-stu-id="5f51f-120">Add a **DefaultIcon** subkey to the drive letter subkey and set its default value to a string that contains the location of the icon.</span></span> <span data-ttu-id="5f51f-121">La prima parte della stringa contiene il percorso completo del file dell'icona.</span><span class="sxs-lookup"><span data-stu-id="5f51f-121">The first part of the string contains the fully-qualified path of the icon's file.</span></span> <span data-ttu-id="5f51f-122">Se nel file è presente più di un'icona, il percorso è seguito da una virgola, quindi dall'indice in base zero dell'icona.</span><span class="sxs-lookup"><span data-stu-id="5f51f-122">If there is more than one icon in the file, the path is followed by a comma, and then by the zero-based index of the icon.</span></span>

 

 



