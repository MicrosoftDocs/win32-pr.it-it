---
description: In Windows 7 e versioni successive, è possibile aggiungere verbi a una cartella usando Desktop.ini. Per ulteriori informazioni sui file di Desktop.ini, vedere How to Customize Folders with Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: Come implementare verbi personalizzati per le cartelle tramite Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979546"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="a3dcc-104">Come implementare verbi personalizzati per le cartelle tramite Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="a3dcc-104">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="a3dcc-105">In Windows 7 e versioni successive, è possibile aggiungere verbi a una cartella usando Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="a3dcc-105">In Windows 7 and later, you can add verbs to a folder by using Desktop.ini.</span></span> <span data-ttu-id="a3dcc-106">Per ulteriori informazioni sui file di Desktop.ini, vedere [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="a3dcc-106">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="a3dcc-107">I file di Desktop.ini devono essere sempre contrassegnati come nascosti dal **sistema**  +   , in modo che non vengano visualizzati dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="a3dcc-107">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="a3dcc-108">Per aggiungere verbi personalizzati per le cartelle tramite un file di Desktop.ini, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="a3dcc-108">To add custom verbs for folders through a Desktop.ini file, perform the following steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="a3dcc-109">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="a3dcc-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="a3dcc-110">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="a3dcc-110">Step 1:</span></span>

<span data-ttu-id="a3dcc-111">Creare una cartella contrassegnata come di sola **lettura** o di **sistema**.</span><span class="sxs-lookup"><span data-stu-id="a3dcc-111">Create a folder that is marked **Read-only** or **System**.</span></span>

### <a name="step-2"></a><span data-ttu-id="a3dcc-112">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="a3dcc-112">Step 2:</span></span>

<span data-ttu-id="a3dcc-113">Creare un file di Desktop.ini che includa un \[ . ShellClassInfo \] DirectoryClass = cartella ProgID.</span><span class="sxs-lookup"><span data-stu-id="a3dcc-113">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>

### <a name="step-3"></a><span data-ttu-id="a3dcc-114">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="a3dcc-114">Step 3:</span></span>

<span data-ttu-id="a3dcc-115">Nel registro di sistema creare **\_ le classi HKEY \_ radice** \\ **ProgID** con un valore CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="a3dcc-115">In the registry, create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="a3dcc-116">Il valore CanUseForDirectory evita l'utilizzo improprio dei ProgID impostati per non partecipare all'implementazione di verbi personalizzati per le cartelle tramite Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="a3dcc-116">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>

### <a name="step-4"></a><span data-ttu-id="a3dcc-117">Passaggio 4:</span><span class="sxs-lookup"><span data-stu-id="a3dcc-117">Step 4:</span></span>

<span data-ttu-id="a3dcc-118">Aggiungere i verbi nella sottochiave ProgID della **cartella** , ad esempio:</span><span class="sxs-lookup"><span data-stu-id="a3dcc-118">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a><span data-ttu-id="a3dcc-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3dcc-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a3dcc-120">Questi verbi possono essere i verbi predefiniti, nel qual caso fare doppio clic sulla cartella per attivare il verbo.</span><span class="sxs-lookup"><span data-stu-id="a3dcc-120">These verbs can be the default verbs, in which case double-clicking the folder activates the verb.</span></span>

 

 

 



